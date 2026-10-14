# Skyfire Squadron: design research

## Games studied
- **1945 Air Force**: vertical WW2-style shmup, short missions, auto-fire, one-finger drag. Lots of plane collecting, upgrades and **wingmen** flying beside you who add firepower.
- **Sky Force Reloaded**: gets the progression loop right. Enemies drop currency (stars) that you **keep even when you fail**, which pays for permanent upgrades (cannon, wing guns, missiles, magnet, health, mega bomb). Each stage has medals for kill %, no-damage runs and rescues. Bosses are huge and **multi-part**: you shoot off wing guns and turrets first, then the core.
- **Raiden / Strikers-style arcade shmups**: the in-run power-up curve (P items raise your shot level from a thin stream to a wide spread). Bombs are a **limited panic button** that clears bullets. Bullets are readable glowing orbs, with a tiny player hitbox on a big sprite.
- **Wings of Fury / Atari Bomber**: **air vs. ground**. Guns are for planes and gunners, bombs are for ships, bunkers and islands. Bombs fall in an arc, so you aim them by leading the target. Ships have AA guns you can knock out first.
- **Carrier-style shooters (1942/1943, Carrier Command lineage)**: carriers that launch fighters, submarines that surface to shoot and then dive, battleships with rotating turrets.

## What makes them fun
1. **Core loop (30–120 s missions)**: fly, dodge, shoot, collect, upgrade, replay. Short missions plus permanent upgrades mean every run counts.
2. **Controls**: one finger, relative drag (the plane follows finger *movement*, so the finger never covers the plane), auto-fire. One extra button at most.
3. **Guns vs. bombs**: two weapons for two layers gives the player a second thing to think about. The bomb arc rewards positioning ahead of the target.
4. **Power-ups**: weapon level, shield, wingmen, magnet, repair. Pop-out bubbles that float on screen and are easy to read.
5. **Bosses**: big multi-part machines where each destroyed part changes the attack pattern. Big explosions, a screen shake and a coin shower at the end.
6. **Structure**: themed stages of about 8 missions. A mini-boss mid-stage and a big boss at the end. 3 stars per mission (finish / kill % / health), with stars gating new planes.
7. **Pain points to avoid**: grinding walls, timers, unreadable bullet clutter, punishing deaths with lost progress.

## Our original design: "Skyfire Squadron"
- **Controls**: drag anywhere to fly (relative), auto-fire always on. **Auto-bomb** (default ON, can be turned off in Settings) drops bombs whenever a ship or ground target is lined up ahead. There's also a manual BOMB button and a **MEGA** button (limited charges) that clears bullets and hits everything on screen. Desktop: mouse drag or arrows/WASD, Space = Mega, B = bomb.
- **Enemies**: fighters (V, swoop, weave), bombers with rear gunners, cargo planes that drop power-ups, patrol boats, battleships with rotating turrets, carriers that launch fighters, submarines (surface and fire; only bombs reach them when dived), island AA guns, bunkers and fuel tanks.
- **Bosses (multi-part, original)**: Ironjaw Dreadnought (battleship), Big Mama Carrier, Frostbite Icebreaker plus sub escort, Storm Baron flying wing. Mini-bosses are heavy cruisers and a giant bomber.
- **Progression**: 32 missions across 4 stages (Sunny Seas, Palm Isles, Frosty Fjords, Thunder Night). 3 stars per mission. Coins are kept on failure. 5 planes, each with its own weapon (twin guns, spread, heavy bomber, piercing rail, homing rockets). 6 shared upgrades (Guns, Armor, Bombs, Mega, Wingmen, Magnet). 7-day daily reward streak.
- **Tone**: cartoony, bright and family-friendly. Downed enemy pilots pop a parachute; no gore.
- **Tech**: single HTML file, canvas 2D. Sprites are pre-rendered and shaded at device resolution. Animated layered ocean with wakes, parallax clouds with shadows, additive lighting and a night lightning flash. Adaptive quality (DPR cap, particle cap, layers) by frame-time.
