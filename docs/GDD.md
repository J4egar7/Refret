# Refret: Game Design Summary (v1.0)

Working title: **Refret**. Engine: Unity 6 LTS (URP), C#. Platform: Windows (Steam). Single-player, third-person 3D action RPG, gamepad and keyboard.

## 1. Pitch
A realistic, grounded, dark-fantasy action RPG with free, expressive movement and combat. You are the last apprentice of a murdered High Warden, carrying the Concord Seal, the only thing that can rebind a failing ward-stone. You hunt the monsters pouring out of the Hollow, found a Company, rebuild what is left, and live with the price of every choice. Players can build their own spells, items, quests, cutscenes and scripts with the same editors the game uses.

## 2. Pillars
1. **Dark, grounded fantasy.** Monsters are the central threat. Victory costs something; hope is earned.
2. **The world remembers.** Choices, honor, reputation and relationships change dialogue, quests, prices and endings.
3. **Build anything.** Every sword, spell, quest and cutscene is data. The dev editors are the player editors.
4. **Your hero, your look.** Deep 3D character customization with import support.
5. **Your people, your home.** Found a faction; watch a camp become a village and a free hold.
6. **Depth over sprawl.** A long, emotional campaign on reusable systems, with optional content instead of filler.

## 3. Story in one paragraph
For 200 years the Concord and its Wards held the monsters of the Hollow behind the Pale. In one year the harvests failed, High Warden Selwyn Marr was murdered, and the Wards began to fail. The game opens with a string of doomed soldiers at Cairn Nine (the hook), then the 15-minute Prologue in Hollowmere. Every Ward runs on a living keeper (the Quiet Tithe); the monsters are the unquiet dead and the starved, fed by every war and famine.

**Structure:** Hook (Cairn Nine) > Prologue (Ashes) > Act 1 (Road and Camp) > Act 2 (Failing Wards, 4 regions any order) > Long Winter > Act 3 (Gathering) > Act 4 (Reckoning) > Act 5 (Last Night) > Epilogues.

**Five endings, chosen by the game (no ending menu):** 3 main (Rebinding, Reign of Steel, Long Hunt) decided by main-story decisions; 2 hidden (Release, Wild Concord) earned through side questlines plus a road requirement. Main endings score only from main-story decisions; every decision option carries a +1 to +3 pull and writes a tag a later scene reads.

## 4. Factions and cast
- **Factions:** Reach Granary Wardens, Tiderun League, Ironmarch Banners, Vael Collegium, the Hollowguard, plus your own Greywatch Company.
- **Companions (6):** Bran Kell, Tamsin Rook, Elias Thorne, Jory Vance, Kharga, Isolde Venn. Each has a combat role, a personal arc, a romance or deep-friendship path, a trust-unlocked spell block, and a way to die or leave.
- **Key figures:** Aldric Hale (mentor, dies in the prologue), Wren (sibling), Chancellor Marek Dray, Lord Commander Ysolde Varn, Mother Sable, Pip.

## 5. Scope (hard limits for v1.0)
- 1 starter town, 1 capital, 4 main regions + 4 optional, 8 dungeons, the Hollow.
- Main story 45-55 h (about 65% combat); 60+ side quests; 5 endings.
- 6 companions, 40+ named NPCs, hundreds of generated settlers with Lifelines.
- Combat: sword, spear, dagger, staffs, 40+ spell blocks, Hunter's Codex (one branch per monster family).
- 60+ monsters in 10 families, 6 large bosses.
- Player tools: character creator/import, spell, item, quest/dialogue and cutscene editors, Lua scripting (MoonSharp), mod export/import.
- **Out of scope:** multiplayer, giant seamless open world, full voice acting, procedural dungeons, PvP, mobile.

## 6. Core systems
Relationships (affinity, trust, romance, jealousy) - Reputation (per town/faction) - Honor - Politics (influence, votes, treaties) - Social (rumors, schedules, etiquette) - Spell blocks (trigger, shape, element, effect, modifier) - Gear (rarity, affixes, sockets, crafting) - Wards and monster pressure - Cost Ledger and Name cards - Seal corruption - Camp/settlement - Notice board, armies, mercenaries.

## 7. Combat-first rules
Combat is about 65% of critical-path time. Calm beats last 3 minutes max and end in a threat. Every region has a combat spine (4-6 fights, a hunt, a set piece, a boss). Decisions change how fights go, not just dialogue.

## 8. Art and tech
Realistic, desaturated, moody grading with selective warm light, fog and weather. Asset packs for environments, Mixamo-style animation, modular character parts. Lua via MoonSharp, UniVRM and glTFast for imports, Newtonsoft JSON, Addressables.

## 9. Production rules
One batch per prompt: build, test, commit. Never start a phase before its dependencies are playable. The vertical slice (end of Phase 8) is the gate before player editors. Data-driven content only; small scripts with one job; a manual test checklist per batch.
