---
layout: post
title: Don't Blink
---
Listening to [Security Now 263](http://twit.tv/sn263) this week Steve Gibson of [GRC](http://www.grc.com/) discussed Blink, a 'new' form of contactless smart credit card technology. Although this has been around since 2005, it's probably only becoming more common now, and hence a major security issue, as current cards expire and are replaced.

Steve described it as "the dumbest thing I've ever heard of in my life. I'm not kidding."

Basically it's an [RFID](http://en.wikipedia.org/wiki/Rfid) on your credit card so you can pass your card close to an in-store RFID scanner to make a purchase, instead of having to go to the inconvenience of manually 'swiping' and then having to pick up a pen and physically touch a piece of paper. 'It makes purchasing so much easier!'

Of course, this was developed prior to the current [financial crisis](https://en.wikipedia.org/wiki/Financial_crisis_of_2007%E2%80%932008), so marketers might not be so keen to tell people to go buy everything on credit.

A security concern that Steve discusses is the possibility of blink skimmers, a 'bad guy' walking around through shopping malls, train stations, and other crowded public areas with a skimming device, getting within inches of your wallet and skimming $25 from your blink credit card in seconds. The skimmer would leave a transaction trail, but could use offshore credit accounts to mask the trail, and hide in a foreign jurisdiction (maybe Nigeria!).

Alternatively, the skimmer might seek to not leave a $25 transaction trail, but instead steal the identity of the card itself, thus leading to credit card fraud on a grander scale. Chase bank state that 3DES symmetric encryption is used during the RFID negotiation and transaction. All you need is the shared key ... a good hacker should be able to determine that key using a bot-net in a couple of years. How long will these cards be around? Can they dynamically change keys?

Some links about the blink contactless card:
* http://www.chaseblink.com/faq.asp - the official blink page at Chase Bank
* http://www.youtube.com/watch?v=9nOtFsH9rbI - media reception to blink
* http://money.howstuffworks.com/personal-finance/debt-management/blink3.htm - how blink security works
* http://en.wikipedia.org/wiki/Contactless_smart_card - a general outline of contactless smart cards
* http://www.popularmechanics.com/technology/how-to/4206464 - a trick to keeping your RFID devices safe in your wallet (using ... Al Foil!)

So, if you get an RFID on your next credit card / passport / library card, what would you do?
