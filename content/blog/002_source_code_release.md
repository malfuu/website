+++
title = "Source code + roadmap to 0.1"
date = 2026-04-19
+++

## source code release + roadmap to 0.1

Hi again!
The source code for Space Station 2197 is officially out. Here is a quick rundown of how the project is built and where we are heading next. If you want to tinker with the code, this should help you get started.

### Architecture

Right away, the code is split in the classic network code with `shared`, `server`, and `client` crates.
We also strictly separate `game` (simulation mechanics) from `meta` (overlying systems) to keep the codebase clean and isolated.

**Additional core crates:**
- **grid:** Chunk-based sparse grid, with 8x8 chunk entities containing tile information.
- **atmos:** Atmospheric simulation code, currently tile-based with huge eyesore functions.

**Plugins**
- **bevy_replicon:** Handles our netcode and replicates game state to clients authoritatively. But it lacks some functionality such as delta compression (to save bandwidth on atmos chunk updates) and (arguably) entity visibility and high object count.
- **mlua:** Currently used to quickly prototype content, though a lot of boilerplate and attaching lua to the project seems bad. In the future we will rely more on Bevy's BSN solution for defining prototypes instead.

We're also using plugins like avian3d, for physics, proving itself to run well even on high object count. The plan is to also rip out stopgap solutions like bevy_egui soon to avoid future headaches.

### Roadmap

Our focus for version 0.1 is fully implementing the Engineering Department. Here is the short version of the to-do list:

**Foundations**
* Overhaul atmospheric simulation
* improve netcode
* placement tools
* lock in a scripting runtime

**Gameplay & Content**
* Implement power
* construction
* crafting
* UI with networked state

and much more. (like making a decent website as well)

And that is all, put in a very succinct way.

Got any questions? Feel free to ask! And also, if you do want to venture into the code, I have a good amount of issues open if you are brave enough to tackle them! Right [here](https://github.com/malfuu/spacestation2197/issues/).

Thank you,
**malfu**

