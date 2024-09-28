# ColdSteel Cheating

1. Advance by a few seconds...
USER019: Base
USER020: Wait a few seconds

The difference is SMALL, which is good. Only five bytes, which is weird.

The test was to find the value which would be used for the time counter, or worse: a checksum. In any case, we have no idea yet, but we know of a field that will ALWAYS be modified, so we can ignore it safely in future diffs.

Lessons:
- Fields are static in offset.
- We know where time/checksum is.


2. Fill a character profile
USER020: Base
USER021: Talk to Casper to fill his character profile

The difference this time is huge. I was expecting a single byte to change, but I forgot another part: conversation archive.

Lessons:
- None

3. Feed Celine in the Library
USER022: Base
USER023: Feed Celine

I would like to find a single trigger check. I am not sure I did. However, I did find how items are stored.

For a reason I don't get, items are padded to a size of 36 bytes.

Lessons:
- Found items.
- Since this save was on a second playthrough, I found a counter of NG+.


4. Can I find difficulty?
USER024: Easy
USER025: Normal
USER026: Hard
USER027: Nightmare

I cannot parse the playtime and it's infuriating me. Therefore, I decided to go and look for the difficulty, since I was pretty sure it could be around the same place, and affecting the. Good news: I found it. Bad news: it's not where I was expecting it.

Lessons:
- Found difficulty
- It's not stored with the playtime.

5. Move to RPCS3
Using my own physical PS3 to test for these things is a pain, so I'm moving my "editing table" to rpcs3.Fiddling around to confirm that the saves worked, and trying to restore some JP-only DLCs, I managed to find something interesting: a table of ALL items, that actually matches the one I got.
https://fearlessrevolution.com/viewtopic.php?t=4467&start=285

Lessons:
- All items.
