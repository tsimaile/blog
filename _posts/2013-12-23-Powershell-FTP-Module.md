---
layout: post
title: Powershell - FTP Module
---

I've been [learning Windows Powershell](http://blogs.technet.com/b/heyscriptingguy/) over the past year, and developing scripts for scheduled tasks to perform administrative functions. One of the tasks requires data retrieval from an FTP server, waits for the data to be processed, and then puts the results back to the FTP server.

![](../images/psftp.png)

Lots of FTP functions have been written and are freely available, but I've found [Michal Gajda](http://commandlinegeeks.com/)'s [PSFTP client module](http://gallery.technet.microsoft.com/scriptcenter/PowerShell-FTP-Client-db6fe0cb) the easiest and most efficient method. It has functions to set multiple connections, and list, get, put, and remove files and folders.

# Import-Module

The PSFTP module is not native to Powershell. To use the module, download and install, then import to access it's functions and perform FTP processes.
1. Download from <http://gallery.technet.microsoft.com/scriptcenter/PowerShell-FTP-Client-db6fe0cb>
1. Extract the module to your PS Module folder (found at $env:PSModulePath)
1. Import-Module using
```powershell
Import-Module PSFTP
```

# Local Variables

Now for the administrative task I was working on. Some local variables are declared for use throughout the script:
```powershell
$ftp_server = "ftp://example.server.com"
$ftp_path = "$ftp_server/folder1/subfolder2"
$local = "\\localserver\sharedfolder1\subfolder2\"
$local_in = Join-Path $local "In"
$local_out = Join-Path $local "Out"
$session = "my_ftp_session"
```

# Credentials

The connection credentials should not be stored in clear-text, but loaded from a SecureString file (which has been created using the appropriate account on the appropriate server). To establish the credentials:
```powershell
# set up credentials object
$username = "username"
$password = Get-Content "pscredentials_$username.txt" | 
    ConvertTo-SecureString
$cred = New-Object `
    -TypeName System.Management.Automation.PSCredential `
    -ArgumentList $username, $password
```

# Get Items

To input the files from FTP to local folder:
```powershell
# establish connection
# get *.REQ files
# copy *.REQ files to local In folder
# remove *.REQ files from FTP server
Set-FTPConnection -Server $ftp_server -Credentials $cred `
    -Session $session -KeepAlive -UseBinary
Get-FTPChildItem -Path $ftp_path -Filter *.REQ -Session $session | 
% {
    $ftp_file = "$ftp_path/$($_.Name)" # determine item fullname
    Get-FTPItem -Path $ftp_file -LocalPath $local_in `
        -Session $session -Overwrite
    Remove-FTPItem -Path $ftp_file -Session $session
}
```

# Put Items

After the data arrives at the local In folder it is processed by a separate application, which returns output to the local Out folder. It can then be put to the FTP server with:
```powershell
# get all files in local Out folder
# put all files to FTP server
Get-ChildItem -Path $local_out |
% {
    $ftp_file = "$ftp_path/$($_.Name)" # determine item fullname
    Add-FTPItem -Path $ftp_file -LocalPath $_.FullName -Session $session
}
```

# Notes

1. The Get and Put actions have been performed within foreach loops ( % {} ) for logging purposes, such that action results are recorded to a text file for later reference. It would be more efficient to pipe the ChildItem results directly, but logging is important for historical tracing and action confirmation.
1. The code lines could be shorter with the use of aliases, for example, by replacing Get-ChildItem with ls, and Copy-Item with cp. I don't use aliases (except foreach loops) for a couple of reasons:
    * using aliases doesn't make code production faster (due to Tab completion)
    * using full commands makes code more readable

Powershell is a great tool for Windows administration. I hope to continue learning thanks to the [Scripting Guy](http://blogs.technet.com/b/heyscriptingguy/), and shared [script resources](http://gallery.technet.microsoft.com/scriptcenter/site/search?f%5B0%5D.Type=ProgrammingLanguage&f%5B0%5D.Value=PowerShell). How have you used Powershell?