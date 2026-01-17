# Anacreon 2.0 (DOS) - Source Code Analysis

## Overview
This repository contains the source code for the 2004 "resurrected" version 2.0 of **Anacreon: Reconstruction 4021**, a classic 4X space strategy game originally developed by George Moromisato in the late 1980s. This specific version was maintained and expanded by **Adam Luker** between 2003 and 2004, introducing significant features and bug fixes to the legendary DOS title.

## Project Details
- **Original Developer**: George Moromisato
- **Version Maintainer**: Adam Luker
- **Year**: 2004 (v2.0 release)
- **Platform**: MS-DOS
- **Programming Language**: Turbo Pascal, x86 Assembly

## Technology Stack
- **Primary Language**: Turbo Pascal (`.PAS` files).
- **Assembly**: x86 Assembly (`FASTSCR.ASM`) used for low-level screen drawing optimizations to bypass slow BIOS calls.
- **Overlay System**: Uses Pascal overlays (`ANACREON.OVR`) to manage memory on 16-bit DOS systems with limited conventional memory (640KB limit).

## Repository Structure & Modules
- **ANACREON.PAS**: The main application entry point and orchestration logic.
- **GALAXY.PAS** / **MAPWIND.PAS**: Core logic for the procedural galaxy generation and the strategic map display.
- **FLEET.PAS** / **FLTCOMM.PAS**: Management of space fleets, movement, and combat commands.
- **NPE.PAS** & **NPE00.PAS - NPE04.PAS**: Logic for "Non-Player Empires" (AI), handling their strategic decision-making and expansion.
- **ATTACK.PAS** / **BATTLE.PAS**: Combat resolution logic for planetary invasions and fleet engagements.
- **FASTSCR.PAS/ASM**: High-performance "Fast Screen" library for high-speed text and UI rendering.
- **NEWGAME.PAS**: Logic for initializing new scenarios and galaxy parameters.
- **DATACNST.PAS** / **DATASTRC.PAS**: Central definitions for the game's complex data models (planets, fleets, tech levels).

## Key Features & v2.0 Improvements
- **Terraforming**: Implemented as a late-game "Gate-level" technology, allowing players to modify planetary environments at a high cost.
- **Advanced Warp Links**: Introduction of "Link Frequencies," allowing players to share their warp gate networks with allies.
- **Disruptor Buffs**: Rebalanced disruptors to be more strategically viable by allowing player warp ships to travel at jump speeds within their range.
- **AI Improvements**: Fixed long-standing bugs where certain fleets were invisible to the AI or players.
- **Scenario Support**: Enhanced scenario parsing for "flavor text" and randomized player starts.

## Historical Significance
Anacreon is one of the earliest examples of the 4X (eXplore, eXpand, eXploit, eXterminate) genre. This source code represents a dedicated community effort to keep the game playable and relevant nearly 15 years after its original release, solving technical debt while expanding the gameplay mechanics.

## How to Explore
1. **changelog.txt**: Read this first to understand the evolution from v1.31 to v2.0.
2. **ANACREON.PAS**: Start here to see how the various modules are linked.
3. **NPETYPES.PAS**: Examine this for the data structures defining the game's entities.
4. **FASTSCR.ASM**: Look here for interesting x86 assembly optimizations for DOS text rendering.
