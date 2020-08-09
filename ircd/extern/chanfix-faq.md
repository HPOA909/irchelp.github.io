---
title: EFNet International Services - Chanfix Module FAQ
author: William Rockwood
dateupdated: 14 July 2001
status: historical
layout: default
---
# EFNet International Services - Chanfix Module FAQ

**q)** Will chanfix work on my +i/+k/+l channel? What if `*!*services@services.int` is banned on my channel?   
**a)** Yes. It will, in fact, leave all modes intact, so if the channel is `+snk foo`, it will remain that way after chanfix has left. Chanfix can join through any bans, modes, etc, so it will be unaffected by any bans. 

**q)** What are the exact requirements for me to be considered a valid client when chanfix samples my channel?   
**a)** You must run identd (you can't have a ~ at the beginning of your username,) your host must be non-dynamic/dialup and your host must have working forward and reverse DNS (IP addresses can not be known by chanfix to be static or dynamic, so it must ignore them.) If you are confused by any of this, please visit [irchelp.org](http://www.irchelp.org/). 

**q)** We don't believe in identd, it's silly and can be easily faked. We simply will not install this on our (system, shell server, etc..) -or- I'm behind a firewall and my firewall administrator won't open up port 113.   
**a)** Chanfix will only consider a client valid if it is idented and is on a non-dynamic/dialup hostname. There are many reasons for this, but the main reason is, we felt this was the best we could do to assure that people do not masquerade as you from your shell service which does not provide identd or your adsl/cable connection which could be easily "spoofed" or "masqueraded" as. We understand your feelings; identd is indeed rather meaningless, but the benefits from requiring it outweigh logic. Firewalled users will need to find another way onto IRC if they wish to be counted in a channel. We realize that this is difficult in many cases, but hopefully you'll still be okay. :) 

**q)** What happens when the network splits in half? Will chanfix operate all alone on one half of it and not on the other?   
**a)** No, chanfix requires that at least 3/4 of the network be present in order for it to both add statistics and to act on opless channels. Once the net has rejoined, chanfix will resume its statistics gathering and will re-op any opless channels with sufficient samples in its database. 

**q)** My channel has been taken over by someone because we oped the wrong person or my botnet was hijacked or hacked, will chanfix help us?   
**a)** While this functionality is being discussed, there is currently no way for chanfix to restore the channel to you. Essentially, chanfix has no concept of "sides" or "ownership" -- it just looks at its scorecard and will only intervene if a channel is entirely opless. Remember, chanfix does not understand "right" or "wrong" just "how many samples does this particular chanop appear in?" 

**q)** What if all the ops in my channel log off at once and while there are still users in my channel, none of the people who are ops are there? Will we get ops when we get back?   
**a)** Short answer: Yes. Long answer: While we would like to think that that is how it would work exactly, there are circumstances that can cause someone to regain ops -without- chanfix, during your absence, so, in the spirit of not actually recognizing channel ownership, we can not guarantee that the channel will still be available when you get back. 

**q)** How many people need to be in my channel for it to be seen by chanfix and for it to take these samples? How long must a channel exist for chanfix to act on it if it becomes opless?   
**a)** Currrently, 4 people must be in a channel, at least one of these must be a valid chanop. Your channel must exist (currently) for 30 minutes (assuming a 5-minute sample rate), or 6 samples must have been taken for the channel. 

**q)** My channel was just taken over. How long will it be before the new ops in the channel are recognized by chanfix as the people that it will re-op?  
**a)** That all depends. The chanfix database spans a period of 2 weeks right now, at some point that may be made longer. You will have to figure out how long you have before the new ops are considered by chanfix to be the primary ops of the channel.

**q)** My channel is opless but chanfix isn't fixing it. What do I do now?   
**a)** This could be happening for a number of reasons. If you are certain that you have an idented connection and the channel meets the minimum requirements, it could be that `services.int`, the server that chanfix operates from, is not currently on the network, or there are not enough servers present for it to operate. It could also be that the channel was oppless before chanfix was introduced to the network on July 10th (i think)-- we may have a few options for you soon, probably none of them terribly pretty. Chanfix makes no claims to be perfect, all you can really do is keep your fingers crossed. The folks in `#help` or `#irchelp` may be able to help you also. 

**q)** Who do you think you are? I want my channel OPLESS !@#$#@ darnit!  
**a)** Sorry for the inconvenience. If you'd like, you could uninstall identd and/or make sure there are less than 4 people in the channel. While we do have the ability to tell services -not- to fix a channel, we are unable to do this by user request. Our sincerest apologies and thanks for your understanding. 

**q)** What is the nickname of the "bot" that ops me?   
**a)** Just to make it clear, it's not a "bot" -- it's just a construct of the server it runs on. "Right now" its nickname is "JUPES" but very soon now, that will change to "SERVICES". Here's what it will look like when it joins when/if you lose ops on a channel:  
`*** JUPES (services@services.int) has joined channel #services`

`*** mode change "+o JUPES" on channel #services by services.int`

Here is where it ops you, then leaves the channel as swiftly as it joined.

**q)** If I am the only op in the channel and there are many non-ops and I get disconnected for some reason, will i get ops when i join back to the channel?   
**a)** Possibly. If the channel still has at least 4 members and is still opless when you return, chanfix will give you ops sometime within the next 5 minutes. 

If these questions and answers are still not answering your questions, you can
email me (link below) and if your question is intelligently posed and I feel
it has not been adequately answered by this FAQ, I will reply to you and
include your question in the official FAQ (yes, your identity will remain
anonymous :). Additionally, you may choose to make a post on the efnet.org
public forums. Please keep in mind that the efnet.org staff are not
representative of chanfix or services.int and may or may not know the answers
to your questions. I'll try to look through the forum from time to time to see
if there are any questions there that I can answer, but it is entirely
possible that I won't always have time to do so. Thanks for your interest and
all the encouragement. :-)

-will 

* * *

_ Written by [William
Rockwood](mailto:rockwood@concentric.net?subject=SERVICES+CHANFIX+FAQ) for
[EFNet](http://www.efnet.org/)

References: [Chanfix Protoservice
Proposal](https://voting.blackened.com/pastvotes/0014.shtml)

Last updated: Sat Jul 14 23:45:45 CDT 2001

