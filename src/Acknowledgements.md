# Acknowledgements

Writing this book, I have merely been standing on the shoulders of giants.

All the research or digging that I could do and describe in this book has been learned from a lot of talented people who made the choice to share their knowledge publicly on the internet. While I could not always quote or point to specific projects in the middle of a chapter because I felt it would break the flow of reading, or because said project was only tangentially related to the topic at hand, I wanted to devote a chapter to many of them that helped me and my understanding.

# *Actionreplay Antics*

# [Pan Docs](https://gbdev.io/pandocs/)

The [**Pan Docs**](https://gbdev.io/pandocs/) are a document, dating back to 1995, that has served as THE technical reference for the GameBoy system architecture. Originally [a single .TXT file](https://gbdev.io/pandocs/History.html), it has since evolved into a full online book, with many contributions, and is widely used by hobbyist emulator developers.

Thanks to their chapter on [Game Genie/Shark Cheats](https://gbdev.io/pandocs/Shark_Cheats.html), I had a definitive answer on the format of Game Shark cheats on the GameBoy: an **incorrect** source had separated the 4-bytes code (`01 99 47 D3`) as follows:

| Opcode | Value | Address |
|--------|-------|---------|
| `01`   | `99`  | `47 D3` |

The misconception most likely stems from ActionReplay/GameShark for other consoles actually using opcodes, with `01` often being the simplest instruction: "write data to address".

# [Shonumi](https://shonumi.github.io/index.html)

While the **Pan Docs** are the reference documentation for the GameBoy system, it lacks in documentation on the non-official peripherals, making perservation of games using some of these hardware very difficult. Shonumi, the developer for the [GBE+](https://github.com/shonumi/gbe-plus) GameBoy emulator started writing the [**Dan Docs**](https://shonumi.github.io/dandocs.html) to study them.

That research is documented on Shonumi's blog, in the "Edge of Emulation" series, where obscure GameBoy peripherals are reverse-engineered to properly document and emulate them.

# [ares](https://ares-emu.net/)

Originally started by developer [near](https://www.reddit.com/r/emulation/comments/vm2avf/remembering_near_developer_of_higan_ares_who/), **ares** is a multi-system game emulator.

Just as the above **Pan Docs** are the reference for the GameBoy architecture, near has been instrumental in the documentation and preservation of his favourite machine, the Super Famicom (aka Super Nintendo). Frustrated with the shortcuts used by emulators of the time (famously, ZSNES, and Snes9x to a lesser degree) to achieve greater compatibility, to the detriment of accuracy, [near](https://en.wikipedia.org/wiki/Near_(programmer)) began **bsnes**, an emulator meant to accurately replicate all hardware parts of the console.

While their work was initially contested because it required high-end computers to emulate a "simple" system, the benefits it brought to game hacking (many old fan translations having only been tested on non-accurate emulators, they wouldn't work properly on real hardware), combined with the evolution of consumer computers performances, made their emulation approach *de facto* nowadays.

# [Pokémon Red decompilation project](https://github.com/pret/pokered)

Started by [iimarckus in 2010](https://github.com/pret/pokered/commit/df2b3b739c9cf8a5d63d6f8f342e63bc67525ebc), this project has since taken a life on its own, and is your best source to understand any question you may have on how the original Pokémon worked.

For instance, did you know that the reason there are 8 badges in the game is because [they were easier to store in the player inventory as 8 bits](https://github.com/pret/pokered/blob/1f6e2bf999401b9444f939bb40c1eb279bc51829/constants/ram_constants.asm#L27)?
