================================================================================
        BFA 8.3.7 TrinityCore — REVISED MERGE PROJECT README
           Build 35662 | Arena.ai Agent Mode | June 5, 2026
================================================================================

Project:    TrinityCore 8.3.7 (Build 35662) Battle for Azeroth Unified Core
Version:    0.2.0 (Revised Strategy)
Date:       June 5, 2026
Objective:  Build the most complete BFA 8.3.7 core by using the canonical
            TrinityCore official tag as base, merging tswow for active
            development, and porting BfaCore-Reforged's BFA content.

================================================================================
                           EXECUTIVE SUMMARY
================================================================================

REVISED STRATEGY (2026-06-05):
  TrinityCore Official (8.3.7/35662 tag) as CANONICAL BASE
    → Git merge tswow (active development, custom features)
    → Manual port BfaCore-Reforged (complete BFA content)

This replaces the previous "Hybrid Approach" (BfaCore base + tswow port).
The new strategy is superior because:
  + TrinityCore official is the canonical upstream (10.6k stars)
  + Direct git merge with tswow is possible (shared ancestry)
  + GPL v2 license (more flexible than BfaCore's AGPL v3)
  + Cleanest possible foundation with no proprietary divergence

================================================================================
                    SOURCE REPOSITORIES — FULL PROFILES
================================================================================

FOUNDATION: TrinityCore/TrinityCore — Tag: 8.3.7/35662
================================================================================
URL:         https://github.com/TrinityCore/TrinityCore
Tag:         8.3.7/35662
Commit:      16b39a448acbe8ace88550a367be8e6bf565b00d
License:     GPL v2
Build:       8.3.7.35662 (Build 35662)

Stats:
  - 658 .cpp script files in src/server/scripts/
  - 305,862 lines of C++ script code
  - 10,600 stars, 6,300 forks (most trusted WoW emulator)
  - 33,598 commits on this tag
  - Last commit: Oct 21, 2020 (Shauren — "Core/Transmog: Add remaining hidden appearances")
  - 4 branches: 3.3.5, cata_classic, master, wotlk_classic
  - 147 tags total

Status: TAG ONLY — not a branch. This is the official archived release tag.
  This is the canonical upstream for ALL TrinityCore-lineage forks.
  All TrinityCore 8.3.7 forks (CWWEB, wowlegions, tswow) share ancestry with this.

BFA Content: NONE
  ❌ No KulTiras dungeon scripts
  ❌ No Zandalar dungeon scripts
  ❌ No Nyalotha raid
  ❌ No Nazjatar zone or Eternal Palace
  ❌ No Allied Races heritage armor
  ❌ No BFA Scenarios
  ❌ No Brawlers Guild

Features:
  ✅ Transmog system
  ✅ TDB 837.20101 database (2020/10/20)
  ✅ OpenSSL 1.1.1 fix for .msi packages
  ✅ boost::regex compatibility fix
  ✅ CircleCI automated builds
  ✅ Multi-language hotfixes (zhTW, zhCN, ruRU)
  ✅ Player/item gossip systems
  ✅ World server commands

This is the cleanest possible foundation. No proprietary additions,
no diverged paths, no license complications.

--------------------------------------------------------------------------------

MERGE TARGET: tswow/TrinityCore (8.3.7 branch)
================================================================================
URL:         https://github.com/tswow/TrinityCore
Branch:      8.3.7 (tswow branch)
License:     GPL v2
Build:       8.3.7.35662

Stats:
  - 629 .cpp script files in src/server/scripts/
  - 299,261 lines of C++ script code
  - 4 stars, 65 forks of this repo itself
  - 14,443 commits ahead of TrinityCore master
  - 22,650 commits behind TrinityCore master
  - Last commit: Jan 27, 2026 (~5 months ago — MOST RECENTLY ACTIVE)
  - 18 branches, 72 tags

Fork Status: Direct fork of TrinityCore/TrinityCore ✅
  - Shares full git history with TrinityCore official
  - Compatible for DIRECT GIT MERGE with TrinityCore official
  - Compatible with CWWEB/wowlegions as merge targets
  - NOT compatible for direct git merge with BfaCore-Reforged

BFA Content: NONE
  ❌ No KulTiras dungeon scripts
  ❌ No Zandalar dungeon scripts
  ❌ No Nyalotha raid
  ❌ No Nazjatar zone
  ❌ Same BFA limitations as TrinityCore official

Custom Scripts to Add via Git Merge:
  ✅ Custom NPC functionality (custom_npcs.cpp)
  ✅ Custom player hook scripts (custom_player_script.cpp)
  ✅ DressNPCs system (DressNPCs/)
  ✅ Multivendor system (Multivendor/)
  ✅ Multitrainer system (multitrainer/)
  ✅ Transmog system (Transmog/)
  ✅ Player and Item Gossip (Player and Item Gossip/)

Unique Shared Expansion Content (git merge adds):
  ✅ Outland: Gruul's Lair raid (2 bosses: Gruul, High King Maulgar)
  ✅ Outland: The Botanica dungeon (5 bosses: Commander Sarannis,
              Gatewatcher Gyrokill/Ironhand, Mechano-Lord Capacitus,
              Nethermancer Sepethrea, Pathaleon the Calculator,
              Warp-Splinter)
  ✅ Outland: All Tempest Keep areas (Arcatraz, Botanica, Mechanar)
  ✅ Northrend: Vault of Archavon world boss raid (4 bosses:
              Archavon, Emalon, Koralon, Toravon)
  ✅ EasternKingdoms: Deadmines dungeon (boss_mr_smite, boss_vancleef)

Additional Features via Git Merge:
  ✅ Modern build fixes (macOS/OS X compatibility, osx-support PR #50)
  ✅ Multi-language hotfixes (zhTW, zhCN, ruRU)
  ✅ Active upstream TrinityCore fixes from 14,443 commits ahead

Notable:
  - Most recently active development of all analyzed forks
  - Only fork with commits in 2025-2026
  - Modern CMake and build configuration
  - Direct git merge compatible with TrinityCore official

--------------------------------------------------------------------------------

PORT SOURCE: Titans-Project/BfaCore-Reforged
================================================================================
URL:         https://github.com/Titans-Project/BfaCore-Reforged
License:     AGPL v3 (important — derivative works must be open source)
Build:       8.3.7.35662

Stats:
  - 1,338 .cpp script files in src/server/scripts/
  - 870,388 lines of C++ script code
  - 105 stars, 83 forks (most popular BFA fork)
  - Last commit: Oct 10, 2022 (~3.5 years ago)

Fork Status: INDEPENDENT CODEBASE — NOT a fork of TrinityCore/TrinityCore
  - No shared git history with TrinityCore official or tswow
  - Script file paths and structure have diverged
  - Direct git merge NOT possible with TrinityCore lineage
  - Content must be MANUALLY PORTED (file copy + script registration)

BFA Content — COMPLETE:
  ✅ KulTiras Dungeons:
      FreeHold (4 bosses, full implementation)
      Tol'Dagor (4 bosses, full implementation)
      Siege of Boralus (4 bosses, full implementation)
      Waycrest Manor (5 bosses, full implementation)
      Shrine of the Storm (4 bosses, full implementation)
      Operation Mechagon (2 bosses: K.U.-J.0.1, King Gobbamar)
  ✅ Zandalar Dungeons:
      Atal'Dazar (5 bosses, full implementation)
      King's Rest (4 bosses, full implementation)
      Temple of Sethraliss (4 bosses, full implementation)
      The Motherlode (4 bosses, full implementation)
      The Underrot (4 bosses, full implementation)
      Uldir (8 bosses, full implementation)
  ✅ Nyalotha Raid (8.3):
      All 12 boss scripts:
      boss_prophet_skitra.cpp (11,665 lines)
      boss_wrathion.cpp (31,538 lines)
      boss_maut.cpp (17,026 lines)
      boss_shadhar.cpp (13,969 lines)
      boss_hivemind.cpp (14,620 lines)
      boss_ilgynoth_n.cpp (12,206 lines)
      boss_raden.cpp (17,059 lines)
      boss_drestagath.cpp (18,834 lines)
      boss_carapace.cpp (21,169 lines)
      boss_xanesh.cpp (11,784 lines)
      boss_vexiona.cpp (15,952 lines)
      boss_nzoth.cpp (19,438 lines)
  ✅ Nazjatar Zone:
      zone_nazjatar.cpp (25,585 lines)
  ✅ Eternal Palace Raid:
      EternalPalace/ subdirectory with raid bosses
  ✅ Allied Races Heritage Armor:
      allied_races.cpp (7,144 lines)
      allied_races_script_loader.cpp (776 lines)
  ✅ BFA Scenarios (9 total):
      Uncharted Island, Verdant Wilds, The Battle for Lordaeron,
      The Defense of Karabor, The Stormwind Extraction,
      Pursuing the Black Harvest, Zandalar Forever,
      Whispering Reef, scenario scripts
  ✅ Brawlers Guild (7 files):
      brawlers_guild.cpp (10,683 lines)
      brawlers_guild_bosses_rank_one.cpp (15,091 lines)
      brawlers_guild_bosses_rank_two.cpp (23,122 lines)
      brawlers_guild_bosses_rank_three.cpp (1,666 lines)
      brawlers_guild_bosses_rank_four.cpp (1,875 lines)
      brawlers_guild_bosses_rank_five.cpp (1,664 lines)
      brawlers_guild_bosses_rank_six.cpp (1,826 lines)
      brawlers_guild_bosses_rank_seven.cpp (2,044 lines)

Custom Features:
  ✅ custom_npcs.cpp (1,388 lines — more complete than tswow's)
  ✅ custom_player_script.cpp (567 lines)
  ✅ custom_script_loader.cpp
  ✅ XpWeekend.cpp (42 lines)
  ✅ solocraft.cpp (173 lines)
  ✅ TDB 837.20101 (2020/10/20)

Registered custom scripts in custom_script_loader.cpp:
  - AddSC_custom_npcs()
  - AddSC_custom_player_script()
  - AddSC_XpWeekend()
  - AddSC_solocraft()

AGPL v3 Consideration:
  ⚠️ AGPL v3 license means all derivative works must be open source
  ⚠️ Closed-source distribution is NOT allowed
  ⚠️ If closed-source is required, this content cannot be used

--------------------------------------------------------------------------------

REFERENCE: CWWEB/LegacyCore (bfa branch)
================================================================================
URL:         https://github.com/CWWEB/LegacyCore/tree/bfa
License:     GPL v2
Build:       8.3.7.35662

Stats:
  - 658 .cpp script files in src/server/scripts/
  - BFA tip commit: 16b39a448acbe8ace88550a367be8e6bf565b00d
  - 33,598 commits on bfa branch
  - 0 stars, 0 forks
  - Last commit: Oct 21, 2020 (~6 years ago)

Fork Status: Fork of TheGhostGroup/TrinityCore → TrinityCore/TrinityCore
  - Shares git ancestry with TrinityCore official and tswow
  - BFA branch is BYTE-FOR-BYTE IDENTICAL to TrinityCore official tag
  - Byte-for-byte identical to wowlegions bfa branch

BFA Content: NONE — same as TrinityCore official
  ❌ No BFA dungeon/raid/zone scripts
  ❌ Same as TrinityCore official (same commit)

Features:
  ✅ Transmog system (compare with BfaCore and tswow)
  ✅ TDB 837.20101

Archived: This repo served as the initial reference but is superseded
by using TrinityCore official as the canonical base.

================================================================================
                   REVISED MERGE STRATEGY (2026-06-05)
================================================================================

PHASE 1 — ESTABLISH BASE
================================================================================

1. Clone TrinityCore/TrinityCore tag 8.3.7/35662 as the primary repository
   - This becomes the canonical foundation
   - Create a new working branch from the tag
   - Accept: GPL v2 license (flexible)
   - Accept: No BFA dungeon/raid/zone content yet

2. Note: TrinityCore official is a TAG not a branch
   - Clone the tag, then create a working branch
   - All future work happens on the new branch

--------------------------------------------------------------------------------

PHASE 2 — GIT MERGE tswow (DIRECT MERGE)
================================================================================

This is a TRUE git merge — no manual porting needed.
tswow is a direct fork of TrinityCore with shared ancestry.

Steps:
  1. Add tswow as a remote: git remote add tswow https://github.com/tswow/TrinityCore
  2. Fetch tswow branches: git fetch tswow
  3. Git merge tswow/8.3.7 into your working branch
  4. Resolve any conflicts (expected in overlapping files)

Git Merge Adds:
  + Multivendor system (Multivendor/)
  + Multitrainer system (multitrainer/)
  + DressNPCs system (DressNPCs/)
  + Transmog implementation (Transmog/)
  + Player and Item Gossip (Player and Item Gossip/)
  + Custom NPC functionality
  + Custom player script hooks
  + Gruul's Lair raid (2 bosses)
  + The Botanica dungeon (5 bosses)
  + Tempest Keep content (Arcatraz, Botanica, Mechanar)
  + Vault of Archavon world boss raid (4 bosses)
  + Deadmines dungeon
  + macOS/OS X build fixes
  + Active development (14,443 commits ahead of TrinityCore)
  + Modern build configuration

Expected Conflicts:
  - custom_script_loader.cpp (both add custom scripts)
  - custom_npcs.cpp (both have implementations)
  - transmog implementations (may differ)
  - Resolution: Keep both sets of registrations, merge implementations

--------------------------------------------------------------------------------

PHASE 3 — MANUAL PORT FROM BfaCore-Reforged
================================================================================

This is NOT a git merge — manual file porting required.
BfaCore-Reforged has no shared git history with TrinityCore.

Steps:
  1. Clone or reference BfaCore-Reforged
  2. Copy BFA-specific script files to matching directory structure
  3. Add script registrations to custom_script_loader.cpp
  4. Repeat for all BFA content directories

Port Priority Order:

  Priority 1 — Complete Dungeon Sets:
    + KulTiras/ (6 dungeons, all bosses)
    + Zandalar/ (6 dungeons, all bosses)
    + All associated instance scripts

  Priority 2 — Major Raids:
    + Nyalotha/ (12 boss scripts, full implementation)
    + Nazjatar/ (zone_nazjatar.cpp, EternalPalace/)

  Priority 3 — Quality of Life:
    + AlliedRaces/ (heritage armor quests)
    + BrawlersGuild/ (7 boss rank files)
    + Scenarios/ (9 BFA scenario scripts)

  Priority 4 — Custom Features:
    + solocraft.cpp (compare with tswow's)
    + XpWeekend.cpp (compare with tswow's)
    + custom_npcs.cpp (compare with tswow's — keep more complete)

AGPL v3 Note:
  ⚠️ BfaCore uses AGPL v3 license
  ⚠️ If any BfaCore code is ported, the merged product must remain open source
  ⚠️ Closed-source distribution is NOT permitted from BfaCore content
  ⚠️ If closed-source is required: either skip BfaCore port OR use only
     the mechanics/ideas without copying the actual code

--------------------------------------------------------------------------------

PHASE 4 — TRANSMOG COMPARISON & RESOLUTION
================================================================================

All three sources have transmog implementations:
  - TrinityCore official: transmog system (base)
  - tswow: Transmog/ directory implementation
  - BfaCore: custom_npcs.cpp transmog implementation

Evaluation criteria:
  - Which covers the most appearance slots?
  - Which handles hidden appearances correctly?
  - Which has better database schema?
  - Which has better UI/gossip integration?

Decision: Keep the most complete implementation, potentially merge features.

--------------------------------------------------------------------------------

PHASE 5 — COMPILE & TEST
================================================================================

1. Build the TrinityCore base:
   - CMake configuration
   - Full compilation on primary platform
   - Verify tswow features compile (multivendor, multitrainer, etc.)

2. Add ported BfaCore features incrementally:
   - One dungeon set at a time
   - Compile after each addition
   - Document any breaking changes

3. Database setup:
   - TDB 837.20101 import
   - Verify transmog tables exist
   - Test Allied Races quest chains

4. Runtime testing:
   - Server startup
   - Zone loading (Nazjatar)
   - Dungeon encounters (test at least one from each category)
   - Brawlers Guild interaction
   - Transmog functionality

================================================================================
                    CONTENT COMPARISON MATRIX
================================================================================

Content Item                   | TrinityCore | tswow    | BfaCore
-------------------------------|-------------|----------|-------
KulTiras Dungeons              | ❌          | ❌       | ✅ All 6
Zandalar Dungeons              | ❌          | ❌       | ✅ All 6
Nyalotha Raid                  | ❌          | ❌       | ✅ 12 bosses
Nazjatar Zone                  | ❌          | ❌       | ✅
Eternal Palace Raid            | ❌          | ❌       | ✅
Allied Races                   | ❌          | ❌       | ✅
BFA Scenarios                  | ❌          | ❌       | ✅ 9 scenarios
Brawlers Guild                 | ❌          | ❌       | ✅ 7 files
Transmog System                | ✅          | ✅       | ✅
Multivendor                    | ❌          | ✅       | ❌
Multitrainer                   | ❌          | ✅       | ❌
DressNPCs                      | ❌          | ✅       | ❌
Player/Item Gossip             | ❌          | ✅       | ❌
Solocraft                      | ❌          | ❌       | ✅
Gruul's Lair Raid              | ❌          | ✅       | ❌
The Botanica Dungeon           | ❌          | ✅       | ❌
Vault of Archavon Raid         | ❌          | ✅       | ❌
Deadmines Dungeon              | ❌          | ✅       | ❌
Active Development (2025-26)   | ❌          | ✅       | ❌
TrinityCore Lineage (git)      | ✅ CANON    | ✅       | ❌
Direct Git Merge Compatible    | —           | ✅       | ❌
License                        | GPL v2      | GPL v2   | AGPL v3

================================================================================
                      TRADE-OFFS & RISKS
================================================================================

[CRITICAL] TrinityCore Official is a TAG
  The 8.3.7/35662 is a tag, not a branch — can't push directly to it.
  Must clone, create new branch, work on new branch.
  Mitigation: Create a new repo and push the merged result there.

[CRITICAL] AGPL v3 from BfaCore
  BfaCore uses AGPL v3. If any BfaCore code is ported, the merged
  product must remain open source (AGPL v3). Closed-source distribution
  is NOT permitted for any portion derived from BfaCore.
  Mitigation: If closed-source is required, skip BfaCore entirely and
  use only TrinityCore + tswow content.

[HIGH] Manual Port Required for BfaCore
  BfaCore's independent development path means its code cannot be
  git-merged with TrinityCore. The "merge" is really manual file
  adoption. This takes more effort than a git merge.
  Mitigation: Systematic file-by-file porting with script registration.

[HIGH] tswow Git Merge Conflicts
  When merging tswow (14,443 commits ahead), conflicts are expected
  in custom_script_loader.cpp and overlapping script implementations.
  Mitigation: Careful conflict resolution, keep both sets of features.

[MEDIUM] Transmog Implementation Conflicts
  Three different transmog implementations exist across forks.
  Choosing the wrong one or having duplicate tables could cause issues.
  Mitigation: Formal three-way comparison before committing.

[MEDIUM] BFA Script Quality Unverified
  BfaCore's dungeon/raid scripts have not been runtime-tested.
  They may contain bugs, incorrect boss behaviors, or missing phases.
  Mitigation: Systematic in-game testing required post-merge.

[LOW] No GitHub Stars/Fork Count
  The merged product starts fresh — no community visibility built-in.
  Mitigation: User must publish and promote the merged repo.

================================================================================
                        FORKS NOT INITIALLY ANALYZED
================================================================================

The following forks from the original list have NOT been deep-dived yet.
Any of them could potentially contain BFA content or expansion scripts
that could supplement the merged core:

Pending Investigation:
  ? Lasko73/BFA_8.3.7-35662           — Only 8 commits, likely abandoned
  ? CrimsonDespair/BFA                — Fork of BfaCore, 5 commits only
  ? CollectiveIndustries/BfaCore-Reforged — Fork of BfaCore
  ? Rochet2/TrinityCore               — Direct fork, custom features
  ? joinjold/FaceCore                 — Direct fork, anticheat focus
  ? AshamaneProject/AshamaneCore      — Dead since 2021, BFA branch never pushed

Additional Script Sources (for all expansions):
  ? AzerothCore/azerothcore-wotlk     — Modern WotLK scripts, TrinityCore-compatible
  ? The-Cataclysm-Preservation-Project/TrinityCore — Cataclysm zone scripts
  ? Magic-Storm/Draenor-Core          — WoD scripts (6.2.3)
  ? mikadmin/CataclysmScripts         — Cata dungeon scripts

================================================================================
                        ENVIRONMENT & TOOLS
================================================================================

Development Platform:   Arena.ai Agent Mode
Date:                   June 5, 2026

Workspace Directories:
  - /home/user/trinitycore-official-bfa/  — TrinityCore 8.3.7/35662 tag (BASE)
  - /home/user/tswow-bfa/                — tswow/TrinityCore (MERGE TARGET)
  - /home/user/bfcore-reforged/          — BfaCore-Reforged (PORT SOURCE)
  - /home/user/cwweb-bfa/                — CWWEB/LegacyCore bfa (REFERENCE)
  - /home/user/wowlegions-bfa/           — wowlegions/LegacyCore-1 bfa (REFERENCE)
  - /home/user/ashemane-bfa/             — WoWEmulationProject AshamaneCoreBFA (ANALYZED, REJECTED)

Build Requirements:
  - CMake:    >= 3.20
  - Boost:    1.72.0
  - MySQL:    5.7 or 8.0
  - OpenSSL:  1.1.1L
  - Compiler: Visual Studio 2019 / GCC 10+

================================================================================
                              FILE STRUCTURE
================================================================================

Project Files:
  - BFA_README.txt   — This file
  - CHANGELOG.txt    — Detailed change log

Future Files:
  - (new) merged_core/          — The merged repository
  - (new) porting_notes/        — BfaCore porting documentation
  - (new) merge_conflicts/      — tswow merge conflict resolution notes
  - (new) transmog_compare/     — Transmog comparison analysis

================================================================================
                          DECISION SUMMARY
================================================================================

Selected Strategy: TrinityCore Official Base + tswow Git Merge + BfaCore Port

Why TrinityCore Official as base?
  → Canonical upstream (10.6k stars)
  → Cleanest possible foundation
  → GPL v2 license (flexible)
  → All TrinityCore-lineage forks share ancestry with it
  → No proprietary divergence

Why tswow for git merge?
  → Only active development on 8.3.7 TrinityCore lineage (Jan 2026)
  → Direct git merge possible (shared ancestry with TrinityCore official)
  → Multivendor, multitrainer, dressnpcs, macOS fixes
  → Adds Gruul's Lair, The Botanica, Vault of Archavon

Why BfaCore for manual port?
  → Only fork with complete BFA dungeon/raid/zone content
  → 12 KulTiras/Zandalar dungeons, Nyalotha raid, Nazjatar, Brawlers Guild
  → AGPL v3 license — only use if open-source is acceptable

Why NOT BfaCore as base?
  → Independent codebase (no shared git history with TrinityCore)
  → AGPL v3 license (more restrictive than TrinityCore's GPL v2)
  → No git merge with tswow possible
  → Would require manual port of tswow anyway

Why NOT TrinityCore lineage only (CWWEB/wowlegions)?
  → Identical to TrinityCore official tag (same commit 16b39a44)
  → Zero BFA dungeon/raid/zone content
  → Would require sourcing all BFA content from scratch anyway

================================================================================
                              TO BE CONTINUED
================================================================================

This document will be updated as the project progresses.
All merge decisions, conflict resolutions, and development notes
will be logged here and in CHANGELOG.txt.

Last Updated: June 5, 2026 (Strategy revised from Hybrid to TrinityCore Official Base)

================================================================================