Introducing PetHack, a NetHack variant for pet lovers!



PREMISE \& NOTES

* PetHack is a simple variant geared towards pet lovers. It makes it easier to obtain and manage pets while still having the classic NetHack feel.
* PetHack is based on NetHack 5.0.0. This will likely be the only release of PetHack unless there are bugs. The goal was not to make extreme changes, but rather to upgrade and serve a specific playstyle.
* There is also an Android port of PetHack! It is based on JodiJodington and gurr’s Android ports for NetHack: 
* I am very, *very* new to coding and GitHub. If there are any issues with the game or repository, please let me know and I will do my best to fix them!



CHANGELOG

* Changed Tourist role

  * They now start with 3-5 tripe rations, 3-5 scrolls of taming, a blessed spellbook of charm monster, a blessed magic whistle, a sack, a leash, and a blessed random figurine *in addition* to their original starting equipment

    * The figurine is completely random, meaning it can be any monster (not based on level/depth) while still following normal figurine generation rules
  * They now start with Basic in enchantment spells and can reach Expert
* Changed charm monster back to a level 3 spell
* If you throw an item to an intelligent pet with hands, they will catch it and equip it if applicable. They will prioritize using items you give them over other items. This idea came from FIQHack.
* Intelligent pets will now hoard healing potions even when they're healthy. Be careful to manage this properly!
* Rebalanced figurine BUC effects

  * Blessed: 100% tame
  * Uncursed: 10% tame, 70% peaceful, 20% hostile
  * Cursed: 0% tame, 10% peaceful, 90% hostile
* New store: Toy store

  * This is a shop that only sells figurines. Figurines that generate in toy stores (or shops in general) can also be of any monster regardless of the player’s level and depth. 
  * Figurine base prices now scale with the monster’s difficulty (difficulty x 50). For example, figurines of Archons will be expensive, while figurines of lichens will be cheap.



Below is NetHack’s original README file in case you would like to reference it. Good luck, and happy hacking!





&#x20;        NetHack 5.0.0 -- General information



NetHack 5.0 is an enhancement to the dungeon exploration game NetHack,

which is a distant descendent of Rogue and Hack, and a direct descendent

of NetHack 3.6.



NetHack 5.0.0 is a release of NetHack. As a .0 version, there may be some

bugs encountered. Constructive suggestions, GitHub pull requests, and bug

reports are all welcome and encouraged.



The file doc/fixes5-0-0.txt in the source distribution contains a full list

of fixes and changes as they were committed. The text in there was written

for the development team's own use and is provided  "as is", so please do

not ask us to further explain the entries in that file. Some entries might

be considered "spoilers", particularly in the "new features" section.



Along with the game improvements and bug fixes, NetHack 5.0 strives to make

some general architectural improvements to the game or to its building

process. Among them, 5.0 has:



&#x20;\*  The source code is compliant with the C99 standard.



&#x20;\*  removes barriers to building NetHack on one platform and operating system,

&#x20;   for later execution on another (possibly quite different) platform and/or

&#x20;   operating system. That capability is generally known as "cross-compiling."

&#x20;   See the file "Cross-compiling" in the top-level folder for more information

&#x20;   on that.



&#x20;\*  The build-time "yacc and lex"-based level compiler, the

&#x20;   "yacc and lex"-based dungeon compiler, and the quest text file processing

&#x20;   previously done by NetHack's "makedefs" utility, have been replaced with

&#x20;   Lua text alternatives that are loaded and processed by the game during play.



Here are some other general notes on the changes in NetHack 5.0 that were not

considered spoilers:

&#x20;-  automatic annotation "gateway to Moloch's Sanctum" for vibrating square

&#x20;       level once that square's location becomes known (found or magic

&#x20;       mapped); goes away once sanctum temple is found (entered or high altar

&#x20;       mapped)



&#x20;                       - - - - - - - - - - -



Please read items (1), (2) and (3) BEFORE doing anything with your new code.



1\.  Unpack the code in a dedicated new directory.  We will refer to that

&#x20;   directory as the 'Top' directory.  It makes no difference what you

&#x20;   call it.



2\.  Having unpacked, you should have a file called 'Files' in your Top

&#x20;   directory.



&#x20;   This file contains the list of all the files you now SHOULD

&#x20;   have in each directory.  Please check the files in each directory

&#x20;   against this list to make sure that you have a complete set.



&#x20;   This file also contains a list of what files are created during

&#x20;   the build process.



&#x20;   The names of the directories listed should not be changed unless you

&#x20;   are ready to go through the makefiles and the makedefs program and change

&#x20;   all the directory references in them.



3\.  Before you do anything else, please read carefully the file called

&#x20;   "license" in the 'dat' subdirectory.  It is expected that you comply

&#x20;   with the terms of that license, and we are very serious about it.



4\.  If you are attempting to build NetHack on one platform/processor, to

&#x20;   produce a game on a different platform/processor it may behoove you to

&#x20;   read the file "Cross-compiling" in your Top directory.



5\.  If everything is in order, you can now turn to trying to get the program

&#x20;   to compile and run on your particular system.  It is worth mentioning

&#x20;   that the default configuration is SysV/Sun/Solaris2.x (simply because

&#x20;   the code was housed on such a system).



&#x20;   The files sys/\*/Install.\*, or sys/\*/NewInstall.\* were written to guide

&#x20;   you in configuring the program for your operating system.  The files

&#x20;   win/\*/Install.\* are available, where necessary, to help you in

&#x20;   configuring the program for particular windowing environments.

&#x20;   Reading them, and the man pages, should answer most of your questions.





&#x20;   At the time of the most recent official release, NetHack 5.0, it had

&#x20;   been tested to run and/or compile on:



&#x20;       Intel Pentium or better running Linux, BSDI

&#x20;           \[compiles, runs]

&#x20;       Intel Pentium or better running Windows 10 or 11

&#x20;           \[compiles, runs]

&#x20;       Intel-based, or Apple M1, M2, M3, M4, M5 Macs running

&#x20;           \[compiles, runs]

&#x20;           macOS 10.11 (El Capitan) to macOS 26 (Tahoe) \[compile, run]

&#x20;           (follow the instructions in sys/unix/NewInstall.unx)

&#x20;       Intel 80386 or greater running MS-DOS with DPMI

&#x20;           \[cross-compiles on Linux, runs on MS-DOS, emulator/dosbox]

&#x20;           built via djgpp compiler (native or Linux-hosted cross-compiler)

&#x20;       AmigaOS 3.0 or later

&#x20;           \[cross-compiles on Linux or macOS, runs on Amiga or emulator]

&#x20;           Running requires Kickstart 39+

&#x20;           6 MB free RAM minimum (8 MB recommended)

&#x20;           Hard drive with \~5 MB free space



&#x20;   There has also been some success runing/comiling on:

&#x20;       OpenVMS (aka VMS) V8.4 on Alpha and on Integrity/Itanium/IA64

&#x20;       OpenVMS (ask VMS) V9.2-3 on x86-64



&#x20;                       - - - - - - - - - - -



If you have problems building the game, or you find bugs in it, we recommend

filing a bug report from our "Contact Us" web page at:

&#x20;   https://www.nethack.org/common/contact.html

Please include the version information from #version or the command line

option --version in the appropriate field.



A public repository of the latest NetHack code that we've made

available can be obtained via git here:

&#x20;   https://github.com/NetHack/NetHack

&#x20;     or

&#x20;   https://sourceforge.net/p/nethack/NetHack/



When sending correspondence, please observe the following:

o Please be sure to include your machine type, OS, and patchlevel.

o Please avoid sending us binary files (e.g. save files or bones files).

&#x20; If you have found a bug and think that your save file would aid in solving

&#x20; the problem, send us a description in words of the problem, your machine

&#x20; type, your operating system, and the version of NetHack.  Tell us that you

&#x20; have a save file, but do not actually send it.

&#x20; You may then be contacted by a member of the development team with the

&#x20; address of a specific person to send the save file to.

o Though we make an effort to reply to each bug report, it may take some

&#x20; time before you receive feedback.  This is especially true during the

&#x20; period immediately after a new release, when we get the most bug reports.

o We don't give hints for playing the game.

o Don't bother to ask when the next version will be out or you can expect

&#x20; to receive a stock answer.



If you want to submit a patch for the NetHack source code via email directly,

you can direct it to this address:

&#x20;   nethack-bugs (at) nethack.org



If a feature is not accepted you are free, of course, to post the patches

to the net yourself and let the marketplace decide their worth.



All of this amounts to the following:  If you decide to apply a free-lanced

patch to your 3.6 code, you are welcome to do so, of course, but we won't

be able to provide support or receive bug reports for it.



In our own patches, we will assume that your code is synchronized with ours.



&#x20;                 -- Good luck, and happy Hacking --



\# $NHDT-Date: 1652133501 2022/05/09 21:58:21 $ $NHDT-Branch: NetHack-3.7 $:$NHDT-Revision: 1.97 $

\# Copyright (c) 2012 by Michael Allison

\# NetHack may be freely redistributed.  See license for details.



