# Idle Quest v2 — Full Spec

## What's Fixed vs v1
- Enemy DEF was NaN (enemies had no `def` property) → Fixed
- Empty equip slot click crashed → Fixed (guards added)
- Death overlay never auto-closed → Fixed
- No enemy HP bar → Added with color transitions
- No offline progress → Added (calculates gold/XP while away)
- Hero never moved → Now animates forward per attack
- Combat text piled up infinitely → Capped at 8 elements
- No boss at section end → Added boss every 5 stages

## New Features
- Enemy HP bar with red/yellow/green transitions
- Hero position advances per kill (walks down path)
- Gold/XP numbers fly to HUD counters
- 6 enemy types (Slime, Goblin, Skeleton, Orc, Wolf, Dragon)
- Boss fight at end of each section (5 stages)
- Boss has special name, more HP, more gold, dramatic entrance
- Web Audio API sound effects (attack, crit, death, levelup, loot, boss)
- Settings panel (SFX on/off, view stats, reset save)
- Offline progress on return (gold + XP earned while away)
- Death screen shows: enemies killed, gold lost, time survived
- Enemy shake animation on crit
- Smooth HP bar drain (CSS transition)
- Toast queue system (multiple toasts stack)
- Auto-battle toggle
- Welcome back banner on return

## Game Feel
- Hero bobs while walking, lunges forward on attack
- Enemy scales up when appearing, shrinks on death
- Screen shake on boss entrance
- Purple flash on level up
- Gold counter animates when gold added
- Stage progress dots pulse

## Stats
- Hero: ATK = level*5 + weapon, DEF = level*2 + armor+helmet+boots, HP = 50 + level*20
- Enemy: HP/ATK scale by stage multiplier
- Crit: 10% chance, 1.5x damage
- DEF reduction: 30% ignored (enemies have DEF = HP/10)
- Gold: scales with stage
- XP: 3-8 per kill, level up = xpToLevel * 1.5

## Progression
- 5 stages per section
- Every 5th stage = BOSS (Dragon)
- After section 1: Orc added, Wolf added, Dragon boss
- Gear tier increases with section
- 25 inventory slots, 4 equipment slots