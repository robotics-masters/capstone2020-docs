# Guide to fix Unity Crash

As posted on Slack

Calum Sep 19th at 12:48 PM

@Ben looks like I'm getting your crash issues with unity now...

    • what version would you reccomend?

    • what steps did you take to prolong the crash?

5 replies

Ben Sep 19th

Hi, I hope I can help.

what errors are you getting are they the same involving JITCompiler and or burst 1.1.1

If you have other errors or issues please advise specifically

How many errors?

Take screenshots of all, or some record of them.

especially note the 1st few and last few.

Does it crash immediately, or on PLAY or in 10min or in 1 hour

Read all this first.

My version is Ubuntu 20.04.1 lts

My Unity is 2019.4.10f1

The version you choose is your choice

It seems more stable now didn't crash yesterday, used it for 5? hours in our sandbox project.

My unity seems stable now

Is this when you open a new project, or the sandbox we are collaborating on, or a tutorial?

It seems that the Kart tutorial definitely has issues with burst. don't open that tutorial for now.

To learn unity watch these 1st instead: https://learn.unity.com/tutorial/using-the-unity-interface#

See Unity 101 in slack resources

and User Manual (for reference) https://docs.unity3d.com/Manual/UnityOverview.html

Steps

Turn off, start fresh,

Turn on, don't open anything else

make sure you are online

(a few times I was offline)

Don't open any tutorial just open a new unity project. Don't click PLAY.

In Unity go to window > package manager

give it a minute to refresh the list from local and server.

there is a filter for registry or for project

choose to the registry.

The package manager is inside Unity, you need to have it open and have stay open long enough to use it.

find

install or upgrade to burst >= 1.3.3

I now have burst 1.3.6Be advised that its 300MB+

After installing Burst >= 1.3.3

Turn off, start fresh,

Turn on, don't open anything else

make sure you are online

Open unity, the sandbox

Unity support replied to my report and said: "Thanks for getting in touch, we actually know about this issue (https://protect-au.mimecast.com/s/cSPECzvkyVCz5nOLF4RO5J?domain=issuetracker.unity3d.com). It's marked as "Won't Fix", but actually it is fixed (or no longer reproduces) in "Burst" version 1.3.3 and newer. The package can be updated through the Package Manager."

They had other advice BUT

I did NOT do apt-get DONOT install libc6-dev-amd64 libc6-dev-i386 libncurses5

My libc6-dev was fine

Did not change

libc6-dev is already the newest version (2.31-0ubuntu9)

My libncurses6 was fine

Did not change

libncurses6 is already the newest version (6.2-0ubuntu2)

I also have gcc 9.3 and clang 10 and java openjdk 11 installed

Surprisingly I found that The FPS doesn't have that issue with burst 1.1.1

Later try to open the FPS tutorial it worked much better than the Kart.

Don't Start the tutorial close the 1st popup window, save the tutorial project.

Save the project so it doesn't need to decrompress again.

My Kart tutorial crashed when I tried to save it, So,

If it can't be saved, while its open,  copy it from /tmp/ ########## / into your /home/ somewhere.

to find the /tmp/ path look at the folder timstamps, or the error messages.

later find it in your unity hub and open it that way, faster to open next time and more stable.

This is after the above

If a tutorial or project has burst issues, use the package manager set filter to project, apply the burst > 1.3.3 package, shouldn't need to download again

Try the FPS tutorial

I completed it

Try the Kart Tutorial

I completed it

Good luck

Let me know (edited) 



Calum  16 days ago

Thanks for the help, trying now



Calum  16 days ago

Ok, excellent advice on copying the package from /tmp and installing burs 1.3.6. Seems to be working now, I made it through the kart tutorial



Calum  16 days ago

Thank you very much



Ben  16 days ago

Very happy to hear

(heart) 1
