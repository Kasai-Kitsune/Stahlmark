# STAHLMARK

A wireframe raycaster FPS. Quake-esque movement on a Wolfenstein-esque-style engine (my hope anyway), arcade lives instead of roguelike runs, procedurally generated ring-based rooms.

> **Status: Pre-Alpha**
> Core loop is playable but unbalanced, unfinished. Multiple enemy types now present. Expect bugs, placeholder art, and potentially breaking changes between commits.

---

## Controls

**Desktop**
- `WASD` to move
- Mouse to look (pointer lock)
- Click to fire

**Mobile (landscape only)**
- Left side: virtual joystick for movement
- Right side: drag to look
- On-screen fire button

---

## What's Working

- Raycaster renderer (320 rays, 60° FOV) with Y-shearing for vertical look
- Quake-style movement and collision
- HUD: HP bar, armor bar, ring counter, reticle
- Procedurally generated infinite ring-based room grid (start room, arenas, caches, ambushes, gauntlets, dark rooms)
- Ring lock system: clearing a ring locks the door back to the previous ring
- Hitscan firing
- Multiple enemy types (Krabbe, Bulwark, Skytter) with distinct behaviors
- In-game debug menu (room clear + enemy spawning)
- Weapon switching and ammo system

---

## Design Notes

- Black fill on every object first, colored edge lines on top.
- Weapons sit on an impact-vs-penetration axis: Nåde (pistol) staggers (slows) everything and penetrates nothing, Klarhet (sniper) penetrates everything and staggers nothing, Gungnir (Bullpup AR) splits the difference. Enemy size determines which weapon is the right call.
- No ADS, no headshots, no 3D weapon models. Everything is hitscan with 2D side-profile HUD sprites.

---

## Notes

This is a solo hobby project and a worldbuilding tie-in to my personal Stahlmark setting. Structure, balance, and content may shift a lot during pre-alpha.
