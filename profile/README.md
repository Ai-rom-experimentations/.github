# AI ROM Experimentations

**AI-assisted ROM hacks, ports, and experiments for old hardware.**

AI ROM Experimentations is a collection of experiments where I use the **Arena agent** to make ROM hacks, ports, and other projects for retro hardware.

I don't write the code myself.

The AI does the actual development: analyzing the source material, figuring out how the original game works, modifying the code, adapting it to different hardware, building the project, and iterating when something breaks.

My role is basically to decide what to try, give the AI direction, test the results, and see how far we can take it.

## What we're making

The projects can be pretty much anything involving older games and hardware:

- ROM hacks
- NES game ports
- NES → SG-1000 experiments
- SG-1000 → other Sega 8-bit hardware experiments
- Master System projects
- Other 1980s Sega systems
- Amiga ports and experiments
- Gameplay modifications
- Graphics and sound experiments
- Hardware-specific experiments
- Weird ideas that probably shouldn't work

If an old game can be disassembled and understood well enough, it's potentially fair game.

## How the projects work

Most projects are built from a **disassembly of the original game**.

The general process looks something like:

    Original game
         │
         ▼
     Disassembly
         │
         ▼
     Arena agent
         │
         ├── Understand original code
         ├── Modify game logic
         ├── Port code to another platform
         ├── Adapt graphics / sound / hardware
         ├── Build ROM
         └── Fix whatever broke
         │
         ▼
    Working experiment

For projects where the disassembly doesn't contain everything needed, the original ROM may also be included or referenced as a source for things such as **graphics, level data, sound data, or other assets**.

The exact setup depends on the game.

## The AI does the coding

This is probably the most important thing to know about the organization:

**I don't write the code.**

The Arena agent handles the actual programming.

That includes things like:

- Assembly
- Game logic
- Platform-specific code
- Graphics conversion
- Memory management
- Hardware interfaces
- Build systems
- Debugging
- Porting
- ROM generation
- Fixing bugs

I mostly provide the goal and direction.

For example:

> “Take this NES game and see if we can get it running on the SG-1000.”

Then the AI gets to figure out how.

Sometimes that works.

Sometimes it doesn't.

Sometimes it produces something that is technically running but absolutely should not be considered finished.

That's part of the experiment.

## Target platforms

### Sega

- SG-1000
- Master System
- Other compatible 8-bit Sega hardware
- Other Sega platforms when interesting

### Nintendo

- NES
- Other Nintendo platforms when practical

### Commodore

- Amiga
- Other compatible systems when an experiment makes sense

The platform list isn't fixed.

If there's a sufficiently interesting technical challenge, we'll probably try it.

## The point

This isn't meant to be a traditional ROM-hacking organization where every project requires me to manually write thousands of lines of assembly.

Instead, it's an experiment in **AI-driven retro development**.

The question isn't just:

> “Can this game be ported?”

It's also:

> **“How much of the process can an AI agent actually handle?”**

And then we test it.

## Repository structure

Most repositories are based around a disassembly of the original game.

A typical project might look roughly like:

    project/
    ├── src/             # Disassembled / modified source
    ├── assets/          # Graphics and other required assets
    ├── tools/           # Conversion/build tools
    ├── build/           # Build output
    ├── patches/         # Optional patches
    └── README.md

The structure can vary depending on the original disassembly and the target platform.

## ROMs and original game data

Where legally appropriate, a project's repository may contain or reference the original ROM when it is needed for development, particularly when the disassembly doesn't contain assets required for the experiment.

ROM data may be used to obtain things such as:

- Graphics
- Tiles
- Sprites
- Maps
- Sound data
- Level data
- Other game resources

Redistribution of copyrighted game ROMs is avoided where necessary. Projects should document what users need to provide themselves.

## Retro, but not *that* kind of retro

The projects are about old hardware, but there's no need to pretend they're mysterious artifacts from 1987.

No fake “lost cartridge” lore.

No unnecessary CRT filters.

No “WELCOME TO THE WORLD OF 8-BIT!!!” nonsense.

Just old games, old hardware, modern AI, and whatever happens when you put them together.

## Status

Projects can be anything from a completely broken proof of concept to a fully playable port.

    idea
     ↓
    experiment
     ↓
    prototype
     ↓
    working
     ↓
    playable
     ↓
    released

And sometimes:

    experiment
     ↓
    why does this even boot
     ↓
    abandoned

That's fine too.

## In short

**I provide the idea.**

**Arena does the coding.**

**The disassembly provides the foundation.**

**The old hardware provides the limitations.**

**And the resulting ROM tells us whether it actually worked.**
