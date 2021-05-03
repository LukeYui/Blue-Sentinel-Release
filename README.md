## **About**

Blue Sentinel is an anti-cheat tool for Dark Souls III, it will protect you from malicious cheats, flag players who use them, and allow you to kick them from your world.

If you're enjoying this mod, and want to support me, you can buy me a coffee here: https://ko-fi.com/lukeyui

## **What does it do?**

This tool aims to identify cheaters and mitigate the impact they have on your online play, through a few different methods:

Detecting stat and level abnormalities of people in your session, allowing you to remove the player with cheated stats or disconnect.
Preventing dangerous effects (such as curse) being applied to you by other players.
Preventing a wide range of exploits, including multiple crashes.
Blocking invalid items from being picked up, or being given directly to you. (a.k.a "Item Inject")
Preventing a wide range of bullet-related frame rate drops.
If enabled, it can autokick detected cheaters when hosting.
If enabled, it can backup saves every time a new session is established and store a set amount of backups before deleting the oldest*.
It will flag alternate accounts of people you have blocked

*Backups can be found in %appdata%\DarkSoulsIII\(YourSteamID64) and are named "(timestamp)_DS30000.sl2.bak"

In addition to this, if you use the overlay, it will display the other players in the session, along with their steam profile names.

For more details on what Blue Sentinel does in the background, see below, note that this is not an exhaustive list and BS has hundreds of patches across multiple different categories: 

Invalid items cannot be dropped to you, or given directly to you.
Fixed 2 crashes associated with equipment packets
Fixed 5 crashes related to player coordinate packets
Fixed 3 crashes, and 6 exploits associated with item packets
Fixed a crash, and an exploit involving a type of world flag packet
Fixed a memory allocation error with player initialisation packets
Fixed 2 crashes, and an exploit, involving player structure packets; Also prevents players changing their SteamID
Fixed 2 buffer overrun crashes relating to world initialisation packets
Players cannot apply custom effects on-hit such as curse
Fixed a out of bounds crash involving WorldChrSync initiation packets
Fixed 4 crashes related to player animation packets
Fixed 2 crashes related to enemy load synchronisation packets
Fixed 2 crashes relating to player bullet initialisation packets
Fixed 2 crashes relating to NPC behavior packets
Fixed an exploit that allowed players to apply effects to you (a.k.a "Autopilot")
Fixed a crash related to irregularly sized packets
Fixed 4 crashes, and 6 exploits relating to "MsgMapList" events. (e.g. "Force Animations")
Removed old netcode which allowed malicious users to modify other's soul count
Removed old netcode which allowed malicious users to modify the "humanity" other players
Fixed over 10 exploits and crashes involving the 'NetPackingVector'
Multiple packet validation checks, trying to fix both common and more 'unique' cheats.

Why should I use a protection tool in (current year)?

The cheating scene in Dark Souls has moved on from simple annoyances like cursing and one-shots to more malicious intent (such as crashing, banning, ruining saves etc)

Unfortunately, the item give cheat (aka Item Inject) was just the tip of the iceberg in this sense. Dark Souls III has some serious network vulnerabilities that can get your account banned or even cause lasting  damage to your PC. I have reported all of these to the publisher and developers however it doesn't look like they will ever be addressed, it's only a matter of time before these security issues become popularised / public and Blue Sentinel offers a very high level of protection against these exploits.

I would recommend that every player who wants to play online uses a protection tool, and Blue Sentinel offers the greatest coverage against both well-known and obscure exploits.

## **Flags**

If you have the overlay enabled, Blue Sentinel will flag users in your session. There are 9 different flags a player can get:

[Blocked] - The player connecting has been blocked via Steam*
[Blocked Alt] - The player is family sharing the game from an account that you have blocked**
[Malicious] - A check in Blue Sentinel has detected irregular data being sent from the player
[Cheating] - Blue Sentinel has detected that the player has a greatly unfair advantage - Reserved for non-downscaled phantoms
[Borderline] - A check in Blue Sentinel has detected irregular data being sent from the player, but it is indistinguishable from extremely high latency
[Invalid Stats] - The player has modified stats that are inconsistent with their soul level
[Impossible Stats] - The player has modified stats that are impossible to achieve through normal means, but have a normal soul level
[Kicked] - The player has been kicked through Blue Sentinel
[Glitching] - The player is abusing exploits (or using "glitches") such as infinite stamina with the Ring of Favour glitch, or avoiding the estus recovery animation to gain a frame advantage

*Dark Souls III will usually kick the player, however it takes 5 minutes between blocking the player and updating in the game.
**Within the ini file, there is an option which allows you to treat blocked alts as normal blocked players, refusing the connection when they join.

Important note - Flags do not necessarily imply malicious intent from the player. For example there is a bug in a commonly used anti-cheat tool which will flag up in Blue Sentinel because it looks identical to a harmful action, if someone gets flagged and doesn't otherwise seem to be cheating, it's worthwhile to reach out to them and ask them about it. Blue Sentinel shouldn't be used as an all-tell for who is and isn't cheating, and please do not witch hunt players who are flagged.

## **Glitches**

Blue sentinel tries to pick up players abusing some glitches and exploits in PvP. I've erred more on the side of caution here, so Blue Sentinel will not flag a glitch if it's not absolutely sure whether the player is glitching or not to avoid false flags. Please note that glitch detection is *disabled by default* within the ini file.

Not all glitches are detected, only the ones that seem more damaging to the online play. This is a balance between: How easy are they to perform; How popular are they amongst the community; What are their impacts on normal PvP? So far, Blue Sentinel should be able to accurately detect:
Estus cancel
Some variances of the "bow glitch"
Illegal sacred flame grabs
Weapon art swap with "Parting Flame"
Weapon art swap with "Repeat Fire"
Infinite stamina with ring of favour rapid equipping/unequipping

When a player performs one of these glitches, they will get the [Glitching] flag. To avoid abuse (e.g. someone only kicking for 1 glitch detected a while ago because they are losing) this flag will expire after 10 - 15 seconds, but will be reapplied if the player continues to abuse glitches. If you use certain glitches yourself whilst using Blue Sentinel, it will turn the detection for other players off.

People have expressed concern about the glitch detection, however this is an optional flag and only accounts for <0.5% of Blue Sentinel's actual function.

Note: If you have glitch detection enabled, and a friendly phantom glitches themselves, glitch detection will be disabled for you for the duration of the session. If you use glitches yourself, the detection will be disabled until restart.

## **Can this soft-ban me?**

This tool cannot give a soft-ban by itself. To be clear:

Blue Sentinel does **not** modify Dark Souls III's code in any way*
Blue Sentinel does **not** disable Dark Souls III's anticheat

*The "SkipLogos" setting in the ini file does do this, but it is a safe edit, and will not cause a softban.

## **How do I use it?**

You should use Blue Sentinel as a stand-alone protection tool - Uninstall any other online protection mods (e.g. watchdog) you may have first.

Download the mod from the Download page
Extract the package you downloaded, and move the following files to your Dark Souls III folder (usually in "C:\Program Files (x86)\Steam\steamapps\common\DARK SOULS III\Game"), it should contain:
xinput1_3.dll - The mod itself
BlueSentinelPref.ini - An INI file where you can change some mod settings - Edit this to your liking

To uninstall the mod, you just have to remove these files, or if you just want a temporary uninstall, rename "xinput1_3.dll" to something like "BlueSentinel.dll", then change it back when you want to use it again.

When the mod runs for the first time, it will create a directory called "Blue Sentinel" in your Dark Souls III folder where logs will be stored.

## **FAQ:**

Q) Does Blue Sentinel check/log IPs?
A) No, unlike other anti-cheat tools Blue Sentinel does not grab or use your or anyone else's or IP addresses.

Q) Why are you flagging glitches?
A) This is a pretty divisive topic - In my view glitches such as "estus cancelling", ring of favour spam, and infinite stun locks have become so widespread and abused that they have become normalised in PvP. Some people argue that they are harmless and part of the game's normal behaviour so shouldn't be viewed as cheating, but I think we can all agree that the developers never intended this behaviour, and if they were still maintaining the game then these things would be patched. I could go on for hours about why I chose to flag some glitches over others, but there's plenty of arguments already out there.

Q) I've found a bug with the current release, can I report this?
A) Please do, I'll try to get round to fixing it as fast as possible.

Q) I know of / have been effected by a cheat that wasn't detected by this mod, can I report this?
A) Absolutely, please don't expect any cheats that aren't sent over the network to begin with to be detected though

Q) Won't this tool be beneficial for cheaters, or give an advantage in PvP?
A) No. Some people feel like seeing the player list gives an advantage, however there are options to turn it off in the ini file.

Q) Can we see the source code?
A) No, while I understand people can be distrustful of mods like this, I'm unwilling to make the source code public. Past experience has told me that certain groups are more interested in either crashing or exploiting protection tools than contributing to them, so I'd much rather not.

Q) Is this a virus?
A) No, the mod is limited to Dark Souls III (when it is running) and does nothing outside of the process. It's function is to check incoming data from other players who are connected to you to make sure it's regular. If you are distrustful of this mod, there is a complete VirusTotal scan report (accessed by clicking the green "tick" next to the file in the 'Files' tab of the mod page. There may be a few flags, however rest assured this is just the code protection within the mod causing a false positive.

Q) Can I modify or redistribute this mod?
A) No, sorry. Watchdog allowed this because we hoped the community could add to it in some way, but unfortunately a few just abused it's kick function to apply for any players, even without flags. Please do not modify, repackage, or redistribute this mod anywhere without my permission.

Q) I have a question not answered here.
A) If you need more information, or wish to report a bug, have a suggestion etc. please make a post about it, or send me a direct message.

## **Notes**

A huge thanks to all of the beta testers of this mod, it would not be possible to have made this without them:
inuNorii, Dalvik, sfix, Gáté, Specter, Roxanne (Busty Patches), AntonioCS, Purpurea, Rayan, iamamish
