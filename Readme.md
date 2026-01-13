# Implementation Plan - THE EXIT 8 LOOP

## Goal Description
Create a psychological horror walking simulator inspired by "The Exit 8". The player traverses a looping hallway, spotting anomalies to decide whether to continue forward or turn back. The goal is to reach Level 8.

## Completed Features

### 1. Core Game Loop
- [x] **Infinite Hallway Mechanic**: Seamless teleportation to create an illusion of an infinite loop.
- [x] **Physics & Movement**: WASD controls, Pointer Lock, Head bob, and Collision detection with walls/objects.
- [x] **Progression System**:
    - [x] Detect "Turn Back" vs "Keep Going".
    - [x] Increment Level on correct decision.
    - [x] Reset to Level 0 on fail.
    - [x] Win condition at Level 8.

### 2. Audio Engine (Psychological Horror)
- [x] **Procedural Ambience**: "The Hum" - Pink Noise (Air) + Sub-bass Sine (Pressure).
- [x] **Natural Footsteps**: Hybrid synthesis (Sine Low-End for weight + Lowpass Filtered Noise for concrete contact).
- [x] **Breathing**: Procedural bandpass wind sound that reacts to running/stress.
- [x] **Feedback SFX**:
    - [x] **Success**: Subtle low-frequency thrum.
    - [x] **Fail**: Sudden static burst.
    - [x] **Jumpscares**: High-gain audio bursts (LoudBang).

### 3. Visuals & Atmosphere
- [x] **Graphical Style**: Three.js, Dark/Gritty lighting, Spotlights, Fog.
- [x] **Post-Processing**: Vignette overlay (CSS), Glitch effects (Title), Camera Trauma (Shake).
- [x] **Props**: Vending Machines, Trash Bags, Ceiling Vents/Pipes (Deterministic placement).
- [x] **UI**: Analog Horror style Main Menu, Pause Menu (ESC), Phone interface.

### 4. Anomaly System
**Tier 1: Subtle**
- [x] `MissingSign` (Visual)
- [x] `DimmedLight` (Lighting)
- [x] `ExtraTrash` (Prop)
- [x] `ColorShift` (Atmosphere)
- [x] `SoundDelay` (Audio)

**Tier 2: Noticeable**
- [x] `MovedObject` (Prop)
- [x] `LightFlicker` (Lighting)
- [x] `ReflectionsWrong` (Material)
- [x] `AmbientDrop` (Audio)

**Tier 3: Unsettling**
- [x] `DuplicateObject` (Prop)
- [x] `WrongTexture` (Material)
- [x] `ScaleDrift` (Camera/FOV)
- [x] `StreetShortened` (Geometry)
- [x] `AudioMismatch` (Audio)
- [x] `Mannequin` (Visual Horror)

**Tier 4: Active Threat / Meta**
- [x] `PhoneGlitch` (UI/Narrative)
- [x] `LightAvoidance` (Interactive)
- [x] `StreetBreathes` (World warping)
- [x] `FalseNormal` (Meta - No anomaly but paranoia)
- [x] `LoudBang` (Audio Jumpscare)

**Tier 5: Jumpscare**
- [x] `FaceFlash` (Screen Overlay)

### 5. Mechanics & Polish
- [x] **Smartphone Tool**:
    - [x] **Lore**: SMS messages from "The Operator" revealing the story (Subject #429).
    - [x] **Flashlight**: Toggle light with Spacebar to inspect dark areas.
    - [x] **Haptics**: Audio buzz on new message.
    - [x] **Unlock**: Available from Level 3 onwards.
- [x] **Map Design**:
    - [x] Extended length (53 units).
    - [x] Deterministic prop generation (Fixed pattern for "Normal" state).

## Technical Stack
- **Engine**: Three.js (r128)
- **Audio**: Web Audio API (Tone generation & Filtering)
- **Language**: Vanilla JavaScript / HTML5
