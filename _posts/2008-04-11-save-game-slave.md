---
layout: post
title: Save Game Slave
date: '2008-04-11 17:14:04 -0700'
categories: game-design
---
Saving games is really important. Being able to save and continue not only allows you to fit gameplay into your own personal schedule, it also allows game developers to create experiences that span more than one game session. Saving may be one of the core technologies of video gaming, but the ways we save haven't changed drastically in the last decade. I'm sure there has been at least one time in your life where you felt like a victim, your hard work or hopes plundered by a game's save system. Maybe you ran out of save slots to use, or you overwrote a save with 40 hours of progress, or you can't copy your save game data to another memory card. If this sounds like you, then read on. In this article I will explain your plight to the masses and then propose the next generation of save game systems.

There are two main types of save file systems. The first one gives players a certain number of personal save slots per game (three or four is common). This certainly benefits cartridge-based games where onboard storage is needed per cartridge to hold this save data. The other save file system, selectable save slots, has its roots in PC gaming and spread to consoles only recently thanks to memory cards and hard drives. This system allows the player to pick from an almost infinite number of slots whenever they want to save the game. Let's analyze the benefits and disadvantages of each system from the perspective of the game developer and the player. I will ignore the technical limitations I've already mentioned.

## Personal Save Slot Systems

Personal save slots have one great advantage. Your mom (or other significant non-gamer) can understand them. This system is like a post office box. You have access to your post office box. It sits next to some other post office boxes, but you have no way of interfering with those boxes and they have no way of interfering with yours. Mom can have her very own Zelda slot, while you and your friends are sharing another one. There's no chance of crossing over or accidentally interfering with the other player. This ease of use inherently translates to the user interface. When you start playing you select your save slot, and from then on all in-game save commands go to that slot, no questions asked.

Where's the downside? For one, games never seem to give enough of these. As I mentioned earlier, three to four is the industry standard. Some portable games have a frustratingly small amount, like two. That was fine a few years back when gaming was a personal experience. As gaming becomes more social, however, an increasing number of people are playing on a single console or with a single cart. College locations such as dorm rooms, greek houses, and campus recreation areas are all good examples. As the most hardcore gamer among my friends, I typically need to keep one of these personal save slots open at all times for when people want to try a game out. The Legend of Zelda: Phantom Hourglass has two save slots. What do I do when I have a save slot on Phantom Hourglass, my girlfriend is using the second slot, and my roommate wants something to do while he's waiting at the doctor's office?

Personal save slots create an extra burden on the game developer. Since the player isn't allowed to branch their save games into multiple slots, game must be designed to let the player revisit any pieces of the game that they missed. This is sometimes accomplished with good constraints like "Don't destroy any locations for story reasons". But when you can't have constraints like that, you must instead spend extra time implementing features like auction houses that let players get their hands on items they missed.

## Selectable Save Slot Systems

Now let's talk about selectable save slot systems. The most visible advantage is that you've got enough save room for you and everyone you know. Unlike personal save slots where the UI is simple and bothers the player only once at the beginning, selectable save slot user interfaces can easily become a hindrance by either frustrating the player or breaking their immersion. For this reason, your UI will make or break saving in your game. Having annoying warning prompts that users must constantly acknowledge yet preventing them from accidental overwriting is a difficult thing to balance. You might want to try tagging save files with a number generated at the start of a new game (or a name), and provide extra warning if the player tries to save over a slot where this identifier does not match.

Another useful UI feature is to automatically highlight the slot the player loaded from. If you were to always start the save slot selection list at slot #1 regardless of what slot they loaded from, then slot #1 would become a dangerous save place. Anyone who hammers the save button may overwrite your work. A downside to not implementing this is that cautious players end up "double saving" their work at significant checkpoints. That is, they choose a far away and inconvenient save slot like one a few pages away or at the end of the list, and save there as well. This is a waste of space.

The second big advantage is that players who understand selectable save slot systems can use and abuse them in powerful ways. Saving in a new slot before major boss battles allows you to replay the cool bosses whenever you want without having to play through the game again. If the player is required to make a choice, they might save before making the decision so that they can "taste" each decision and choose the one they like best. On the Xbox 360, careful saving can let you go back and take another shot at unlocking an achievement you missed.

(As a side note, achievements are just meta rewards so why do game designers go out of their way to help you acquire in-game rewards you missed but not achievements? It's not okay to crumble a castle on top of a chest with a rare sword in it, making the chest unreachable. But it is okay to deny an achievement because the player failed to complete a mini-game they get only one shot at without taking any damage? This is the same basic mistake.)

This power ends up also being a disadvantage. First, the system is not intuitive. How does mom understand it? Second, if at any point players are required to rely on their ability to manipulate save slots to fully experience your game, you've failed them as a designer. If cool boss battles are a feature of your game, you should think about implementing a special mode that lets players replay bosses. If they must make a decision between good and evil you should properly educate them with information, or better yet (since gamers hate to read) let them try out both sides as part of the storyline and THEN choose.

The final disadvantage to selectable save slot systems is there is no universally understood organizational structure to the slots. Most games simply provide a sequentially numbered list of save slots starting at #1. How do you decide which numbers go to which players? Who will remember that information after not playing the game during a two week business trip?

## The Ultimate Save System

I will end my analysis by building a save slot system that attempts to integrate the best of both personal and selectable systems. The first important step happens during the start of a new game. A personal save system with personal slots is mimicked as closely as possible, with one important difference. Instead of the name of the slot being tied to the in-game character, it is instead tied to the person who owns the save slot. This is important because if you have two purists who insist on naming the characters their official names, the slots lose individuality and players are back to remembering that slot #1 belongs to one person and slot #2 to another. Most people prefer Link to be called Link, unless they take a not-so-serious approach to Zelda games and name him something like TheCooch. In a twisted sort of way, the Xbox 360 already works like this. Super Mario Galaxy also supports this by letting players attach their Mii heads to a save slot.

Whenever a save point is reached in the game, there are still no surprises. The game is saved into the personal slot, on top of the old data. Here is where things get interesting. Players can pause a game and from a menu tell the game to create a **snapshot**. Snapshots are copies of their most recent save that can be reloaded at any time; but not used to save the game. So if you're playing a game and you think a particular cutscene or enemy encounter or mini-game is particularly interesting, you can pause the game and take a snapshot. You'll be able to play that snapshot whenever you want and be very close to the interesting part of the game. This is all totally optional, so mom doesn't have to know about this feature if it's going to confuse her.

Anyone who's played Half-Life 2 knows that an intelligent auto-save system can really help the player out. With snapshotting, an auto-snapshot system can be triggered whenever the game developer thinks the player just experienced a memorable game moment. After beating a boss, for instance, take an auto-snapshot of the last save. Now the player can replay that boss whenever they want. For Xbox 360 games, auto-snapshots taken before achievements that players only get one shot at would be greatly appreciated. Another good use would be during a high adrenaline part of the story, like a chase scene.

This system intentionally prevents the player from being able to branch their saves and take another stab at the game. It does this by disabling the save feature when the player loads a snapshot. Forcing the player to juggle their saves to experience 100% of your game content is bad design.

The best part of this hybrid system is that it can be centralized on the platform so that all games can utilize it without needing to write custom code to implement it. Players could even share snapshots with each other. Imagine sending a snapshot to your friend over Xbox Live with the message: "I got to Dracula before leveling my character's whip! Try and beat him!"

Hopefully we'll see features like this on the next generation consoles, like the Wii-er, Xbox 720, and PlayStation 4.