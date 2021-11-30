---
layout: post
title: Backup Regime
---

Originally posted on 28-Feb-2009 at: [http://groups.yahoo.com/group/csteachers/message/13472](http://groups.yahoo.com/group/csteachers/message/13472)
Reposted here for posterity (and in the event that Yahoo! ...).

# Question

<ggeorgoulopoulos@...> wrote:
> 1. Can someone tell me how far back one can expect to be able to back up from in his or her particular organisation - is it more than a week?
> 1. Now, can someone tell me of an application that can a) back up students work, in the first case and b) backup up modified files in the second case and, c) create a separate folder/file in the destination with those files that have been modified since the last update

# Answer

> Howdy George et.al.,
> 
> 1. At Kadina HS we keep an archive of data from end-of-year, stored on external HDD as NTbackup bkf file via Windows Server 2003. This policy has been in place since 2007.
> 1. Using NTBackup we use scheduled scripts to perform a full-backup of admin/staff and student data each week (over the weekend). The script wipes the external HDD and creates an encrypted (EFS) folder for archiving. Then each week-night (except Fri) a scheduled script will perform an incremental backup (around 6PM).
> 
> Each Friday the external HDD is replaced with another (rotating between three). Since we are using incremental backups; we can therefore restore any file to it's state on any day in the last three weeks. The external HDDs are stored off-site at my house (approximately 6 mins from the school). They are encrypted, so there should be no privacy issues if the HDDs are lost or stolen while off-site.
> 
> At the end of term a HDD is removed from rotation, and a 4th HDD is introduced which was removed the term before that. So it's possible to restore data from last term.
> 
> At the end of year a new HDD is purchased and introduced to the rotation, and the last HDD of the year is removed to permanent archive.
> 
> I think George's second question is mainly about using full and incremental backups. NTBackup can do this fine.
> 
> Also, for freeware at home I use [Cobian Backup](https://www.cobiansoft.com/cobianbackup.html) 9 which easily sets up scheduled full, incremental, and differential backups in zip and encrypted formats. For the difference between these try wikipedia.
> 
> BLURB: While formulating the school's backup policy we did a lot of research and talked to a lot of people. We wanted something that was simple to restore (quickly find data and retrieve), used med- to high-level encryption for privacy (not just a zip password), and easy to maintain (i.e. minimal user interactions). We considered purchasing Symantec Backup Exec but found that it's encryption was too complex to implement. We have been using the above method succesfully, able to meet several requests to restore specific data to a specific date. Of course, all of this may be defunct once the DET introduces eBackPacks for students (and staff?).
> 
> Cheers,
> Tim Simaile IPT/SDD,
> Kadina High School NSW

## addendum

> At the beginning of 2011 we implemented Windows Server 2008, but I've found their native backup system confusing, and retrieval difficult. So I've resorted back to the latest [Cobian](https://www.cobiansoft.com/cobianbackup.html). If you use, and you like, please donate and support open-source sofwtare developers.