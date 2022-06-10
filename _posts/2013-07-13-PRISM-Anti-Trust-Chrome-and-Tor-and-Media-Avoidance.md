---
layout: post
title: PRISM - Anti-Trust, Chrome and Tor, and Media Avoidance
---

[Sneakers (1992)](http://www.imdb.com/title/tt0105435/) is one of my fav movies. In it Robert Redford leads an ethical hack team (played by Sidney Poitier, David Strathairn, Dan Aykroyd, and River Phoenix) down a rabbit hole of cryptography, government espionage, and [too many secrets](https://www.youtube.com/watch?v=G_XRqJV2zdk). Ever since, I've always assumed there is state-sponsored network monitoring, especially after the FBI implemented [Carnivore](https://en.wikipedia.org/wiki/Carnivore_(software)) in 1997, and [ECHELON](https://en.wikipedia.org/wiki/ECHELON) was reported in 2001.

On 06-Jun-2013 [news broke](http://www.washingtonpost.com/investigations/us-intelligence-mining-data-from-nine-us-internet-companies-in-broad-secret-program/2013/06/06/3a0c0da8-cebf-11e2-8845-d970ccb04497_story.html) of state-sponsored surveillance known as [PRISM](https://en.wikipedia.org/wiki/PRISM_(surveillance_program)), which reportedly utilises corporate collected data to monitor customer online activities and communications.

Steve Gibson](https://twit.tv/people/steve-gibson) explained PRISM as an industrial-scale implementation of [big-data](https://en.wikipedia.org/wiki/Big_data) ([Security Now #408](http://twit.tv/show/security-now/408)), and [TWIET #46](http://twit.tv/show/this-week-in-enterprise-tech/46) discussed the inherent lack of trust in government. It is apparent that the state believes it's citizens are guilty unless proven data-less.

The issue isn't whether or not secret state surveillance is happening. The issue is, why is it secret at all? And how will the captured data be stored and used?

# Anti-Trust

Supporters of state-sponsored surveillance argue "If you're not doing anything wrong, you have nothing to hide." Unfortunately this reasoning is not applied to PRISM itself; if it's so good, why was it secret?

<img src="https://upload.wikimedia.org/wikipedia/commons/f/f4/Censored_WPA_poster.jpg" width="200" style="float:right;">

An intelligence official released a declassified document on 15-Jun-2013 to "show Americans the value of the program" [according to AP](https://www.cbsnews.com/news/officials-nsa-programs-broke-terror-plots-in-20-nations/). However the program had previously been too good for public recognition.

During times of war, civil mail has been intercepted and even censored. In those cases, the public was notified that their [communications had been observed](http://www.postalcensorship.com/examples/ww2civilus/ww2civil_us16.html) by a state-sponsored agency. The state looked at (and sometimes removed) data, but everybody knew, and understood it was for the greater good of the nation.

PRISM looks at far more than mail meta-data, but currently the public (and the [senate](https://www.theverge.com/2013/7/23/4550434/senator-wyden-us-surveillance-state-fisa-prism-patriot-act)) is not permitted to know about it.

# Sheriff Analogy

<img src="http://upload.wikimedia.org/wikipedia/commons/0/0a/Deputy_sheriff_Mogollon_New_Mexico.jpg" width="200" style="float:right;">

Let's devolve the technology and consider a real-world analogy.

Imagine you live in a small rural town, where everyone knows everyone else, and the Sheriff  Alice cares for and looks after the citizens. While sitting on her porch she watches over Main Street, and notes when something seems out-of-place. With this knowledge she solves and prevents crime.


Unfortunately Sheriff Alice can't watch every street at once, so she gets Deputy Bob and Dylan on patrol, and they take note of everything they see. They report their observances to Sheriff Alice, and prevent crime.

The deputies also record and/or read the mail as it passes through the towns mail sorting centre. This helps them determine who is talking to whom, and what the topic of conversation is.

Unfortunately when criminal Eve sees the deputies, she doesn't commit crime, and she sends her mail in a unknown language. So the Sheriff appoints his deputies as undercover agents, to observe while concealed, and interpret the unknown language. Now they're getting better at preventing crime. Especially when they can keep all of their notes for an unlimited length of time.

So far, all of the deputies notes are of events occurring on public streets in plain view, and all of the mail is passing through a public service.

As far as we know PRISM is only capturing public digital traffic meta-data; looking for communication links and trends. So why is it so secret if it's doing nothing wrong?

What happens to the [5 zettabytes](https://www.nationalgeographic.com/pages/article/130612-nsa-utah-data-center-storage-zettabyte-snowden) of captured data? If Citizen Carol decides to run for Mayor, and Sheriff Alice doesn't like the Carol (or the incumbent Mayor tells Alice not to like Carol), the deputies can troll through year's worth of historical notes of Carol's actions, often without context, with the purpose of smearing her public-image, or persuading Carol to withdraw from the race.

The surveillance program becomes a mechanism to maintain power with the incumbent powerful. Particularly useful if you wish to dictate policy over a small rural town.

# Chrome and Tor

[How To: Google Chrome and Tor](/blog/2013-01-08-How-To-Google-Chrome-and-Tor/) was published on 08-Jan-2013, primarily after a query from a friend. It outlines how to use Tor to anonymise Google Chrome browsing. This would impede meta-data capture and big-data analysis of web-traffic, because the traffic would appear as originating from the Tor cloud, rather than a personal IP address. However, Tor only anonymises traffic, it does not encrypt it once it's outside the Tor cloud.

Pageviews increased around the time of PRISM disclosure on 06-Jun-2013. Pageviews jump up in May, before the disclosure (I'm not really sure why). The traffic in May and June is almost exclusively new visitors (91%), spending an average of 3:30 on the post.

For a comprehensive list of PRISM prevention technology, including web-traffic encryption, see [PRISM-BREAK](https://prism-break.org/).

# Media Avoidance

<img src="https://upload.wikimedia.org/wikipedia/commons/b/b1/PRISM_logo.jpg" width="200" style="float:right;">

Mainstream media has been focusing primarily on the messenger, and not the message. There are daily updates of the whereabouts of the [leaker](http://en.wikipedia.org/wiki/Edward_Snowden), and opinions of whether he is a traitor or patriot. Not much attention has been paid to the PRISM program itself.

This could be because of confusion and misunderstanding of what PRISM is, how it works,  future ramifications, and what it implies about state-policy. As with most mainstream reporting, whether discussing politics, finance, pandas, or motor vehicle accidents,  if it can't be told in 30 seconds, it can't be told.

Media avoidance could also be considered a trust issue; between news producers and the viewing/reading public. Even if media executives understood the security and privacy issues of PRISM, maybe they don't trust their audience to comprehend (or care), and so they choose not to try to discuss so as not to confuse. Unfortunately the lowest-common-denominator wins, and the dumbening continues.

# Conclusion

Please let me know what you think.
- Do you anonymise or encrypt your web-traffic?
- Should the media be explaining this better to the public?
- Have you seen Sneakers?

# Update 14-Jul-2013

Cameron Murphy (President of [NSW Council Of Civil Liberties](http://www.nswccl.org.au/)) spoke on ABC News24 at [13-Jul-2013 10:10AM](https://twitter.com/CameronMurphy__/status/355837425622335488) about similar issues raised by [Telstra surveillance](http://www.zdnet.com/telstra-agreed-to-retain-data-for-us-authorities-7000017986/). 
