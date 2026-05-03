# Bluthbaf

A simple Vampire Survivors-inspired 2D game, developed in GameMaker Studio 2. I've been learning bits of game-dev throughout the years, so I
gave myself the goal of actually making a game myself - for fun! This challange took about 17 days to "complete".

Note that the actual source code is private due to licensing.

<img width="1288" height="754" alt="bluthbaf" src="https://github.com/user-attachments/assets/877610a1-ef6d-4648-b303-42d6662874ca" />


## The Game

- 4 waves of hostile NPCs
- Boss fight arena
- Random item drops (buffs, debuffs, traps, heals, ...)
- Purchasable upgrades / progression
- Procedurally-generated deals between waves

## Screenshots

<img width="1288" height="754" alt="gameplay" src="https://github.com/user-attachments/assets/3a7d9658-f39d-414e-8758-77ea498d7609" />
<img width="1288" height="754" alt="gameplay_intermission" src="https://github.com/user-attachments/assets/f7a23464-56a3-4cc1-9967-00de5d4f82b8" />
<img width="1288" height="754" alt="gameplay_upgrades" src="https://github.com/user-attachments/assets/dd2d9376-87b2-45e9-ae0c-dc12e4d97a1b" />
<img width="1288" height="754" alt="gameplay_deals" src="https://github.com/user-attachments/assets/3a222968-fb00-48ab-987d-10bb19afa544" />
<img width="1288" height="754" alt="gameplay_bossfight" src="https://github.com/user-attachments/assets/70fbb489-475e-4a24-b301-2e54e841ed98" />
<img width="1288" height="754" alt="gameplay_death" src="https://github.com/user-attachments/assets/0c0a13eb-2a96-4ddf-a8d1-739a15b69775" />
<img width="1288" height="754" alt="gameplay_victory" src="https://github.com/user-attachments/assets/1ab2aeb8-8abb-41f9-bda7-6605f7bbcbd8" />

## Technical Stuff

### Attributes system

The player and NPCs all have their own unique attributes, to which we can apply buffs & debuffs via modifiers

<img width="1547" height="1125" alt="dev_attributes" src="https://github.com/user-attachments/assets/f1ea1ce6-574b-4f8a-9bad-2a195b68ef3b" />

### Peripheral

I made a custom UI framework based on GMS2's Flex Panels. It is vastly inspired by HTML and JS.
You can define re-usable layouts with XML, supply bindings and add dynamic functionallity through 
GML.

<img width="1205" height="503" alt="ui_markup" src="https://github.com/user-attachments/assets/a2e57228-8406-44b0-ba29-19c1bd7509ce" />
<img width="973" height="507" alt="ui_script" src="https://github.com/user-attachments/assets/e232fcfa-bb23-4b33-9f4b-ae26aaba7c35" />
<img width="919" height="223" alt="ui_result" src="https://github.com/user-attachments/assets/a1cbb135-dec1-4b74-9c8d-7ebb25384559" />

### JSON deserialition

Instead of manually creating loader functions for various classes/resources (sequences, item drops, modifiers, ...), Bluthbaf 
supports deserializing JSON data into real instances/structs at run-time based on additional metadata.

In the following example, we instantiate the `CItemDrops` constructor (and populate it with associated data) by loading a .json file via `DeserializeFile()`.

<img width="519" height="141" alt="jd_code" src="https://github.com/user-attachments/assets/71d297b5-0ccd-4582-b7fa-4b79cfabf8c3" />
<img width="791" height="947" alt="jd_json" src="https://github.com/user-attachments/assets/7268d6be-4987-443f-ab48-dbf1a71d0dd4" />


### Misc

On top of that, the game features some addition custom systems:

- Time management (clocks, tasks & sequences)
- Event bus for game-wide communication
- Console variables (game rules, preferences)

## Ending Note

This challange served to combat my inner perfectionism, and was also an opportunity to learn more. Thanks for reading this whole thing. As a reward, here's a screenshot of the game from its first day of development! :D

<img width="1283" height="765" alt="dev_day1" src="https://github.com/user-attachments/assets/da8ee9b2-22c0-43d0-aaa9-038134e25b0a" />

