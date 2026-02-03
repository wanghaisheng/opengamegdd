# 6. Levels

> Define the player experience across spatial and temporal dimensions, from overall content structure to individual level details.

## 6.1 Level Taxonomy

- **Main Story Levels:** Core narrative progression stages.
- **Side / Commission Levels:** Optional quests for resources or world-building.
- **Tutorial / Onboarding Levels:** Introductory stages for new mechanics.
- **High-Difficulty / Endgame Content:** (e.g., Abyss, Tower Climbing, Arena).
- **Event Levels:** Limited-time content associated with seasonal events.

## 6.2 World / Map Structure

- **Organization:** How the world is divided (Open World, Chapters, Hubs).
- **Unlocking Logic:** Prerequisites and recommended progression paths.
- **Traversal:** Fast travel points, waypoints, and movement mechanics.

## 6.3 Level Progression

- **Flowchart:** Sequence of level unlocking (dependencies and branching).
- **Difficulty Curve:** Rules for escalating challenge (enemy strength, mechanical complexity, resource pressure).
- **Mechanic Introduction:** Pacing for introducing new gameplay elements (tutorial → practice → mastery).

## 6.4 Level Template

> Use this structure for Level #1, #2, etc., to ensure consistency across the team.

### 6.4.1 Level #1 – Basic Info

- **Level ID:** Unique identifier.
- **Level Name:** Display name.
- **Type:** (Main, Side, Tutorial, Event).
- **Recommended Power / Level:** Required stats or level range.

### 6.4.2 Synopsis

- **Role:** (e.g., Teaching mechanics, Narrative climax, Resource farming).
- **Narrative Context:** Where this level fits within the story chapter.

### 6.4.3 Introductory Material

- **Opening:** Dialogue, cutscene, or comic-style intro.
- **Briefing:** Objective text and necessary hints.

### 6.4.4 Objectives

- **Primary Objective:** Mandatory condition for success.
- **Secondary Objectives:** Optional goals for extra rewards.
- **Hidden Objectives:** Easter eggs or advanced challenges.

### 6.4.5 Physical Description

- **Topology:** Layout zones, critical paths, side paths, and dead ends.
- **Verticality:** Elevation changes, platforms, and jump routes.

### 6.4.6 Map

- **Layout:** Schematic or link to the map file.
- **Markers:** Spawn points, objectives, key items, and interactive objects.

### 6.4.7 Critical Path

- **Walkthrough:** The most common path players will take.
- **Choke Points:** Potential difficulty spikes and mitigation strategies (detours, hints, failsafes).

### 6.4.8 Encounters

- **Waves:** Enemy configuration and spawn logic.
- **Elites / Bosses:** Key mechanics and behaviors.
- **Environmental Hazards:** Traps, terrain effects, and interactive dangers.

### 6.4.9 Level Walkthrough

- **Player Perspective:** Step-by-step description of the experience.
- **Feedback:** Audio-visual cues and numerical feedback at key moments.

### 6.4.10 Closing Material

- **Settlement:** Scoring, rewards, and performance statistics.
- **Outro:** Dialogue, cutscene, or teaser for the next level.

> Duplicate this structure for Level #2, #3, etc.

### 6.4.11 Numerical & Economy Budget

- **Enemy Budget:** Stats, expected damage output, and time-to-kill (TTK).
- **Player Targets:** Expected power range and pass rate for different player segments (Casual / Mid-core / Hardcore).
- **Resource Output:** Expected yield and variance for currencies, materials, and XP.
- **Reward Structure:** Tiered rewards for Primary / Secondary / Hidden objectives.
- **Time & Cost:** Estimated playtime and stamina/resource consumption (aligned with Economic System).
- **Exploit Prevention:** Safeguards against AFK farming, kiting, or skipping content.

### 6.4.12 System Hooks

- **Quest System:** Completion triggers, quest chain progression, daily/weekly task updates.
- **Gameplay System:** Tutorial triggers, difficulty scaling, event reporting.
- **Progression System:** Recommended growth goals, breakthrough material drops.
- **Monetization:** Non-intrusive entry points for acceleration or direct purchase (e.g., revive, stamina refill).
- **Telemetry:** Entry/Exit logs, duration, failure reasons, resource flow, and feature usage.
