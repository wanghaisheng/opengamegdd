# 10. Game Art

> Define the overall visual direction, art style, and asset planning to provide a unified visual baseline for long-term updates.

## 10.1 Art Direction Overview

- **Style Tags:** Realistic, Cartoon, Low Poly, Pixel Art, etc.
- **References & Benchmarks:** Comparison with industry leaders (e.g., Genshin Impact, Tencent titles, Voodoo casual games).
- **Target Atmosphere:** Relaxing, Oppressive, Epic, Cute, etc.

## 10.2 Concept Art

- **World Concept:** Visualizing the setting and lore.
- **Key Locations:** Concepts for major cities, landmarks, and biomes.
- **Character & Enemy Design:** Primary cast and antagonist visualization.

## 10.3 Style Guides

- **Rules:** Unified standards for line work, silhouette, proportion, color palette, and lighting.
- **Consistency:** Ensuring 2D UI and 3D assets share a cohesive language.
- **Negative List:** Explicitly forbidden styles or elements to avoid.

## 10.4 Characters

- **Hierarchy:** Protagonists, Key NPCs, Enemies, Villagers.
- **Detail Standards:** Bone counts, polygon budgets, and texture resolution per tier.
- **Skins & Costumes:** Rules for the cosmetic system (critical for LiveOps and monetization).

## 10.5 Environments

- **Types:** Cities, Wilderness, Dungeons, Special Instances.
- **Tone:** Color grading and lighting mood for each area.
- **Modular Construction:** Strategy for Tiles, Modules, and Prefabs.

## 10.6 Equipment & Props

- **Rarity Visuals:** Distinguishing Common, Rare, and Legendary gear.
- **Functional vs. Cosmetic:** Visual differentiation between gameplay items and decorative props.

## 10.7 Cutscenes

- **Format:** Real-time 3D, 2D Animation, Motion Comic, Static Illustrations.
- **Specifications:** Storyboarding standards, subtitle sizing, and branding placement.

## 10.8 UI / UX Art

- **Style:** Flat, Skeuomorphic, Cartoon, Sci-Fi/Holographic.
- **Iconography:** System for main icons, sizing, and shape language.
- **Motion:** Button feedback, screen transitions, and loading indicators.

## 10.9 Technical Art Considerations

- **Shader Strategy:** Uber Shaders, VFX Shaders, Character Shading models.
- **VFX Budget:** Particle counts, overdraw limits, and post-processing costs.
- **Asset Standards:** Naming conventions, directory structure, and reference rules.

## 10.10 Asset Pipeline & Naming

- **General Naming Format:** `Prefix_Subject_Descriptor/Channel_Variant` (Avoid spaces/special chars, keep under 50 chars).
- **Prefix Examples:**
    - **Textures:** `T_` (e.g., `T_hero_body_D`, `T_hero_body_N`, `T_hero_body_RMA`)
    - **Static Meshes:** `SM_` (e.g., `SM_rifle_01`)
    - **Skeletal Meshes:** `SK_` (e.g., `SK_hero`)
    - **Materials / Instances:** `M_` / `MI_` (e.g., `M_hero_skin`, `MI_hero_skin_01`)
    - **Animations:** `ANM_` (e.g., `ANM_hero_run_01`)
    - **Audio:** `MX_` (Music), `SX_` (SFX) (e.g., `MX_theme_loop`, `SX_footstep_gravel_01`)
    - **Particles / VFX:** `PS_` (e.g., `PS_explosion`)
    - **UI Elements:** `UI_` (e.g., `UI_button_normal`)
    - **Lights:** `Light_` (e.g., `Light_lamp_P_01`)
- **Texture Channels:** `_D` (Diffuse), `_N` (Normal), `_R` (Roughness), `_AO` (Ambient Occlusion), `_M` (Metallic), or `_RMA` packed.
- **Versioning:** `_01`, `_A`, `LOD0`, `v001` (Maintain two-digit versioning).
- **Folder Structure:**
    - `Art/Characters/Hero/{Meshes, Textures, Materials, _wip}`
    - `Art/Weapons/Rifle/{Models, Textures}`
    - `Art/Environments/{Rocks, Trees}`
    - `Art/UI/{Sprites, Fonts}`
    - `Art/FX/Particles/`
    - `Audio/{SFX, Music, VO}`
    - `_Publish/` (Final exports only, no source files)
- **Metadata Tags:** JSON/XML for LOD, Platform, Usage, Author, Version, Dependencies (for search, packaging, and auditing).
- **Terminology Mapping:**
    - Character (Actor), Background (Set), Prop (Object), Light (Source), VFX (Visual Effects), Sound (Score/SFX), Screen (Subtitle/HUD).
- **Implementation:** Document upon project kickoff; batch rename scripts; CI/CD validation for naming and metadata.

### Asset Formats

- **3D Model (`3d_model`):** SM/SK geometry and bone data.
- **Image (`image`):** Single-frame textures, maps, or UI images.
- **Image Sequence (`image_sequence`):** Frame-based image series (PNG/JPG/TGA) for animation/VFX; distinct from video containers.
- **Sprite Sheet (`sprite_sheet`):** Combined texture atlas with index data, for UI/2D animation.
- **Video (`video`):** Containerized media (MP4/H.264/H.265/WEBM) for cutscenes or showcases.
- **Audio (`audio`):** BGM, SFX, VO.
- **Other:** Shader, Material, Font, Prefab, Level, Particle System, UI Element.

- **Guide:** [image_sequence_guide.md](GDDMarkdownTemplate/templates/image_sequence_guide.md)

### Format Selection & Naming Points

- **Video:** Unified high-quality playback. Example: `VID_Cutscene_Chapter1_v001.mp4`.
- **Image Sequence:** Controllable animation/VFX. Example: `SEQ_GachaReveal_0001.png` (4-digit padding).
- **Sprite Sheet:** UI/2D Animation. Example: `SPR_UI_ButtonPress_atlas_v001.png` (with index file).
- **Image:** Textures. Example: `T_hero_body_RMA.tga` (Suffix rules apply).
- **Particles / VFX:** Example: `PS_fire_small_loop`, `PS_explosion_heavy`.
- **Audio:** Example: `MX_theme_loop.ogg`, `SX_footstep_gravel_01.wav`, `VO_hero_intro_en.mp3`.

### Selection Advice

- **Interactive & Controllable Camera:** Prioritize `3d_model` + `image` + `fx_particle` (Real-time).
- **Unified Presentation, Weak Interaction:** Use `video` with multi-platform adaptation.
- **High Volume 2D/UI Animation:** Prioritize `sprite_sheet`; use `image_sequence` for complex shots or heavy VFX.
