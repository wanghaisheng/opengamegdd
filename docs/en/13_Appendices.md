# 13. Appendices

> Serves as an index and central repository for asset lists, glossaries, and KPI definitions.

## 13.1 Asset List

- **Maintenance:** Format (Spreadsheet / External Link / Asset Management System).
- **Fields:** ID, Name, Type, System, Path, Owner, Status.

### 13.1.1 Art

- **Model and Texture List:** Character meshes, environment props, and material maps.
- **Animation List:** Cycles for characters, objects, and UI.
- **Effects List:** VFX particles, shaders, and post-processing.
- **Interface Art List:** Icons, frames, buttons, and backgrounds.
- **Cutscene List:** Storyboards and assets for cinematic sequences.

### 13.1.2 Sound

- **Environmental Sounds:** Ambience, weather, and looping background tracks.
- **Weapon Sounds:** Fire, reload, impact, and handling foley.
- **Interface Sounds:** Clicks, hovers, confirms, and errors.

### 13.1.3 Music

- **Ambient:** Background tracks for exploration and safe zones.
- **Action:** High-intensity tracks for combat and chases.
- **Victory / Defeat:** Short stingers for round results.

### 13.1.4 Voice

- **Actor Lines:** Script breakdown by character.
- **Asset Table:** Organized by Character / Chapter / Language.

## 13.2 Glossary

- **Definitions:** Unified terminology for key game concepts.
- **Acronyms:** Standard abbreviations (e.g., FTUE, ARPDAU, DAU).
- **Goal:** Preventing misinterpretation across teams and regions.

## 13.3 KPI Definitions

> Precise definitions for metrics mentioned in Sections 3.9, 9.9, and 12.8.

- **Retention:** D1 / D7 / D30 calculation methods.
- **Monetization:** ARPU, ARPPU, ARPDAU, Conversion Rate formulas.
- **Engagement:** Participation rates, completion rates, and lift analysis.

## 13.4 External References

- **Competitor Analysis:** Links to market research and teardowns.
- **Internal Docs:** Post-mortems, sharing sessions, and technical wikis.
- **Platform Specs:** Documentation for Identity, Payment, Data, and Anti-cheat SDKs.

## 13.5 Asset Roadmap

- **Definition:** Converting asset lists into an actionable production schedule (Phases, Timeline, Dependencies, Milestones).
- **Core Steps:**
    - **Input:** Asset lists (Characters, Backgrounds, Props, VFX, Audio, UI).
    - **Phasing:** Concept → Modeling → Texturing → Animation → Testing → Release.
    - **Scheduling:** Gantt chart or Kanban, including 10–20% buffer and cross-team dependencies.
    - **Tools:** Excel/Google Sheets, GanttPRO, Miro.
- **Header Suggestions:**
    - ID, Category, Description, Quantity, Variant, Specs (Res/Poly), Priority, Dependency, Owner, Start/End Date, Status, Source (GDD Page/Storyboard).
- **Benefits:** Reduces delays and costs, improves collaboration efficiency.

### 13.5.1 Templates

- **CSV Template:** [asset_list_template.csv](GDDMarkdownTemplate/templates/asset_list_template.csv)
- **Markdown Template:** [asset_list_template.md](GDDMarkdownTemplate/templates/asset_list_template.md)
- **Metadata JSON Schema:** [asset_metadata_schema.json](GDDMarkdownTemplate/templates/asset_metadata_schema.json)

### 13.5.2 Specific Asset Templates

- **Gacha Animation Spec (MD):** [gacha_animation_spec.md](GDDMarkdownTemplate/templates/gacha_animation_spec.md)
- **Gacha Storyboard (MD):** [gacha_animation_storyboard.md](GDDMarkdownTemplate/templates/gacha_animation_storyboard.md)
- **Gacha Metadata Schema (JSON):** [gacha_animation_metadata_schema.json](GDDMarkdownTemplate/templates/gacha_animation_metadata_schema.json)

### 13.5.3 Video Asset Templates

- **Video Production Guide (MD):** [video_asset_guide.md](GDDMarkdownTemplate/templates/guides/video_asset_guide.md)
- **Video Storyboard (MD):** [video_storyboard_template.md](GDDMarkdownTemplate/templates/video_storyboard_template.md)
- **Video Metadata Schema (JSON):** [video_asset_metadata_schema.json](GDDMarkdownTemplate/templates/video_asset_metadata_schema.json)
- **Encoding Profiles (CSV):** [video_encoding_profiles.csv](GDDMarkdownTemplate/templates/video_encoding_profiles.csv)
- **Video Shot Breakdown (MD):** [storyboard_for_video_assets.md](GDDMarkdownTemplate/templates/guides/storyboard_for_video_assets.md)
- **API Video Generation Guide (MD):** [api_video_generation_guide.md](GDDMarkdownTemplate/templates/guides/api_video_generation_guide.md)
- **MVP Gameplay Video Guide (MD):** [mvp_gameplay_video_guide.md](GDDMarkdownTemplate/templates/guides/mvp_gameplay_video_guide.md)

### 13.5.4 Image Sequence Guide

- **Usage & Production (MD):** [image_sequence_guide.md](GDDMarkdownTemplate/templates/guides/image_sequence_guide.md)
- **Shot Breakdown (MD):** [storyboard_for_image_sequence_assets.md](GDDMarkdownTemplate/templates/guides/storyboard_for_image_sequence_assets.md)

### 13.5.5 Asset Extraction Guide

- **Extraction & Formatting (MD):** [asset_extraction_guide.md](GDDMarkdownTemplate/templates/guides/asset_extraction_guide.md)

### 13.5.6 Universal Storyboard Method

- **Methodology & Examples (MD):** [universal_storyboard_method.md](GDDMarkdownTemplate/templates/guides/universal_storyboard_method.md)

### 13.5.7 Format Production Guides

- **Image:** [image_asset_production_guide.md](GDDMarkdownTemplate/templates/guides/image_asset_production_guide.md)
- **Sprite Sheet:** [sprite_sheet_production_guide.md](GDDMarkdownTemplate/templates/guides/sprite_sheet_production_guide.md)
- **3D Model:** [3d_model_production_guide.md](GDDMarkdownTemplate/templates/guides/3d_model_production_guide.md)
- **Audio:** [audio_asset_production_guide.md](GDDMarkdownTemplate/templates/guides/audio_asset_production_guide.md)
- **Particles / VFX:** [fx_particle_production_guide.md](GDDMarkdownTemplate/templates/guides/fx_particle_production_guide.md)
- **UI Elements:** [ui_element_production_guide.md](GDDMarkdownTemplate/templates/guides/ui_element_production_guide.md)

### 13.5.8 VFX Discussion

- **Format & Mapping (MD):** [vfx_discussion.md](GDDMarkdownTemplate/templates/guides/vfx_discussion.md)

### 13.5.9 Playable Ad Guide

- **Playable Video Guide (MD):** [playable_ad_video_guide.md](GDDMarkdownTemplate/templates/guides/playable_ad_video_guide.md)

## 13.6 Common-language Mapping

- **Character (Actor):** Protagonist, Enemy, NPC; capable of movement and interaction.
- **Background (Set):** Forests, cities, rooms.
- **Prop (Object):** Weapons, furniture, interactive items.
- **Light (Source):** Torches, sunlight, shadow casters.
- **VFX (Visual Effects):** Explosions, fire, smoke.
- **Sound (Score/SFX):** BGM, footsteps, vocal cues.
- **Screen (Subtitle/HUD):** Health bars, menus, notifications.
- **Usage:** Facilitates communication between technical teams and non-specialists.

## 13.7 Advanced Templates & Checklists

> Detailed configuration tables and checklists for complex systems.

### 13.7.1 Economy & Monetization

- **Economy CSV Configs:**
    - Structure for items, pricing, sources, and sinks.
- **Monetization Checklist:**
    - Pre-launch verification (Price anchors, Confirmation flows, Sale tags).
- **Subscription Growth Checklist:**
    - LTV optimization items for subscription-based games.

### 13.7.2 VIP System Tables

- **VIP Level & Privilege Table:**
    - XP requirements and specific benefits per VIP tier.
