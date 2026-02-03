# 8. Artificial Intelligence

> Describe the behavioral logic of enemies, allies, and NPCs, as well as their relationship with difficulty, performance, and anti-cheat measures.

## 8.1 Opponent / Enemy AI

### 8.1.1 AI Taxonomy

- **Types:** Patrol, Assault, Defensive, Ranged, Summoner, etc.
- **Boss & Elite AI:** Unique mechanisms and phase transitions.

### 8.1.2 Perception & State

- **Perception System:** Sight cones, hearing radius, and threat generation.
- **State Machine:**
    - **Required:** State Transition Diagram (Idle → Alert → Chase → Combat → Flee).

### 8.1.3 Behavior Logic

- **Architecture:** Selection of Behavior Trees, GOAP, or Scripted Logic (**Behavior Trees recommended for complex AI**).
- **Decision Frequency:** Update rates and performance budgeting.
- **Difficulty Scaling:** Impact on behavior (smarter tactics vs. just higher stats).

### 8.1.4 Group AI

- **Coordination:** Flanking, covering fire, and role distribution.
- **Aggro Management:** Threat distribution and token-based attack slots.

## 8.2 Non-combat Characters

- **Ambient NPC Schedules:** Daily routines, patrol paths, and interaction nodes.
- **Service NPCs:** Interaction flows for Merchants, Quest Givers, and Function NPCs.
- **Atmospheric NPCs:** Crowd density and background behaviors to enliven the world.

## 8.3 Friendly Characters & Companions

- **Roles:** DPS, Healer, Tank, Buffer.
- **Follow Logic:** Distance maintenance and pathing relative to the player.
- **Synergy:** Combo triggers and elemental reactions with player actions.

## 8.4 Support AI

### 8.4.1 Player and Collision Detection

- **Colliders:** Hitboxes, hurtboxes, and physics layers.
- **Tolerance:** "Coyote time," edge correction, and forgiving hit detection.

### 8.4.2 Pathfinding

- **Algorithm:** NavMesh, Grid-based, or Waypoints.
- **Complex Geometry:** Handling destructible environments, verticality, and dynamic obstacles.
- **Authority:** Division of responsibility between Client (prediction) and Server (validation).

## 8.5 Difficulty & Adaptivity

- **Modes:** Design philosophy for Normal, Hard, Nightmare, etc.
- **Dynamic Difficulty Adjustment (DDA):** Scaling enemy strength/count based on player performance.
- **Balancing:** Safety nets for new players vs. skill ceilings for veterans.

## 8.6 Performance & Anti-cheat Considerations

- **Budget:** Maximum active AI agents per frame and tick rate limits.
- **Server Authority:** Critical states and outcomes validated server-side.
- **Trust Model:** Defining what data the client can see vs. what it can influence.
