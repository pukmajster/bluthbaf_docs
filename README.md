# Bluthbaf

A simple Vampire Survivors-inspired 2D game. I've been learning bits of game-dev throughout the years, so I
gave myself the goal of actually making a game myself - for fun! This challange took about 17 days to "complete".

Note that the actual source code is private due to licensing.

<img width="1288" height="754" alt="bluthbaf" src="https://github.com/user-attachments/assets/31acf6f5-4a8e-400c-97f8-3909cf945b73" />

## The Game

- 4 waves of hostile NPCs
- Boss fight arena
- Random item drops (buffs, debuffs, traps, heals, ...)
- Purchasable upgrades / progression
- Procedurally-generated deals between waves

## Screenshots

<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-07-12" src="https://github.com/user-attachments/assets/8a6cad30-e26c-4afb-a03c-1aee3cf6d720" />
<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-03-57" src="https://github.com/user-attachments/assets/d8131688-fc2b-41e8-a822-972d5c787a49" />
<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-06-23" src="https://github.com/user-attachments/assets/302192ed-e951-41e6-8973-e128d2070ff4" />
<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-05-37" src="https://github.com/user-attachments/assets/890c4c96-e0c9-441b-8d8c-d86afd5e9c42" />
<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-07-49" src="https://github.com/user-attachments/assets/b76a8203-99d6-45c3-902a-c7681974b6cc" />
<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-05-03" src="https://github.com/user-attachments/assets/e60db76e-f662-4dc0-8f2c-3e50c13e9e14" />
<img width="1288" height="754" alt="Screenshot From 2026-04-20 00-09-24" src="https://github.com/user-attachments/assets/c472ee8c-c40f-4c6f-9435-9d085294932d" />

## Technical Stuff

### Attributes system

The player and NPCs all have their own unique attributes, to which we can apply buffs & debuffs via modifiers

<img width="1547" height="1125" alt="image" src="https://github.com/user-attachments/assets/cb18db6a-a0c9-427f-91e5-a3ff1ea07d82" />

### Peripheral

I made a custom UI framework based on GMS2's Flex Panels. It is vastly inspired by HTML and JS.
You can define re-usable layouts with XML, supply bindings and add dynamic functionallity through 
GML.

<img width="1205" height="503" alt="image" src="https://github.com/user-attachments/assets/36ce7e43-f7a1-415c-bb99-f42e022c7e58" />
<img width="973" height="507" alt="image" src="https://github.com/user-attachments/assets/70638040-fd03-4de5-880d-45b1b7c00560" />
<img width="919" height="223" alt="image" src="https://github.com/user-attachments/assets/aa77f97f-7bfa-4055-a3a6-e8c4afc8f980" />

### JSON deserialition

Instead of manually creating loader functions for various classes/resources (sequences, item drops, modifiers, ...), Bluthbaf 
supports deserializing JSON data into real instances/structs at run-time based on additional metadata.

In the following example, we instantiate the `CItemDrops` constructor (and populate it with associated data) by loading a .json file via `DeserializeFile()`.
<img width="519" height="141" alt="image" src="https://github.com/user-attachments/assets/c0861540-26b0-4d0c-9bb0-8c6582f175db" />
<img width="791" height="947" alt="image" src="https://github.com/user-attachments/assets/64894d9a-464a-4904-8efc-72bc65792348" />

### Misc

On top of that, the game features some addition custom systems:

- Time management (clocks, tasks & sequences)
- Event bus for game-wide communication
- Console variables (game rules, preferences)

## Ending Note

This challange served to combat my inner perfectionism, and was also an opportunity to learn more. Thanks for reading this whole thing. As a reward, here's a screenshot of the game from it's first day of development! :D

<img width="1283" height="765" alt="Screenshot From 2026-03-26 23-00-40" src="https://github.com/user-attachments/assets/a8dd2f62-bc8f-4348-9b39-bcf46975316a" />
