+++
title = "Project Announcement"
date = 2026-04-13
+++

## Introduction

Hi, I wanted to share Space Station 2197. A Space Station 13 spin-off now in 3 dimensions.
I have been working on it the past few months on the side, and I think it's in a good position to show off and gauge people's reactions.

But personal introductions first - Hi, you can call me malfu. I have been playing Space Station 13 since 2011, where I stumbled upon it among the much more popular games on BYOND at that time. It’s been my favorite game ever since, and lately, I haven’t been able to stop daydreaming about a 3D fork. Personally, my only hope is that this project results in a mature game that I can just play. I only wonder how it will turn out.

## Project

If you *somehow* don't know Space Station 13, (some people would say) it is an atmospheric simulation roleplaying sandbox game in space.
All playable versions of it are 2D only, but I hope to take a step beyond that and step into three dimensions.
It will run on the Bevy game engine and utilize the open sourced assets of RE:SS3D (the original 3D attempt!).

And not to forget the most important thing: the project will be free and open-source. Forever. 
I do not think Space Station 13 is something to commercialize, and it does not make sense for anybody to think otherwise. This game was made by the community for the community. And it will remain as such.

### Difficulties

This is a huge undertaking and technical decisions matter. 
Rest assured, I am not going to boast about whatever *super rad technology* is used. That is not interesting.
Instead I will point out weakpoints, hopefully to be transparent in all challenges, decisions and solutions.

Also, fair warning, some of the following points are somewhat technical and might require some Bevy and SS13 know-how.

#### Content & Scripting

Forks are the lifeblood of the game. Naturally, this requires a good runtime scripting language...
That is also secure & sandboxed...
And that is also fast...
Aaaand that the syntax is not a complete eyesore.

I will be honest - I have no idea what SS2197 should use. There is not a lack of options, but a decision must be made.
Luau or .NET seem interesting, hell, a WASM solution is possible as well.
But this choice can only be made when benchmarks and a thorough analysis are made.

So as of right now, as a stop gap, core game systems are written in rust while content is defined using Lua Scripting to set prototypes. Scripting a la Factorio.

Additionally, we do not use Bevy's BSN yet. When version 0.20 releases, SS2197 will completely rely on BSN for entity prototyping and definitions.

#### Editor

I think an editor is essential. This includes not only mapping stations but also a visual tool for modifying entity prototypes.
Design questions arise of whether it should be fully offline or only online, among other things.
But again, I am unsure how this will turn out, and for now a simple (yet finicky) offline map editor is included.

#### Bevy & Ecosystem

Bevy... Oh Bevy... my beloved...
Bevy is the game engine of choice. The modular nature of the engine has proven very useful for the project.
But it could be argued that the most important part of it is the community surrounding it and its ecosystem of crates.
Among them include `avian3d` for physics, and `bevy_replicon` for networking, which are used in SS2197.
Bevy and their crates have their problems, including instability, bugs, and reliance on open source contributors. But I feel that inserting ourselves in this welcoming and hard-working community, and participating in their ecosystem by using open-source crates, and potentially even giving back, is a net benefit to all. 
I do not think there is another choice - especially [anti-developer game engines](https://en.wikipedia.org/wiki/Unity_(game_engine)#Runtime_fee_controversy).

#### And much more

These are not the only problems, other stuff include: UI, atmospheric simulation (which to be fair is currently implemented with gas flows only!), and groundwork to work on.

### Other things

#### Roadmap

While many forks start off barebones and try to tackle many problems at once, I propose a different development for this project.

A Department-focused development roadmap.
This means that each department in-game is developed in series, alongside accompanying game mechanics relevant to that department.

It would go something like this:

* **Engineering Department:** Alpha version of the game, includes Atmospheric simulation, tools & interactions and a basic round-based gameplay loop.
* **Security Department:** Focus on combat & weapons mechanics.
* **Medbay Department:** Focus on Medicine & Chemistry mechanics.
* **Service Department:** Focus on Roleplaying flavour and mechanics.

And so on...

My hope is to give a sense of incremental content that is easily noticeable by players and keeps people engaged with the project as it evolves. While easing developers by providing more concise objectives on what to do next.

This does have its drawbacks, e.g. during early development, preferential focus will be given to roadmap milestones, rather than contributions that might fall out of the next milestone's scope. Or that mechanics might need to be revisited later as they might not yet be possible to be fully implemented without another department's content.

#### License

Right now, I am licensing the core project under the MPL 2.0 License.
Reasoning being: MIT is good, but does not incentivize giving back to the community, and AGPL, well...
I identify a sort of "AGPL fatigue" among the SS13 community. While its premise is well-intentioned, it is extremely restrictive in what you can do. Its virality completely disallows private forks, secret server-side recipes or other fun stuff.
However, content-side scripting will be occluded from this license. If this project ever gets official servers, scripting will always be available and permissive if you wish to fork an official upstream.

#### Playtests

Oh, and simply dumping code on GitHub is not fun. We should play it!
I wanted to try out the game publicly as soon as possible. 
Therefore routine playtests of the game are planned.
Initially they will not be fun. But hopefully it will be entertaining to see the evolution of the project while giving us valuable feedback of what you like and what you absolutely hate.
If you are interested, join the Discord discussion, more details to follow.

#### Nothing is final

Finally: nothing is final. The license, content, or even the name "Space Station 2197", are not final.
If you are interested, join the discussion! Just like how, in-game, it is more fun to play with other players, it is also fun to develop with other maintainers. Even though I have started this by myself, I have no delusions to think that I alone have all, or even any, of the answers. I genuinely hope to hear your feedback and possibly contribute alongside you.

## Conclusion

Anyways, that's all for now. 
What does this mean for you, **the player**?
Hopefully a distant yet interesting project that looms ever closer to completion.
If you wish to have a more vested interest, make sure to join whatever communication channels we use, chat about and join the playtests.

And also, if you, whoever you might be, have any questions, critiques or even feel like ranting: 
My DMs are always open. I will try my best to get back to you.

**TL;DR:** FOSS SS13 in 3D made in rust with technical debt already and playtests coming soon.

