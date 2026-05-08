# FPS-GAME-1v1-TRAINING

A browser-based CS2 3D Aim Trainer where you can practice your aim solo or compete in 1v1 matches with friends using peer-to-peer connections.

## Features

### Solo Practice Mode
- **60-second aim training sessions** with targets spawning directly in your view
- **Score tracking** - Earn 10 points per target hit
- **Accuracy statistics** - Real-time accuracy percentage
- **Customizable crosshair** - Multiple styles, colors, sizes, and widths
- **Audio feedback** - Distinct sounds for hits and misses

### 1v1 Multiplayer
- **Peer-to-peer gameplay** using PeerJS
- **Create or join rooms** with custom room codes
- **Real-time player positions** synced between players
- **Health system** - 100 HP with 20 damage per hit
- **Live health bars** for both players

### Customization Options
- **Sensitivity slider** (0.1 - 10.0)
- **Crosshair styles** - Default or T-style
- **Center dot toggle**
- **Custom crosshair colors**
- **Adjustable crosshair dimensions** - Length, width, and size
- **Volume control** (0 - 100%)
- **Sound on/off toggle**

All settings are **saved to localStorage** and persist between sessions.

## How to Play

### Solo Mode
1. Click **Start Practice**
2. Click to lock your cursor
3. Move your mouse to aim
4. Click to shoot targets
5. Press ESC to pause and adjust settings

### Multiplayer Mode
1. Click **1v1**
2. **Create Room** - Enter a custom room code and share it with a friend
3. **Join Room** - Enter a room code to join an existing game
4. Aim and shoot your opponent
5. First player to deplete opponent health wins

## Technology Stack

- **Three.js** - 3D graphics and rendering
- **PeerJS** - Peer-to-peer networking
- **Web Audio API** - Sound generation
- **localStorage** - Settings persistence

## Game Mechanics

### Aim Training
- Targets spawn randomly within your view (4-7.2 units away)
- Targets spawn at varied heights (0.5-1.5 units vertical)
- Targets rotate continuously for visual feedback
- Hit targets glow briefly and respawn immediately

### 1v1 Combat
- Players move with WASD keys
- Camera controlled with mouse (with pointer lock)
- Raycast hit detection for shooting
- 20 damage per successful hit
- Game ends when a player's health reaches 0

## Controls

| Key | Action |
|-----|--------|
| **Mouse Move** | Look around |
| **Click** | Shoot |
| **W** | Move forward |
| **A** | Move left |
| **S** | Move backward |
| **D** | Move right |
| **ESC** | Pause/Resume |

## Audio

- **Hit sound** - 880Hz triangle wave (hit feedback)
- **Miss sound** - 220Hz square wave (miss feedback)
- **Start sound** - Two-tone beep sequence
- **Lobby ambience** - Ambient drone background (when in menu)

## Settings

Access the pause menu (ESC) to adjust:
- Mouse sensitivity
- Crosshair style and appearance
- Volume and sound effects
- Target size

## File Structure

The game is a single HTML file containing:
- HTML structure and UI elements
- CSS styling for the game interface
- JavaScript with Three.js scene setup
- Game logic and mechanics
- PeerJS multiplayer networking
- Web Audio synthesis

## Getting Started

1. Open the HTML file in a modern web browser
2. Start with solo practice to warm up
3. Challenge friends to 1v1 matches
4. Customize your crosshair and sensitivity for optimal aim
5. Adjust volume and sounds to your preference

## Browser Requirements

- Modern browser supporting WebGL
- Web Audio API support
- Pointer Lock API support for mouse control
- localStorage support

## Multiplayer Networking

Uses PeerJS library for WebRTC peer-to-peer connections:
- **No server required** - Direct browser-to-browser connection
- **Room codes** - Custom identifiers for easy room sharing
- **Real-time sync** - Position and shooting data sent continuously
- **Automatic cleanup** - Connection closes when players disconnect

---

**Enjoy training your aim and competing with friends!** 🎮
