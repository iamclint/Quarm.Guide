# EverQuest Project Quarm Getting Started Guide (Updated: April 24, 2024)
##### By Xanax/Xantagonist < Former Glory > 

## Table of Contents
1. [Part 1: Installing the Main Game](#part-1-installing-the-main-game)
    - [Step 1: Create a TAKP Forum Account](#step-1-create-a-takp-forum-account)
    - [Step 2: Download the Game Client](#step-2-download-the-game-client)
    - [Step 3: Converting your TAKP client to Quarm](#step-3-converting-your-takp-client-to-quarm)
    - [Step 4: Installing Zeal](#step-4-installing-zeal)
    - [Step 5: dgVoodoo2](#step-5-dgvoodoo2)
    - [Step 6: Issues Running the Game](#step-6-issues-running-the-game)
2. [Xanax's Checklist for Minimal Crashes](#xanaxs-checklist-for-minimal-crashes)
3. [Part 2: Installing Optional Textures and Effects](#part-2-installing-optional-textures-and-effects)
4. [Part 3: Installing Optional 3rd Party Programs](#part-3-installing-optional-3rd-party-programs)
5. [FAQ](#faq)
6. [Suggestions Feedback and Help](#suggestions-feedback-and-help)

## Part 1: Installing the Main Game

#### Backup Warning - Anytime you change something or overwrite a file, backup that file, backup the whole TAKP folder if you want. It's easy and fast and I'm not going to remind you to backup files after every step. - Backup Warning

### Step 1: Create a TAKP Forum Account
Before you can download and install the game, you'll need to create an account on the TAKP forums.

**NOTE: You must only create 1 forum account. You can create up to 10 game accounts under your forum account, but you must not create more than 1 forum account. If this is detected, the extra forum accounts will be deleted, and access to any game accounts associated with them will be lost. Also, please name your forum and game accounts carefully as these cannot be changed or deleted after creation. Read the forum FAQ and Rules for more information [here](https://www.takproject.net/forums/index.php?forums/server-info.90/).*

1. Visit the following link and follow the instructions to register a new account: [Login](https://www.takproject.net/forums/index.php?login%2F)

2. Once you have created a forum account and are logged in, navigate to the "Game Accounts" section.

3. Click "Create Login Server Account" and create a game account.

### Step 2: Download the Game Client
1. Visit the Getting Started page on the TAKP wiki: [Getting Started](https://wiki.takp.info/index.php?title=Getting_Started)
2. Click on the "Getting Started with Windows" section.
3. Download the stable 2.1 version of the game client [here](https://www.dropbox.com/s/bppy4ebt7vl7hwk/TAKP%20PC%20V2.1c.zip?dl=0), or use the latest 2.2 version [here](https://drive.google.com/file/d/1qoBktDeJMJKPBr-EZxub1vspJhz11i1y).

### Step 3: Converting your TAKP client to Quarm
1. Join the [Project Quarm Discord](https://discord.gg/3nDQ9AkUz8).
2. Navigate to the #server-files channel.
3. Download the `eqgame.dll` file from the following message [#server-files](https://discord.com/channels/1133452007412334643/1135981619858128998/1170491429253034047). This is the latest stable release.
   An experimental release of `eqgame.dll` can be found under [#zeal-discussions](https://discord.com/channels/1133452007412334643/1210670176077348934/1227704216655761499).
5. Extract the `eqgame.dll` file to your TAKP folder (where you installed the game client).

#### Source: [LevelUpLarry](https://www.youtube.com/watch?v=u83_FICd97c)

### Step 4: Installing Zeal

Zeal is used to add additional functionality to EverQuest. Main additions include camera smoothing, better tab targeting, spell sets, and melody. A full list of features can be found in the [readme](https://github.com/iamclint/Zeal/blob/master/README.md).

#### Prerequisite 1. (Required) Enable sound in your eqclient.ini

Make sure Sound=TRUE is listed in your `eqclient.ini`. Zeal uses the EverQuest sound engine to inject code into the game, thus the sound must be enabled for Zeal to function. You will still have access to various sound options in game by pressing ALT + O and adjusting the sliders for Sound Realism, Music Volume, and Sound Volume.

#### Prerequisite 2. (Required) Excluding your TAKP Installation
Excluding your TAKP installation from being scanned by your antivirus software can also help reduce load times, zoning times, and eliminate stuttering when opening your bags. This is highly recommended and is a prerequisite for downloading Zeal, as explained below.

##### Windows 10

 Instructions for performing the above through Windows Settings panel:

*This may be slightly different for the different versions of Windows 10. This was taken from the 1909 version released late 2019.*

-Right click the windows button in the lower left hand corner and select search.

![Defenderexclusion1](/img/step4/Defenderexclusion1.png)

- Search for and select Windows Security.

![Defenderexclusion2](/img/step4/Defenderexclusion2.png)

- Click Virus and threat Protection.

![Defenderexclusion3](/img/step4/Defenderexclusion3.png)

- Under Virus and threat Protection settings, click manage settings.

![Defenderexclusion4](/img/step4/Defenderexclusion4.png)

- Under exclusions, click Add or Remove Exclusions.

![Defenderexclusion5](/img/step4/Defenderexclusion5.png)

- Click Add an exclusion and select Folder.

![Defenderexclusion6](/img/step4/Defenderexclusion6.png)

- Select the folder that you currently have (or intend to have) the TAKP files extracted into and run from when you play.

##### Powershell

Open administrative PowerShell and type in the below, replace C:\TAKPv22 folder path with where you unzipped the game files.

`Add-MpPreference -ExclusionPath "C:\TAKPv22"`

`Add-MpPreference -ExclusionProcess "C:\TAKPv22\eqgame.exe"`

![AV_Exclusions_PowerShell_Example](/img/step4/AV_Exclusions_PowerShell_Example.png)

#### Why is Zeal getting flagged as a Virus/Malware?
Zeal is a file that adds new features and improvements to EverQuest by injecting custom code into the game's sound engine. This process is called code injection. While code injection is sometimes associated with malware or viruses because it modifies the game files, Zeal serves a legitimate purpose in enhancing the gaming experience.

However, because Zeal is currently in early development and does not have a digital signature, it may be flagged as potentially harmful by antivirus software. A digital signature is a way to verify that a file is safe and comes from a trusted source. Since Zeal does not have this signature yet, antivirus programs treat it with suspicion.

The Project Quarm team plans to address this issue by obtaining a digital certificate from Microsoft to sign Zeal in the future. This digital signature will confirm that Zeal is a legitimate and safe program, eliminating any concerns about its legitimacy.


#### Download and Extract Zeal.asi to your TAKP Folder
1. To download Zeal, visit the project's GitHub repository at and navigate to the '[Releases](https://github.com/iamclint/Zeal/releases)' section. You'll find the latest version available for download in a file named `zeal.zip`. Ensure that you have previously excluded your TAKP folder from virus scans, as discussed in the previous step.
2. If you encounter any difficulties downloading the file, consider using an alternative browser such as Edge or Firefox. Alternatively, if you're using Chrome and experiencing issues, you may need to force the download by following the instructions [here](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/This-file-is-dangerous-so-Chrome-has-blocked-it-message-received-when-downloading-ZIP-files-from-BIM-360-Team.html).
3. Once downloaded, extract the contents of the zip file directly into the root directory of your TAKP folder. Make sure you see `zeal.asi` in your TAKP folder and if you encounter any trouble, your first step is to make sure `zeal.asi` is still in your TAKP folder.
4. Log into the game and type /zeal version to show the version number. /help zeal will output the command list.

#### UI Files for Zeal

Zeal comes prepackaged with a uifiles folder containing files modified to display new features found within Zeal. When extracting `zeal.zip` to your TAKP folder, it will place these files in your /uifiles/duxaUI/ folder, which is the default user interface when `NewUI=TRUE` and `OldUI=FALSE` in your `eqclient.ini`. 

![ChangeButton_ZealOptions](/img/step4/ChangeButton_ZealOptions.png)

However Zeal does not come with user interface files for every Zeal feature and your game chat window will show errors when playing. These are not harmful to your gameplay experience and can be ignored. EverQuest will identify which files are missing or broken and attempt to load them from the deafault folder instead. 

![uierrors](/img/step4/uierrors.png)

If you are following this guide, you can download a replacement UI from various sources such as [qqui Calmethar](https://www.eqinterface.com/downloads/fileinfo.php?id=6959), [eqinterface.com](https://eqinterface.com/downloads/index.php?cid=115&dp=0&sh=full&so=desc&sb=lastupdate), or from [#ui-discussion](https://discord.com/channels/1133452007412334643/1162826324092657757). Just make sure to check the date and description for Zeal additions.

If you are already using a custom user interface, you can determine which UI elements are missing Zeal features and causing errors by analyzing the `UIErrors.txt file` found within the root of your TAKP folder. An easy fix is to download another UI that has everything working such as [qqui Calmethar](https://www.eqinterface.com/downloads/fileinfo.php?id=6959), and just move the files you need into the UI folder you are using. Most user interfaces can be pieced together from different sources to achieve the look and feel you prefer.

### Step 5: dgVoodoo2 

[dgVoodoo2](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) is a set of implementations of old graphics APIs for Windows 7 and later versions. If you are still having problems with intermittent game crashes, this may help.

1. Download the latest version [here](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). Open the zip file and extract only dgVoodooCpl to the root of your TAKP folder.
2. For Windows, inside the zip file, under /MS/x86/ copy all four .dll files to the root of your TAKP folder, overwriting any older files found.

    `D3D8.dll` `D3D9.dll` `D3Dlmm.dll` `DDraw.dll`

3. Run dgVoodoo.conf from within your TAKP folder.
4. Press the "./" in the upper right to select your TAKP folder.
5. Under Adapters, make sure your primary video card is selected.
6. Select "Windowed Mode".
7. Navigate to the DirectX tab.
8. Change VRAM to match your video card's VRAM.
9. Uncheck dgVooDoo watermark.

Source: [El Hefe](https://www.youtube.com/watch?v=ArLNnN0GwfQ)

### Step 6: Issues Running the Game

If you see any of these when trying to first run the game:

- windows application error
- the memory could not be read

This could be caused by WinEQ2 running in the background which is not compatible with this client. Exit the WinEQ2 application and try again.

It could also be caused when Directx 9c or a Visual C runtime is not installed. Try installing the following, rebooting and trying again:

[Visual C 2015 runtime](https://www.microsoft.com/en-us/download/details.aspx?id=53587) - download the 32bit version
[Directx 9c](https://www.microsoft.com/en-us/download/details.aspx?id=8109)
could also be that proper [AV exclusions](https://wiki.takp.info/index.php/Set_Windows_Defender_Exclusion_on_Windows_10) are not set

#### Set Compatability

Navigate to your TAKP folder and find `eqgame.exe`. Right click and select Properties. 
Under Compatibility, select "Run this program in compatibility mode for Windows XP (Service Pack 3)" and "Run this program as an administrator". 

### Xanax's Checklist for Minimal Crashes

I wrote this guide because half of my guild seems to crash when they zone in and out of the planes. Everyone is on different pieces and versions of this game. Meanwhile I've thrown most of this guide into 3 different game folders and they all work well, only crashing occasionally when I drop to character select, or if I change my audio output source. Here's what I'm using:

1. 2.1 version of TAKP was recommended back in October and I've stuck with it.
2. Secrets's experimental .dll from zeal-discussions.
3. Excluded TAKP folder from antivirus scanning.
4. Always running the latest Zeal unless it contains a specific bug I want to avoid. Always keep previous versions backed up.
5. dgVoodoo fix
6. Running program as Administrator.
7. Also running several muted sound files, EQ Basic 1.1, KaichoFX Spell Effects, and the game looks absolutely amazing!

If you ask me, the first 3 are the biggest contributors to stability. Hopefully we can lessen these crashes and work towards fixing the rest over time.

## Part 2: Installing Optional Textures and Effects
You can install various texture packs and visual effects to enhance the game's appearance.

#### Classic HD Textures
Download Link: https://wiki.project1999.com/EQ_Classic_HD#The_Al.27Kabor_Project_version:

**Note: The link contains special instructions for applying these textures to the Al'Kabor Project (TAKP).**

#### EQ Basic 1.1
Link: https://www.reddit.com/r/project1999/comments/10rz5r0/eq_basic_v11_an_eq_graphics_overhaul_project/

Download: https://drive.google.com/file/d/1PbP9Pwnjkaw4-cgN7_as8SL8PAKQlYGB/view

To install EQ Basic 1.1, follow these steps:

1. Make a copy of your EverQuest directory before overwriting any files.
2. After making a copy, extract the downloaded `.7z` file into your copied EverQuest directory.
3. Create a new shortcut pointing to your newly copied EverQuest directory.
4. Log into the game as usual and enjoy the new experience!

#### Old EQ Spell Gems/Particle Effects/Music

https://www.reddit.com/r/everquest/comments/36ovuk/howto_old_eq_uispell_gemsparticle_effectsmusic/

#### KaichoFX Spell Effects
Download Link 1: https://drive.google.com/file/d/1zXoiMFk-Z-f2Qc6tI9ZUJjfR98rVdLoK/view

Installation Instructions [here](https://www.reddit.com/r/ProjectQuarm/comments/17h98xq/comment/k6prhur/)

#### Sound File Fixes
Link: https://www.takproject.net/forums/index.php?threads%2Fwindows-10-ambient-noise-too-loud.8234%2F

This link provides edited sound files to change the volumes of certain annoying sounds like rain and wind/snow.

#### Old Skeleton Models
Download Link: https://github.com/nickgal/EqSkelePatcher/releases

To install the Old Skeleton Models, follow these steps:

1. Visit the link above and download the release for your operating system.
2. Extract the downloaded zip file.
3. Locate the `gequip5.s3d` file in your EverQuest directory (where you installed the game).
4. Drag and drop the `gequip5.s3d` file directly onto the `eq_skele_patcher.exe` file.
5. If Windows flags the executable, click "More Info", then "Run Anyway" to continue.
6. Locate the `global6_chr.s3d` file in your EverQuest directory.
7. Repeat steps 4 and 5 by dragging and dropping the `global6_chr.s3d` file onto the `eq_skele_patcher.exe` file.

After following these steps, the Old Skeleton Models will be installed and applied to the game.

Sources: [ItsKensterrr](https://www.youtube.com/watch?v=spMp-f7S7FA) | [ItsKensterrr](https://www.youtube.com/watch?v=zvhGnkbRW9g)

## Part 3: Installing Optional 3rd Party Programs

These programs add functionality not found in the game client by reading your EverQuest player log files. Programs that use hooks to inject code into the game are now allowed, with the one exception being Zeal.

#### GINA

A log monitoring application that provides audio and visual feedback based on triggers you either define or import.

https://eq.gimasoft.com/gina/Default.aspx | [Supplemental Documentation](https://kingdomdkp.com/index.php/Guides/Tools/How-to-installing-gina--basic-functions.html?)

#### EQ Nag

An EverQuest notification agent. An alternative to GINA.

https://github.com/guildantix/eq-nag/releases | [Documentation](https://guildantix.github.io/eq-nag/)

#### NParse (TAKP Fork)

Provides player location and spell tracking support for TAKP by reading the player log.

https://github.com/hitechhippie/nparse-takp

#### Quarm Tool

Log parser containing 3D Maps, Timers for everything, damage meters, and mob info.

https://github.com/EJWellman/QuarmTool

#### ZlizEQMap

ZlizEQMap is a map tool mainly designed for servers that emulate old versions of EverQuest. It features a local database of maps from the old EQAtlas website (now hosted on allakabor.com and tessmage.com), along with player positioning (x plotted on map), transparent overlay, waypoints, zone connections, and more.

https://github.com/hada79/ZlizEQMap

#### Supplemental Maps for ZlizEQMap (More Accurate)

https://www.project1999.com/forums/showthread.php?t=386944

#### EQ Tell Notifier

Desktop notifications for tells received in game

https://github.com/rtcox/EQ_tell_notifier/tree/main

#### Lossless Scaling

Lossless Scaling allows you to scale windowed games to full screen using the state-of-the-art scaling algorithms, as well as use ML based proprietary scaling and frame generation.

https://store.steampowered.com/app/993090/Lossless_Scaling/

#### Borderless Gaming

I don't use this with EQ but I need to mention it alongside Lossless Scaling. I use it with my 4k OLED monitor to remove the Windows border around games sometimes to prevent OLED burn-in. Its pricey on Steam but free on Github.

https://github.com/Codeusa/Borderless-Gaming/releases

## FAQ

- [Where can I learn more about Project Quarm?](#where-can-i-learn-more-about-project-quarm)
- [When I use my mouse wheel to scroll backwards, I do not see my character in 3rd person. How do I enable Mouse Look?](#when-i-use-my-mouse-wheel-to-scroll-backwards-i-do-not-see-my-character-in-3rd-person-how-do-i-enable-mouse-look)
- [How do I make the chat text bigger in game?](#how-do-i-make-the-chat-text-bigger-in-game)
- [Why doesn't (zeal feature) appear in my User Interface?](#why-doesnt-zeal-feature-appear-in-my-user-interface)
- [Problem with Mule Account?](#problem-with-mule-account)
- [How do I change my resolution?](#how-do-i-change-my-resolution)
- [How do I run the game full screen?](#how-do-i-run-the-game-full-screen)
- [I'm using the Stone UI from 1999?](#im-using-the-stone-ui-from-1999)
- [How do I view nameplates from far away?](#how-do-i-view-nameplates-from-far-away)
- [The game still isn't smooth. Camera movement is still jittery?](#the-game-still-isnt-smooth-camera-movement-is-still-jittery)
- [I logged in and I can only move the camera left and right or only up and down? Mouse speed is really fast too?](#i-logged-in-and-i-can-only-move-the-camera-left-and-right-or-only-up-and-down-mouse-speed-is-really-fast-too)
- [I want to turn off the loud music at character creation or character select screen?](#i-want-to-turn-off-the-loud-music-at-character-creation-or-character-select-screen)
- [Quarm enabled snow and its very loud?](#quarm-enabled-snow-and-its-very-loud)
- [I have a new laptop with an integrated graphics card and I'm experiencing graphical problems?](#i-have-a-new-laptop-with-an-integrated-graphics-card-and-im-experiencing-graphical-problems)
- [How do I disable Velious armor textures?](#how-do-i-disable-velious-armor-textures)
- [Sometimes my character's spell gems stay greyed out and the server stops responding to my client.](#sometimes-my-characters-spell-gems-stay-greyed-out-and-the-server-stops-responding-to-my-client)
- [Chat channels keep dropping?](#chat-channels-keep-dropping)
- [Why is my non-QWERTY keyboard not working correctly in game?](#why-is-my-non-qwerty-keyboard-not-working-correctly-in-game)
- [I'm having mouse issues?](#im-having-mouse-issues)
- [I'm getting a EQMAIN.DLL error running the game?](#im-getting-a-eqmaindll-error-running-the-game)
- [The text in game is fuzzy and not clear?](#the-text-in-game-is-fuzzy-and-not-clear)
- [The gamma slider doesnt work?](#the-gamma-slider-doesnt-work)
- [The EULA acceptance window moved so I cant log in?](#the-eula-acceptance-window-moved-so-i-cant-log-in)
- [I have white and yellow bars covering my text?](#i-have-white-and-yellow-bars-covering-my-text)
- [The game runs too fast?](#the-game-runs-too-fast)


### Where can I learn more about Project Quarm?
**A:** The main website projectquarm.com contains a link to the [Project Quarm Discord](https://discord.gg/3nDQ9AkUz8).

### When I use my mouse wheel to scroll backwards, I do not see my character in 3rd person. How do I enable Mouse Look?
**A:** You may have disabled mouse look. While logged into the game, press F12 to enable/disable mouse look.

### How do I make the chat text bigger in game?
**A:** /chatfontsize 1-5

### Why doesn't (zeal feature) appear in my User Interface?
**A:** Zeal adds functionality so the User Interface needs to be told how to display that functionality. Zeal contains a few UI files you can drop into the TAKP/Uifiles/ folder that you use. Alternatively, you can find new user interfaces with added functionality. I use [Nillipus UI 1440p](https://discord.com/channels/1133452007412334643/1162826324092657757/1224809011392807003)[Merchant](https://discord.com/channels/1133452007412334643/1162826324092657757/1224861589799178321) and [qqui Calmethar](https://www.eqinterface.com/downloads/fileinfo.php?id=6959) is updated frequently.

### Problem with Mule Account?
**A:** [Creating a mule](https://discord.com/channels/1133452007412334643/1135968760281432164/1208195978016854096) "The #makemule command is now available in game. Running the command in game will give you further instructions for how to flag the account as a mule and will ask that you run an additional command for confirmation.

Flagging an account as a mule can not be undone and will delevel the character running the command to 1 SO BE CERTAIN OF YOUR INTENTIONS. 

The character running the command must first be of appropriate level and no other characters can exist on the account when the command is run. Once an account is flagged as a mule then all characters on the account will be mules bound in EC tunnel and can not leave EC nor level past level 1. These accounts should not contribute to overall server population - this is so we can accurately track server population across third-party population tracking websites, such as UnixGeek's EQEmulator player stats.

The mule account will be exempt from IP restrictions allowing you to run a game client and buy/sell/transfer items independent of your main account. Again, RUNNING THE COMMAND AND CONFIRMING WILL DELEVEL YOU TO 1 AND FLAG THE ENTIRE ACCOUNT AS A MULE ACCOUNT. BE CERTAIN OF YOUR INTENTIONS. @CSR WILL NOT REVOKE THIS FLAG UNDER ANY CIRCUMSTANCES, NOR ARE THEY EQUIPPED TO DEAL WITH ANY ISSUES THAT ARISE."

### How do I change my resolution?
**A:** In your `eqclient.ini` you can find the [VideoMode] section. Change this to match your desktop's settings. 

`[VideoMode] 
Width=1920
Height=1080
(match your display settings with the proper height and width prior to launching the game)`

### How do I run the game full screen?
**A:** You want to run the game in windowed mode first. In your `eqclient.ini` set this option `WindowedMode=TRUE`. Find [VideoMode] and set it to your desired resolution. When you are logged into EverQuest, press SHIFT + Enter to switch between windowed and fullscreen modes. If you are still having problems, see the 3rd party programs section for LosslessScaling.

### I'm using the Stone UI from 1999?
**A:** In your `eqclient.ini` set NewUI=TRUE and `OldUI=False`.

### How do I view nameplates from far away?
**A:** Use an [updated](#step-3-converting-your-takp-client-to-quarm) `eqgame.dll` and make sure `eqclient.ini` has `EnableExtendedNameplateDistance=TRUE`. 

### The game still isn't smooth. Camera movement is still jittery?
**A:** First make sure you're using the experimental `eqgame.dll` file as this fixes the framerate options in your `eqclient.ini`. With previous versions of `eqgame.dll` the frame rate/refresh rate values would not be respected. 

The supported client includes a frame rate limiter not found in the original client. You can change foreground and background FPS limits (this gets put in automatically if absent) by editing these lines in your `eqclient.ini`:

`[Options]`
`MaxFPS=60 - This is the framerate you limit the foreground client window to. If this is set too high, it may consume too many system resources. Typically 60 is a good number to start with and adjust if necessary. A setting of 0 disables the limit.`

`MaxBGFPS=60 - This is the framerate you limit the background client windows to. You don't want this too low, since it will affect autofollow ability. But, if you have it too high, it may consume too many system resources. 60 is typically good. A setting of 0 disables the limit.`

`MaxMouseLookFPS=60 - Allows you to set the mouselook FPS to help with mouselook slowness. If your mouselook is too slow, try adjusting this to 60 or 45. A setting of 0 disables the limit.`

`NoFPSLimiter=0 - Enables/disables the No FPS Limiter and likes to set itself to 1. For the smoothest experience, set this to 0.`

The recommended frame rate for MaxMouseLookFPS is 60 (or 30) to avoid mouse look issues. It's 0 (unlimited FPS) by default. Very high frame rates will make mouse look less usable. However you can change these if desired. You may want a higher background FPS for better autofollowing. These features (among other fixes) are a part of the latest eqgame.dll you would have downloaded under the Obtaining the Client Section for Windows. [Source: wiki.takp](https://wiki.takp.info/index.php/Getting_Started_on_Windows)

### I logged in and I can only move the camera left and right or only up and down? Mouse speed is really fast too?
**A:** Sometimes Zeal's camera movement settings do not save properly so the camera feels too fast, or wont move at all. In game you can ALT + O to open the options menu and navigate to the Zeal tab. I like all my camera settings around .3. These settings can also be found in `eqclient.ini` at the bottom under [Zeal] `MouseSensitivityX=0.300000` `MouseSensitivityY=0.300000` `MouseSensitivityX3rd=0.300000` `MouseSensitivityY3rd=0.300000`.

### I want to turn off the loud music at character creation or character select screen?
**A:** Delete the following files from your TAKP folder. `eqtheme.mp3` `combattheme1.mp3` `combattheme2.mp3` `deaththeme.mp3`

### Quarm enabled snow and its very loud?
**A:** Originally posted on discord by Hallic|Kelendil: For those interested in reducing or deleting the new event snow sound, the name of the file for the snow/wind loop is `wind_lp1.wav` located in the `snd2.pfs` file in your EQ directory. You will need a special pfs file viewer to open, extract or delete this file. To do so, use [EQ-Zip EverQuest Archive Manager](https://github.com/Shendare/EQZip/releases). First open `snd2.pfs` and you will see a list of several environmental sounds there. You can export or delete the `wind_lp1.wav` OR even use an online .wav volume reducing tool such as [Change Volume](https://mp3cut.net/change-volume) to reduce the volume. You can then upload the reduced volume wave file back into `snd2.pfs` (overwrite and replace the loud one) and now you have a much softer sounding ambient wind. You can do this for all the sound files btw and even make custom ones.

### I have a new laptop with an integrated graphics card and I'm experiencing graphical problems?
**A:** *Hybrid Graphics Support* Some laptops containing hybrid graphics, with discrete graphics processing capabilities, often do not get utilized by the PC Client. This is due to the graphics in the older PC client being based on MS DirectX 8. A DirectX wrapper has been found that can successfully enable use of the discrete GPU, over the slower on board graphics. If you are experiencing performance issues on a relatively new laptop with an integrated GPU, give one of the following two options a try. One option is using dgVoodoo2, read more [here](https://wiki.takp.info/index.php/Getting_Started_on_Windows).

Option 1: You can download the dgVoodoo2 wrapper at [dgVoodoo2](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). This specific [Version 2.8.2](http://dege.fw.hu/temp/dgVoodoo2_81_exp4.zip) seems to work well on AMD and NVidia based hybrid graphics.

To install this wrapper, you need to open the downloaded zip file, and copy the `D3D8.dll` file found in the MS subfolder, and put this in the same folder as your `eqgame.exe`. Then just run the eqgame.exe normally. DO NOT PUT THIS FILE IN YOUR WINDOWS SYSTEM FOLDER!!! After selecting this display adapter, the game should run normally, with the exception of changing screen resolutions. If you change the display resolution in game, it WILL crash the client. So only do this in a safe location. You can optionally change the resolution by hand in the `eqgame.ini`.

In order for dgVoodoo to fire, you have to set `eqgame.exe` to use High Performance Mode in your NVidia control panel. Refer to below screenshot

![NvidiaPerformanceSetting](/img/faq/NvidiaPerformanceSetting.png)

If you have an AMD card, find an equivalent setting in the Radeon control panel.

If the wrapper is loaded, in game it will have a "dgVoodoo" watermark in the lower right corner of the display. The performance difference is usually very noticeable. But if you want to be sure, you can use software such as [GPU-Z](https://www.techpowerup.com/gpuz/), to monitor the load on the discrete graphics card. Remove the watermark by running dgVoodooCpl.exe, clicking the DirectX tab, and unchecking 'dgVoodoo Watermark.' OR you can locate the dgVoodooWatermark line in your dgVoodoo.conf file and make sure its set to false: "dgVoodooWatermark = false" If it doesn't exist, create it.

Option 2: [DXwrapper](https://www.dropbox.com/s/phvxgl6ojf2xqih/DxWrapper.zip?dl=0). This wraps the dx8 to dx9. It will use the amd graphics on a switchable graphics laptop, even though it selects the onboard graphics at run time. By using GPU-Z, you can see which graphics card is doing the work. What doesn't work, is adjusting the gamma from the slider in game. Just put these 3 files in your TAKP install folder and give it a try. If it doesn't work or you don't see performance gains, then remove them. [Source: wiki.takp](https://wiki.takp.info/index.php/Getting_Started_on_Windows)

### How do I disable Velious armor textures?
**A:** Locate the section in your `eqclient.ini` for Velious armor textures and set them to FALSE. Velious armor textures are not enabled by default as they can cause an issue with Vah Shir armor not displaying. 

`LoadVeliousArmorsWithLuclin=FALSE
LoadArmor17=FALSE
LoadArmor18=FALSE
LoadArmor19=FALSE
LoadArmor20=FALSE
LoadArmor21=FALSE
LoadArmor22=FALSE
LoadArmor23=FALSE`

### Sometimes my character's spell gems stay greyed out and the server stops responding to my client.
**A:** This is what is commonly referred to as 'desyncing'. The precise cause(s) of the problem are unknown (else they would get fixed up) but there are things that can be done to reduce the chance of this occurring.

- Ensure that your internet connection is uncongested. Try using a wired connection to your router instead of wifi.
- Make sure your firewall isn't blocking client ports.
- Make sure your frame rate is limited if running the Windows client.
- Use one of the clients linked above if you're using a different one.
- Try connecting over a VPN. Some users claim this helps.

[See also this post summarizing connection issues for TAKP](http://www.takproject.net/forums/index.php?threads/connection-issues-read-this.4488/#post-24796). [Source: wiki.takp](https://wiki.takp.info/index.php/Getting_Started_on_Windows)

### Chat channels keep dropping?
**A:** If your chat channels regularly drop, you can try adding `ChatKeepAlive=1` in the defaults section of the eqclient.ini, this will increase frequency the keepalives are sent to every 15 seconds.

If one packet is dropped that is the keepalive from Client to Server, you will time out before it triggers again, if the ChatKeepAlive=1 is not set. So this specific condition can contribute to chat channels dropping. [Source: wiki.takp](https://wiki.takp.info/index.php/Getting_Started_on_Windows)

###  Why is my non-QWERTY keyboard not working correctly in game? 
**A:** The default client is packaged with the QWERTY keyboard layout file. This can be changed by replacing the `keyboard.txt` in your TAKP folder with the one made for your locality [keyboard.txt by nationality](https://drive.google.com/open?id=0B70BIislzWn_U01KbnNXQVZ3WU0). *Please note that several are still missing and will be uploaded as we can find/make them*

### I'm having mouse issues?
**A:** Usually caused by DPI Scaling setting in Windows. Need to set it to 100% DPI scaling. You may find this forum thread useful: [Mouse issues](Usually caused by DPI Scaling setting in Windows. Need to set it to 100% DPI scaling. You may find this forum thread useful: Mouse issues)

### I'm getting a EQMAIN.DLL error running the game?
**A:** This happens if you try to launch the game from Windows Search results. Don't launch from search results. Navigate to the folder manually and run `eqgame.exe` directly, or create a desktop shortcut, or launch via hotkey.net. Also this error can happen if your anti-virus deletes some game files. Make sure you set AV exclusions and the game files aren't being quarantined.

![Eqmain-dll-error](/img/faq/Eqmain-dll-error.png)

### The text in game is fuzzy and not clear?
**A:** In each of your EQ folders:
- Right click `eqgame.exe`, properties, compatibility tab, change DPI settings, check the box "Override high DPI scaling behavior" and select "Application" in the dropdown.

### The gamma slider doesnt work?
**A:** For some people, the in-game Gamma slider does nothing. Follow the below steps on how to increase Gamma on Windows 10 machines:

- Right click on Desktop -> choose "Display Settings"
- Click on "Advanced display settings"
- Click on "Display adapter properties for Display 1"
- Click on "Color Management" tab, then click on "Color Management..." button
- Click on "Advanced" tab, then click on "Change system defaults..." button at the bottom
- Click on "Advanced" tab, then click on "Calibrate display" button at the bottom.

A "Welcome to Display Calibration" window will pop up. If you use multiple monitors you need to move this window to the monitor you wish to adjust gamma on. Click Next, Next, Next.

Now in the "Adjust gamma" screen, move the slider up a little bit until desired setting is found. You can have your EQ running next to it to find a suitable level, and click Next when done.

You can click on "Skip brightness and contrast adjustment", and click Next past the color balance screens, and untick the "Start ClearType Tuner" and click on Finish.

Now back at the Color Management - System Defaults screen, tick the "Use Windows display calibration" setting and click Close.

Now your gamma has been increased for this monitor!

*Note: If the Gamma resets on next reboot, you need to get back to the "Color Management - System Defaults" screen, and re-tick the "Use Windows display calibration" setting and click Close. This will bring back your previous settings.*

### The EULA acceptance window moved so I cant log in?
**A:** This is the first window you see when you run the game. Settings for this are in the eqw.ini file in your EQ folder. Positions are set numerically according to each resolution you use (2 for x and y would be the upper left for example):

![Eqwini](/img/faq/Eqwini.png)

### I have white and yellow bars covering my text?
**A:** This is likely caused by an incompatible version of dgvoodoo. You can either look for a newer or older version that is compatible with your graphics card or can disable dgvoodoo by moving the d3d8.dll out of the EQ client folder and relaunching the client.

This issue is fixed in v2.2 client that has an updated dgVoodoo2 d3d8.dll which is compatible with AMD cards. You can download it from [here](http://dege.fw.hu/temp/dgVoodoo2_81_exp4.zip)

![Barscoveringtext](/img/faq/Barscoveringtext.png)

### The game runs too fast?
**A:** If you are using an AMD 7xxx series CPU in your system you may need to adjust your system's settings to avoid this issue. The following were done by different people to correct this issue:

- "I disabled PBO and reduced clock speed to 3900 in bios then in Ryzen Master switched to normal profile and its working for me now. Game running at normal speed."
- "I fixed my AMD 7950x. PBO off, CPU boost off, fixed 42x 100 for 4.2Ghz set clock speed. Set the Ram to 6000 with XMP II."

Use Ryzen Master to apply settings [Source: TAKP Forums](https://www.takproject.net/forums/index.php?threads/everything-is-at-10x-speed.27284/)) 

## Suggestions Feedback and Help

#### [Project Quarm Discord #zeal-discussions](https://discord.com/channels/1133452007412334643/1210670176077348934) | [Project Quarm Discord #tech-help](https://discord.com/channels/1133452007412334643/1133453502182596729) | [Project Quarm Discord #ui-discussion](https://discord.com/channels/1133452007412334643/1162826324092657757)

Still reading? I'd like to expand this guide and keep it maintained. What I need from you are more questions to populate the FAQ at the bottom. I need to install Visual Studio and document steps to attaching the game to it to log the data that Secrets and Salty need when the game crashes or bugs out. I'd like to host a fully updated ZlizEQMap [zonedata file](https://github.com/hada79/ZlizEQMap/blob/master/ZoneData/ZoneData-The%20Al'Kabor%20Project.txt) but this one isn't updated for Quarm. I have some other ideas too. Please submit suggestions/help/feedback to me via DM on X or Discord. Feel free to ask `Xanax/Xantagonist <Former Glory>` any questions, anywhere you find me in game! 

#### @LordDemonos on [X](https://twitter.com/home)
#### lorddemonos on [Discord](https://discord.com/)
#### Special Thanks to `Zephon <Mayhem>` `Manie <Erud's Crossing Guard>` `Gamjee` `Calmethar.` `Salty`

