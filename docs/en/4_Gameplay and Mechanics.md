# 4. Gameplay and Mechanics

> Define exactly what players can do, how they do it, and how the system responds to their actions.

## 4.1 Gameplay

### 4.1.1 Game Progression

- **Main Progression Path:** (Chapters / Map Exploration / Level Unlocking / Star Rating, etc.)
- **Player Lifecycle Stages:** (Newbie → Growth → Maturity / Competitive)
- **Content Unlock Pacing:** (Daily / Weekly / Version updates)

### 4.1.2 Mission / Challenge Structure

#### 4.1.2.1 Mission System Architecture [Weight: 4%]

##### Mission Classification System
- **Main Quests**
  - Chapter Progression: Story unlock, stage goals, key nodes
  - Tutorial Missions: Learning objectives, control guidance, system introduction
- **Side Quests**
  - Character Quests: NPC background, relationship building, reward unlock
  - Area Quests: Map exploration, resource collection, area cleanup
- **Daily Missions**
  - Grinding Missions: Material collection, monster hunting, dungeon challenges
  - Activity Missions: Login rewards, online time, social interaction
- **Weekly/Monthly Missions**
  - Growth Missions: Level breakthrough, power improvement, system unlock
  - Limited-time Events: Holiday events, version events, special challenges

##### Mission Logic Evaluation Checklist
- [ ] **Mission Chain Integrity**: Logical relationships and dependencies between missions
- [ ] **Objective Achievability**: Feasibility and difficulty curve of mission objectives
- [ ] **Reward Reasonableness**: Match between mission rewards and difficulty investment
- [ ] **Trigger Conditions**: Pre-conditions and timing design for mission triggers
- [ ] **Completion Validation**: Detection mechanism for mission completion status

#### 4.1.2.2 Mission Design Template

##### Mission Basic Information
```
Mission ID: QUEST_[TYPE]_[CHAPTER]_[NUMBER]
Mission Name: [English Name]/[Local Name]
Mission Type: [Main/Side/Daily/Weekly]
Mission Level: [MinLevel] - [MaxLevel]
Estimated Duration: [Minutes] minutes
Repeat Cycle: [One-time/Daily/Weekly/Monthly]
```

##### Mission Logic Flow
```
Trigger Condition → Mission Accept → Objective List → Progress Tracking → Completion Validation → Reward Distribution
        ↓                  ↓              ↓                ↓                    ↓                    ↓
[Level/Story] [NPC Dialogue] [Kill/Gather] [Counter/UI] [CheckAll] [Item/Exp]
```

##### Objective Type Definitions
- **Elimination Type**: Kill [Target] × [Count]/[Total]
- **Collection Type**: Gather [Item] × [Count]/[Total]
- **Escort Type**: Escort [NPC] to [Location] within [Time]
- **Interaction Type**: Interact with [Object] × [Count]
- **Exploration Type**: Discover [Area] × [Count]/[Total]

#### 4.1.2.3 Mission Balance Validation

##### Quantitative Evaluation Metrics
- **Completion Rate Analysis**: Target completion rate should be 70%-95%
- **Duration Match**: Actual completion duration deviation from estimated < 20%
- **Difficulty Curve**: Mission difficulty should match player growth curve
- **Reward Value**: Cost-performance ratio of reward value and mission investment

##### Mission Chain Logic Validation
```
Mission A → Mission B → Mission C
    ↓        ↓        ↓
[Unlock] [Prerequisite] [Result]
```

##### Test Case Design
- **Tutorial Test**: Can new players complete tutorial missions smoothly
- **Difficulty Test**: Mission completion experience for target level players
- **Boundary Test**: Mission status handling under extreme conditions
- **Concurrency Test**: Logic handling of multiple simultaneous missions

#### 4.1.2.4 Mission Automated Generation

##### LiveOps Mission Templates
```
Daily Mission Template:
- Condition: Player level ≥ [Level]
- Objective: [Action] [Target] × [Count]
- Reward: [RewardType] × [Amount]
- Refresh: Reset daily at [Time]

Event Mission Template:
- Period: [StartDate] - [EndDate]
- Condition: Event participation ≥ [Percent]%
- Objective: Cumulative completion [MissionType] × [Count]
- Reward: [ExclusiveReward] × [Amount]
```

##### Mission Generation Algorithms
- **Weight Allocation**: Adjust mission type weights based on player behavior data
- **Difficulty Adaptation**: Dynamically adjust mission difficulty based on player power
- **Reward Personalization**: Customize reward content based on player needs and preferences

- **Mission Types:** (Main / Side / Daily / Weekly / Event Missions)
- **Mission Templates:** (Objectives: Collect, Kill, Escort, Race, Puzzle, etc.)
- **Difficulty & Reward Tiering:**
- **Automated Generation Rules:** (For long-term LiveOps content delivery)

### 4.1.3 Puzzle Structure (If Applicable)

- **Core Puzzle Mechanics:**
- **Difficulty Curve:**
- **Tolerance & Hint System:** (To prevent blockers)

### 4.1.4 Objectives

- **Short-term Objectives:** (Per session / Per login)
- **Mid-term Objectives:** (Days / Weeks)
- **Long-term Objectives:** (Character growth, Collection, Leaderboards, Achievements)
- **Alignment with Business & LiveOps Goals:**

### 4.1.5 Play Flow

- **Session Flow:** (Entry → Prep → Gameplay → Settlement)
- **Round / Wave Structure:** (For Tower Defense, Roguelike, etc.)
- **Interruption & Resume:** (Reconnection, Pause, Offline Rewards)

### 4.1.6 Core Thrill Loop vs Meta Loop

- **Core Thrill Loop:**
    - Describe the micro-level "Action-Feedback" high-frequency loop (e.g., Aim-Shoot-Headshot Feedback).
    - Define "Dopamine" release points and pacing.
- **Meta Loop:**
    - Describe the macro-level resource accumulation and growth loop.
    - How does the Core Loop drive the Meta Loop? How does the Meta Loop feed back into the Core Loop?

## 4.2 Mechanics

### 4.2.1 World Rules & Physics

#### Global Rules
- **Time System:** (Day/Night cycle, Time scale)
- **Environmental Rules:** (Weather, Terrain effects, Gravity changes)
- **Scale & Measurements:** (Scale ratio and measurement units)

#### Physics Details
- **Basics:** Gravity, Collision, Friction settings.
- **Key Interactions:** Bouncing, Destruction, Projectiles, etc.
- **Performance & Cheat Prevention:** (e.g., Server-side validation)

### 4.2.2 Movement

#### General Movement

- **Movement Modes:** (Walk / Run / Jump / Roll / Dash / Fly, etc.)
- **Speed & Acceleration Rules:**
- **Stamina / Resource Consumption & Recovery:**

#### Other Movement

- **Special Moves:** (Climb / Glide / Grapple / Teleport)
- **Interaction with Level Design:**

### 4.2.3 Objects

#### Picking Up Objects

- **Pickable Types:** (Items, Resources, Equipment)
- **Pickup Range, Auto-pickup Rules & Animation Feedback:**

#### Moving Objects

- **Movable Rules:** (Boxes, Mechanisms, Vehicles)
- **Collision & Blocking Logic:**

### 4.2.4 Actions

#### Switches and Buttons

- **Trigger Conditions:** (Step, Attack, Interact, Remote trigger)
- **States:** (One-time / Resettable / Timer)

#### Picking Up, Carrying and Dropping

- **Carrying Limits:** (Weight, Quantity, Stamina cost)
- **Throwing Rules:** (Parabola, Hit detection)

#### Talking & Reading

- **Interaction Range & Trigger:**
- **UI Presentation:** (Bubble / Dialogue Box / Full Screen)
- **Skipping & Log History:**

### 4.2.5 Combat

#### 4.2.5.1 Skill System Architecture [Weight: 4%]

##### Skill Classification System
- **Active Skills**
  - Instant Skills: Cast logic, target selection, projectile calculation
  - Channel Skills: Channel mechanism, resource consumption, interruption conditions
  - Charge Skills: Charge phases, damage multipliers, interruption risk
- **Passive Skills**
  - Permanent Effects: Attribute bonuses, trigger conditions, numerical algorithms
  - Conditional Triggers: Event listening, trigger probability, cooldown mechanisms
- **Combo Skills**
  - Chain Logic: Pre-conditions, combo multipliers, combination limits
  - Synergy Mechanisms: Character coordination, position requirements, timing windows

##### Skill Logic Evaluation Checklist
- [ ] **Skill Chain Integrity**: Complete logic chain from input to output for each skill
- [ ] **Condition Consistency**: Logical self-consistency between trigger conditions and effect performance
- [ ] **Numerical Reasonableness**: Balance of damage multipliers, cooldown times, resource consumption
- [ ] **Interaction Logic**: Interactions and conflict resolution between skills
- [ ] **Boundary Cases**: Skill behavior definition under extreme scenarios

#### 4.2.5.2 Skill Design Template

##### Skill Basic Information
```
Skill ID: SKILL_[TYPE]_[NUMBER]
Skill Name: [English Name]/[Local Name]
Skill Type: [Active/Passive/Combo]
Target Type: [Self/Single/Group/Area]
Cast Range: [Melee/Ranged/Full Screen]
```

##### Logic Flow Chart
```
Input Detection → Condition Validation → Resource Check → Animation Play → Effect Calculation → Result Application → Cooldown Start
        ↓                  ↓                  ↓              ↓                ↓                  ↓                ↓
[Button/Trigger] [Status/Range] [MP/CD]      [Action/VFX] [Damage/Buff] [HP Change] [Timer]
```

##### Numerical Formula Definitions
- **Damage Formula**: BaseDamage × (1 + StatBonus) × (1 + ComboBonus) × (1 + ElementBonus) - Defense
- **Heal Formula**: BaseHeal × (1 + HealPower) × (1 + TargetHealReceived)
- **Status Effect**: Duration = BaseDuration × (1 + EffectDuration), Stack = min(CurrentStack + 1, MaxStack)

#### 4.2.5.3 Skill Balance Validation

##### Quantitative Evaluation Metrics
- **DPS Evaluation**: Theoretical DPS vs actual DPS deviation < 15%
- **Utility Value**: Equivalent damage conversion for non-damage skills
- **Risk Assessment**: Risk-cost matching for high-reward skills
- **Diversity Validation**: Differentiation degree > 30% for same skill types

##### Test Case Design
- **Basic Function Test**: Single skill performance under ideal conditions
- **Combination Test**: Synergistic effects of multiple skill combinations
- **Opposition Test**: Skill balance in PvP environment
- **Boundary Test**: System stability under extreme numerical values

#### 4.2.5.4 Skill Iteration Process

##### Version Records
| Version | Changes | Logic Score | Test Results | Approval Status |
|---------|----------|-------------|--------------|-----------------|
| v1.0 | Initial Design | 85/100 | Passed Test | Approved |
| v1.1 | Adjust Multipliers | 92/100 | Balance Optimized | Live |

##### Logic Scoring Standards
- **90-100 points**: Logic completely self-consistent, no conflicts, full boundary case coverage
- **80-89 points**: Logic basically self-consistent, minor optimization space
- **70-79 points**: Logic has minor issues, needs adjustment
- **60-69 points**: Logic has obvious conflicts, needs redesign
- **<60 points**: Logic has serious defects, not recommended

### 4.2.6 Economy

#### Currency & Resources

- **Soft/Hard Currency Structure:** (Gold, Diamonds, Tokens, etc.)
- **Resource Classification:** (Growth resources, Stamina, Materials, Collectibles, etc.)

#### Sources & Sinks

- **Resource Sources:** (Combat, Missions, Events, Ad rewards, Shop, etc.)
- **Resource Sinks:** (Upgrades, Gacha, Enhancement, Refresh, Acceleration, etc.)
- **Daily/Weekly Resource Budget:** (Using major company "resource budget table" approach)

#### Monetization Design

#### 4.2.6.4 Business System Architecture [Weight: 3%]

##### Monetization Classification System
- **Direct Purchase**
  - Permanent Items: One-time purchase of characters, weapons, skins
  - Limited Bundles: Limited-time, limited-quantity discounted packages
  - Feature Unlock: Paid unlock of in-game features
- **Subscription**
  - Monthly/Seasonal Cards: Regular payments for continuous benefits
  - Battle Pass: Paid acceleration of reward acquisition through gameplay
  - VIP Privileges: Tiered payments for exclusive benefits
- **Randomized Payment**
  - Gacha System: Random acquisition of characters, equipment
  - Loot Box System: Random opening of items
  - Lottery Mechanism: Low-probability, high-value incentive mechanism
- **Advertisement Monetization**
  - Rewarded Video: Active viewing for rewards
  - Interstitial Ads: Forced ad displays
  - Cross-promotion: Promotion of other games

##### Business Logic Evaluation Checklist
- [ ] **Payment Logic**: Reasonable combination of payment points and game experience
- [ ] **Value Balance**: Balance between paid and free content
- [ ] **Revenue Model**: Balance between long-term and short-term revenue
- [ ] **Compliance**: Compliance with regional laws and regulations
- [ ] **Addiction Prevention**: Minor protection and addiction prevention mechanisms

#### 4.2.6.5 Payment Design Template

##### Product Basic Information
```
Product ID: PRODUCT_[TYPE]_[NUMBER]
Product Name: [English Name]/[Local Name]
Product Type: [Direct Purchase/Subscription/Gacha/Ad]
Product Price: [Currency] [Amount]
Product Description: [Function Description/Value Description]
Sales Restrictions: [Time Limit/Quantity Limit/Level Limit]
```

##### Payment Point Design Logic
```
Need Identification → Value Presentation → Payment Guidance → Payment Process → Benefit Distribution → Follow-up Service
        ↓                  ↓                  ↓                  ↓                  ↓                  ↓
[Pain Point] [Value Packaging] [UI Guidance] [Payment Interface] [Delivery Confirmation] [Customer Service]
```

#### 4.2.6.6 Economic Balance Validation

##### Quantitative Evaluation Metrics
- **Payment Rate**: Paying users / Active users, target 5-15%
- **ARPU**: Average revenue per user, compared to category benchmarks
- **ARPPU**: Average revenue per paying user, controlled within reasonable range
- **LTV**: User lifetime value, greater than 3x CAC
- **Payment Penetration**: Reasonable distribution of users across payment tiers

### 4.2.7 Numerical Design

#### 4.2.7.1 Numerical System Architecture [Weight: 4%]

##### Numerical Classification System
- **Base Attributes**
  - Survival Attributes: HP, Defense, Toughness, Resistance
  - Output Attributes: Attack, Critical Hit, Hit Rate, Penetration
  - Functional Attributes: Speed, Range, Duration, Cooldown Reduction
- **Derived Attributes**
  - Power Score: Comprehensive strength evaluation value
  - Survival Score: HP × (1 + Defense Coefficient) × Toughness Coefficient
  - Output Score: Attack × (1 + Critical Rate × Critical Damage) × Hit Rate
- **Resource Values**
  - Currency System: Exchange ratios between gold, diamonds, tokens
  - Material Value: Equivalent value conversion of various training materials
  - Time Cost: Time value assessment of stamina, energy

##### Numerical Logic Evaluation Checklist
- [ ] **Formula Consistency**: Logical self-consistency of all numerical calculation formulas
- [ ] **Growth Reasonableness**: Smoothness and reasonableness of numerical growth curves
- [ ] **Balance Validation**: Balance relationships between different numerical values
- [ ] **Boundary Control**: Reasonable setting of numerical upper and lower limits
- [ ] **Inflation Control**: Prevention of numerical inflation in long-term operations

#### 4.2.7.2 Core Numerical Formulas

##### Combat Formula System
```
Damage Calculation Formula:
FinalDamage = BaseDamage × (1 + AttackBonus) × (1 + CriticalDamage) × ElementBonus 
             - TargetDefense × (1 - ArmorPenetration) × (1 - Resistance)

Heal Calculation Formula:
FinalHeal = BaseHeal × (1 + HealPower) × (1 + TargetHealReceived) 
           × (1 - HealReduction)

Status Effect Formula:
StatusDamage = BaseStatusDamage × StackCount × Duration 
               × (1 + StatusAmplification)
```

##### Growth Formula System
```
Level Experience Formula:
ExpNeeded = BaseExp × (Level ^ GrowthFactor) × ExpMultiplier

Attribute Growth Formula:
FinalStat = BaseStat + (Level × GrowthPerLevel) 
            + EquipmentBonus + BuffBonus

Power Calculation Formula:
PowerScore = HP_Weight × HP + Attack_Weight × Attack 
            + Defense_Weight × Defense + Skill_Weight × SkillPower
```

#### 4.2.7.3 Numerical Balance Validation

##### Quantitative Evaluation Metrics
- **DPS Balance**: Same-level character DPS difference < 15%
- **Survival Balance**: Same-level character survival ability difference < 20%
- **Growth Balance**: Smoothness of numerical growth curves at all levels > 90%
- **Economic Balance**: Resource production-consumption ratio controlled between 0.8-1.2

##### Numerical Simulation Testing
```
Simulation Scenario Design:
- 1v1 Combat Simulation: 1000 battles, win rate distribution
- Team Combat Simulation: 5v5 standard configuration, balance testing
- Dungeon Challenge Simulation: Different configuration completion rates
- Long-term Growth Simulation: 1-3 month numerical development trajectory
```

#### 4.2.7.4 Numerical Table Design

##### Standard Numerical Table Template
```
Character Stats Table:
| Level | HP | Attack | Defense | Speed | CritRate | CritDamage | Power |
|-------|----|---------|---------|-------|----------|------------|-------|
| 1     | 100| 50      | 30      | 100   | 5%       | 150%       | 1000  |
| 2     | 110| 55      | 33      | 102   | 5.5%     | 152%       | 1150  |
| ...   | ...| ...     | ...     | ...   | ...      | ...        | ...   |

Equipment Stats Table:
| ItemID | ItemName | Level | MainStat | SubStats | Cost | SellPrice |
|--------|----------|-------|----------|----------|------|-----------|
| WEAP001| Iron Sword| 1     | Attack+20| Crit+5%  | 100  | 50        |
| ...    | ...      | ...   | ...      | ...      | ...  | ...       |
```

##### Numerical Validation Rules
- **Incremental Validation**: All level numerical values must be incremental
- **Proportional Validation**: Reasonable proportional relationships between attributes
- **Boundary Validation**: Numerical values do not exceed preset upper and lower limits
- **Consistency Validation**: Cross-table data consistency
