# BriarIDS

<b>Be sure to check out the <a href="https://github.com/musicmancorley/BriarIDS/wiki">WIKI</a> for detailed instructions and further information!  I've updated it with plenty of useful information</b>

Feeling generous?  Why not shoot me a $1 and I'll add it to the Briar fund.  I'd like to test out some additional hardware TAP devices down the road and other complimentary hardware solutions.  This would allow for more extensive logging and with your help we can make this goal a reality! https://www.paypal.me/BriarIDS/1

If BriarIDS is used for educational purposes in the classroom setting (ie. Network Security courses, etc) please send me some feedack if you dont' mind, letting me know how it cooperated.  Thanks!

Introduction
============
A simple yet effective IDS for the Raspberry PI.  BriarIDS is configured to work with Raspbian and takes advantage of the PyQT GUI frontend for an all-in-one solution that monitors your home network.  Bro is now integrated into the BriarIDS GUI for additional logging options.  Snorby is still a work in progress concerning an automated installation.  Will post progress notes on wordpress site periodically.  
<img src="https://github.com/musicmancorley/BriarIDS/blob/master/briarimage.png">
Why the name BriarIDS?
=======================
It's kinda cheesy.  The name comes from the protection Briars and Brambles (Raspberry bushes) give to rabbits when under attack.  
So how's it different from other IDS solutions?
===============================================
It's not really.  The key difference is how it's setup.  This is a home network based IDS solution using Suricata that primarily monitors WAN traffic (LAN too if you wanted).  I looked all over the web for a SIMPLE home-based IDS using the PI and getting a network TAP working; I didn't have much luck.  I'll reemphasize that there were Raspberry PI solutions out there, some that were quite amazing.  They just weren't very agreeable with home network-based configurations.  I just wanted a simple command-line solution that's cooperative in a few minutes upon installation.  Snorby and SGUIL and all the other GUI frontends are always awesome secondary add-ons and those will be integrated into BriarIDS shortly.  For now, I just want to provide a simple working IDS that is fairly straight forward and user friendly.
Why the Raspberry Pi?
====================
Since I wanted to provide the most cost effective and feasible solution for homeowners to protect their network, I knew a Raspberry PI would fit the bill assuming it cooperated.  A PI will run you roughly $40-$60 with a decent SDcard purchased along with it. Next, as we all know, you need a tap interface or some way to get packets into your monitoring interface.  While there are other somewhat reasonably priced solutions out there, I decided to take advantage of what I already had to work with at the house.  That's where Tomato Router firmware comes in.  The IPTables --tee functionality did the job and copied all my WAN packets over to the Raspberry Device with ease.  Once things began cooperating I wanted to share this solution with everyone.  I know I can't be the only one out there who desires to have an easy and affordable solution for their home network security perimeter.
What OS does it run on?
=======================
Raspbian
Can this be ported to other OSes?
=================================
Yup.  Try it out in a VM running the latest Debian or Ubuntu.  It should cooperate with the exception of the critical-stack agent.  You will want to download the intel x86/x64 .deb file versus the .arm currently set to download in the script.
What Router(s) have you tested this with?
=========================================
Just the Linksys E1200v2 thus far
What Tomato firmware version are you using?
======================================
tomato-E1200v2-NVRAM64K-1.28.RT-N5x-MIPSR2-132-Max.bin
I have more questions...
========================
I hoped you would.  Check out the wiki and let me know what needs to be added.
