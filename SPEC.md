# WWII Beach Landing - 2D Arcade Game Specification

## 1. Project Overview
- **Project Name**: D-Day Rush
- **Type**: 2D Side-scrolling Arcade Shooter
- **Core Functionality**: Player controls a WWII soldier running across Omaha Beach, dodging enemy fire while progressing forward
- **Target Users**: Casual gamers seeking quick, action-packed arcade experience

## 2. Visual & Rendering Specification

### Scene Setup
- **View**: 2D side-scrolling, camera follows player horizontally
- **Background Layers** (parallax):
  - Far: Gray sky with smoke/dust
  - Mid: Ocean waves, distant explosions
  - Near: Beach sand, obstacles, debris

### Color Palette
- **Primary**: Sandy beige (#C4A35A), Ocean blue (#4A6FA5)
- **Accent**: Muzzle flash orange (#FF6B35), Blood red (#8B0000)
- **UI**: Military olive (#556B2F), Dark brown (#3C280D)

### Visual Style
- Hand-drawn/sketchy aesthetic with bold outlines
- Pixel-art inspired but with smooth animations
- Screen shake on explosions
- Particle effects: sand spray, smoke, sparks

### Materials & Effects
- Vignette effect for intensity
- Screen flash on damage
- Bullet trails (tracer effect)
- Explosion sprites with expanding rings

## 3. Game Mechanics Specification

### Player (Allied Soldier)
- **Movement**: Automatic forward run (constant speed)
- **Controls**:
  - SPACE / UP / W: Jump
  - DOWN / S: Dive/Slide (low profile dodge)
- **Health**: 3 hits (shown as dog tags)
- **Invincibility frames**: 1.5 seconds after hit
- **Animation states**: Run, Jump, Slide, Hit, Death

### Enemies & Hazards
1. **MG Nest**: Stationary, fires burst of bullets in arc
2. **Sniper**: Fires single aimed shots from distance
3. **Artillery**: Periodic explosions at random beach positions
4. **Barbed Wire**: Obstacle, must jump over
5. **Craters**: Can slide into for cover

### Scoring
- Distance traveled: 1 point per unit
- Enemy killed (shooting back): 50 points
- Survival bonus: 100 points per 10 seconds
- Combo multiplier for consecutive dodges

### Difficulty Progression
- Speed increases every 30 seconds
- Enemy spawn rate increases over time
- More artillery and sniper attacks as distance increases

## 4. Audio Specification
- **Sound Effects** (synthesized):
  - Gunfire (player & enemy)
  - Explosions
  - Jump/Dive
  - Hit/Damage
  - Victory fanfare on reaching end
- **Music**: Fast-paced military drum beat (generated)

## 5. UI Specification
- **HUD**:
  - Top-left: Score counter (military stencil font)
  - Top-right: Distance meter
  - Bottom-center: Health (3 dog tag icons)
- **Game States**:
  - Title Screen: "D-DAY RUSH" with "Press SPACE to Start"
  - Playing: Active gameplay
  - Game Over: Final score, "Press SPACE to Restart"
  - Victory: Reached the end of the beach (5000m)

## 6. Technical Specification
- **Engine**: HTML5 Canvas 2D
- **Resolution**: Responsive, 16:9 aspect ratio
- **Target FPS**: 60
- **No external dependencies** - pure vanilla JS

## 7. Acceptance Criteria
1. Player can jump and slide to dodge incoming fire
2. Enemies spawn and shoot at player
3. Parallax background scrolls creating depth
4. Score increases based on distance and kills
5. Game over triggers when health depleted
6. Victory triggers at 5000m distance
7. Screen shake and particle effects work
8. All sound effects play correctly
9. Game runs smoothly at 60 FPS
10. Controls are responsive (< 16ms input lag)
