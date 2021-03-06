Browser-based Item Tracker for A Link to the Past
v 5.1.0-rc
by crossproduct (twitch.tv/crossproduct)
and halfarebel (twitch.tv/halfarebel)

                                ^
                                |
       /\    ���||��� |   |�- |�|�|    /\
      /__\     / |__  |   |  \|_|_|   /__\
     /\  /\   /  |    |   |  /| | |  /\  /\
    /__\/__\ |__ |___ |___|_- | | | /__\/__\
                                ^
                                ^

------------------------------------------
(:::[========> INTRODUCTION <========]:::)
------------------------------------------

This tracker is designed for use with A Link to the Past randomizer streams.
It's browser-based, so it should work on most platforms!
Just open the tracker in your browser and do a Window Capture in OBS!

Feel free to open the HTML files in a text editor if you want to change the
image sizes or the background color. Soon, I'd like to have a config.exe to
adjust such things.

In the future, I'd like to figure out how make the window borderless, and
possibly keep sheets saved on a server to be capture with CLR Browser. I may
also implement a way to customize your layout.

Start playing ALttP Randomizer today!

Web Version should always have the latest features:
http://vt.alttp.run/


--------------------------------------------------
(:::[========> TRACKER INSTRUCTIONS <========]:::)
--------------------------------------------------

- Open the launcher, index.html.
- Click the button corresponding to the desired Mode and Mapfulness (Popup
  blocker no longer an issue).
- Opening the tracker, tracker.html, without url query parameters, will not
  work. It will only show a black page.
- The launcher and tracker is only tested for Chrome.

-[--- Item Tracker ---]-

- The first box is the Item Tracker. It shows you which items you have.
  Click to toggle!
- The chests represent the "unique" chests of each dungeon.
- Click the corresponding chest icon if you're in a dungeon and open a chest
  that IS NOT a Map, Compass, Key, or Big Key.
- The square with Link contains info for Tunic, Sword, AND Shield.
- Boss squares have sub-squares to remind you which prize a boss will give you:
  Click to toggle from Unknown, Green pendant, Red/Blue, Crystal, and Crystal 5/6
- Vitreous and Trinexx have medallion subsquares, as well!
	- The Location Tracker WILL consider these icons when it determines
	  availability for Misery Mire, Turtle Rock, AND Mimic Cave
- Click on the bosses and chests to "check off" locations for the dungeons.
  CLICKING THE MAP WILL NOT UPDATE DUNGEON LOCATIONS!
- Things that have multiple steps (items such as sword, gloves, as well as chests,
  prizes, medallions) can be cycled the other direction with right clicks.

-[--- Location Tracker ---]-

The second box is a map of the Light World, the third box is a map of the Dark World.
Mousing over a location square will give you a little bit of information.

- Small squares are chests and Heart Piece locations strewn about the land of Hyrule!
	- Green areas are attainable with your current items (the logic assumes you
	  have access to bombs).
	- Red areas are unreachable.
	- Yellow areas are unreachable, but you can see what item is there!
		- Exceptions for Mimic Cave and Escape Sewer Side Room are noted
		  in the captions.
	- Blue areas are attainable, but will require dark room navigation.
	- Gray areas have already been searched. (The chests between Link's house
	  and Sanctuary start off as Gray by default in Standard Mode.)
	- Click a Red/Green/Yellow/Blue square to check it off and turn it Gray.
	- You may want to click a Red/Yellow square if you get it via minor
	  glitches, or see the item and decide you do not want it.
	- Click a Gray square to revert it to Red/Green/Yellow/Blue
	  (the tracker will recalculate whether it's reachable)

	*PRO TIP!!! The "Agahnim" icon is very important in the tracker's logic!
		Remember that you can kill Agahnim as long as you have Cape+Sword or
		L2 Sword (watch out for dark room)! Will killing him open up new item
		locations? Click on him to see!

- Large squares are dungeons!
	- The inner square represents the Pendant/Crystal.
	  Do you have the right items to beat the dungeon master?
	- The outer square represents the unique chests inside.
	  The logic for dungeon chests takes into account how many chests are
	  remaining for that particular place.
	  For example: If you can reach Thieve's Town, then you are guaranteed
	  at least 3 unique items. If there is only 1 chest left, it may be
	  inaccessible without Hammer.
	- Red/Green/Gray squares follow the same convention as overworld locations.
	- If an outer square is Green, you are guaranteed AT LEAST ONE unique chest,
	  not all of them.
	- Yellow squares may or may not be accessible, based on where keys are
	  (and unknown medallion requirements)
	NOTE: The Ice Palace crystal is always reachable as long as you can get in
	  (and have Fire Rod or Bombos). If the Ice Palace crystal is yellow,
	  YOU MUST BOMB JUMP TO COMPLETE THE DUNGEON!
	- Clicking the dungeon squares on the map HAS NO EFFECT!
	- Clicking the corresponding chests on the Item Tracker will
	  toggle the outer square.
	- Clicking the corresponding boss picture on the Item Tracker will
	  toggle the inner square.

-[--- Keysanity ---]-

Currently the keysanity mode of the tracker correspond to open mode with the
keysanity variation. Each of the 10 crystal/pendant Dungeons have associated
dungeon maps that can be shown by clicking their overworld squares, and
dismissed by clicking the close button in the top left of the dungeon map.

- Item tracker
	- Instead of a square with a group of chests they will share space with
	  aquired vs total number of small keys. Click the small key to increase the
	  number of aquired keys for that dungeon.
	- Since keys, map, compass are not confined to their dungeon, all dungeon
	  locations are tracked, resulting in higher chest counts which are shown by
	  a number over a single chest.
	- Clicking the chests will make the chest count mismatch with marked the
	  locations on the dungeon map and will cause the dungeon to show in yellow
	  until the counts match again. Clicking the boss still marks the location
	  on the dungeon map since they correspond directly to each other.
	- The big key for a dungeon is tracked on the boss square.
	- Agahnim share space with two small key counts, with the upper representing
	  Castle Tower keys, and the lower the Hyrule Castle key.
	- Ganon's Tower item locations, small and big key are represented to the right
	  of Link's sprite.

- Location tracker
	- The dungeon maps show the item locations in a similar way as the overworld
	  item locations, but with bigger squares and an image for the big chest
	  and boss.
	- Desert Palace, Palace of Darkness, and Turtle Rock also show doors which
	  aid in showing correct logic.
	- The launcher provides two extra options for keysanity that can be toggled
	  off if the player can not perform bomb jumps in Ice Palace, and the Palace
	  of Darkness Hammeryump, respectively. Without Ice Palace bomb jumps some
	  locations can show as yellow if they might possibly require a bomb jump to
	  reach.
	- There is also two additional overworld locations that represent the two
	  chests on the way up Castle Tower since they can contain unique items in
	  keysanity.


--------------------------------------------
(:::[========> FUTURE CHANGES <========]:::)
--------------------------------------------

From highest priority:
- Right Click to toggle items/dungeon prizes backwards
- Scaling: x2 or x3 instead of the normal x4
- Modes and settings
	- Select mode and variations independently
	- Inverted Mode
	- Swordless
- Sequence Breaks (orange?)
- Colorblind support
- Go Mode indicator


------------------------------------------
(:::[========> DISTRIBUTION <========]:::)
------------------------------------------

Feel free to share this tracker by posting a link to my Twitch channel:
	twitch.tv/crossproduct

(Sharing the GitHub link doesn't help me as much.)
DO NOT DISTRIBUTE THIS TRACKER ON YOUR WEBSITE!
DIRECT PEOPLE TO MY TWITCH CHANNEL FOR DOWNLOAD!

If you would like to make modifications to the tracker and share it on your site,
follow these guidelines:
- Ask permission. Let me know how and why you are altering and redistributing.
- Direct Message me via Twitch or Discord (see contact info above)
- The changes must be significant!
- GOOD CHANGES: layout customizability, non-browser platform, new features, etc
- BAD CHANGES: minor logic fixes, icon customization
- You must credit me and provide a link to my Twitch channel.


----------------------------------------
(:::[========> CONTACT ME <========]:::)
----------------------------------------

Any questions or comments about the tracker?
Have any requests for new features or icon skins?
Is there a bug or a mistake in the chest availability logic?

These are the fastest ways to reach me...

TWITCH CHANNEL:
	twitch.tv/crossproduct

ALTTP DISCORD SERVER:
	https://discordapp.com/invite/3Bsfnwk


--------------------------------------------
(:::[========> SPECIAL THANKS <========]:::)
--------------------------------------------

-[--- Randomizer Developers ---]-

	Karkat (mmxbass)
	Dessyreqt
	Veetorp

-[--- Support ---]-

	jet082
	WildAnaconda69
	Alucard2004
	uphier
