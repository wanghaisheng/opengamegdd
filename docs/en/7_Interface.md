# 7. Interface

> Define the tangible layer between the player and the game: HUD, menus, input methods, and feedback.

## 7.1 Visual System

### 7.1.1 HUD (Heads-Up Display)

- **Core Information:** HP, Energy, Skills, Resources, Timers, etc.
- **Layout & Hierarchy:** Prioritizing information near the center of vision vs. peripheral details.
- **Dynamic Feedback:** Hit markers, crit indicators, healing numbers, and status changes.

### 7.1.2 Menus

- **Main Menu Structure:** Functional grouping (Inventory, Character, Quest, Events, Shop).
- **Information Architecture:** Sub-menu depth and navigation flow.
- **Status Indicators:** Red dots (notifications), "NEW" tags, and time-limited markers.

### 7.1.3 Rendering System

- **Perspective:** First-person, Third-person, Top-down, and camera principles.
- **VFX Priority:** Performance budgeting for low-end vs. high-end devices.
- **Settings Impact:** Aspect ratio support and adaptive UI layout.

### 7.1.4 Camera

- **Follow Rules:** Distance, smoothing, and collision handling.
- **Special Cameras:** Target lock-on, cutscene angles, and interaction transitions.
- **Motion Sickness Prevention:** Field of View (FOV) settings and camera shake limits.

### 7.1.5 Lighting Models

- **Art Style:** Realistic, Cartoon/Cel-shaded, High Contrast, etc.
- **Dynamic Lighting:** Day/night cycles and real-time shadows (if applicable).
- **Interactive Lighting:** Visual cues and guidance lights.

## 7.2 Control System

- **Input Devices:** Touchscreen, Keyboard & Mouse, Gamepad, Gyroscope.
- **Mapping:** Movement, Attack, Interact, Jump, Skills.
- **Advanced Mechanics:** Combos, Animation Canceling, Macro restrictions.
- **Onboarding:** Gesture guidance and error tolerance for new players.

## 7.3 Audio

- **Mixing Principles:** Prioritization (Voice > BGM > SFX).
- **Contextual Layering:** Combat, Town, Field, Main Menu.
- **Dynamic Mixing:** Ducking rules (e.g., lowering ambient noise during key dialogue).

## 7.4 Music

- **Theme:** Main theme and leitmotifs.
- **Contextual Scores:** Regional tracks, Combat themes, Boss music, Resting tunes.
- **Event Integration:** Special tracks for seasonal events or updates.

## 7.5 Sound Effects (SFX)

- **Interaction SFX:** Click, Swipe, Confirm, Cancel.
- **Combat SFX:** Attack, Hit, Skill cast, Explosion.
- **Feedback Hierarchy:** Success, Failure, Warning, Reward.

## 7.6 Help System

- **Tutorials:** Forced guidance steps vs. free-roam hints.
- **In-Game Help:** Tooltips, "Long-press" info, and illustrated guides.
- **Update Education:** Highlighting new features and tutorial levels for patches.

## 7.7 Accessibility & Localization

- **Visual Aids:** Font size scaling, contrast modes, colorblind support.
- **Text Alternatives:** Subtitles and logs for voice content.
- **Localization:** Text expansion handling, reading direction (RTL/LTR), and cultural formatting.

## 7.8 Screen Storyboard Method

- **Goal:** Merge UI descriptions with storyboard techniques to unify state, transition, and interaction documentation.
- **Process:**
    - Define "Screen States" (Initial, Hover, Click, Animating, Loading, End).
    - Record details per "Shot": Focus, UI Components, Interaction, Feedback, Audio, Accessibility, Transition, Performance, and Analytics.
- **Recommended Fields:**
    - Screen/State, Shot/Time, Camera/Focus, UI Components, Interaction/Gesture, Feedback (Visual/Audio), Accessibility/Localization, Transition/Sequence, Performance Budget, Analytics Events.
- **Templates & Guides:**
    - Guide: [interface_screen_storyboard_guide.md](GDDMarkdownTemplate/templates/interface_screen_storyboard_guide.md)
    - Template: [interface_screen_storyboard_template.md](GDDMarkdownTemplate/templates/interface_screen_storyboard_template.md)

## 7.9 UX Design Philosophy

> Beyond functional UI, focus on the psychological motivation behind player interaction.

- **Curiosity-Driven Design:**
    - Using unknown UI elements (e.g., silhouettes) to trigger exploration.
- **Self-Narrative:**
    - Reflecting player growth in the interface (e.g., evolving main menu backgrounds, avatar frames).
- **Feedback Juiciness:**
    - Ensuring every interaction provides satisfying visual, auditory, or haptic feedback.

## 7.10 Onboarding & Paywall Flows

- **Onboarding Flow (FTUE):**
    - First Time User Experience flowchart.
    - Timing of key "Aha Moments."
- **Paywall Design:**
    - **Trigger Timing:** Presenting offers at the moment of highest need.
    - **Value Proposition:** Clearly communicating "Why is this worth it?"
    - **Psychology:** Anchoring effects, social proof, and urgency.
