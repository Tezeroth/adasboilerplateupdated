# Project Changes Log

This document tracks all significant changes to the project since December 10th, 2024. Each change is explained in simple terms for non-technical readers.

## December 10th, 2024

### Initial Setup
- Created the basic project structure
- Set up the main HTML file (index.html) with A-Frame framework
- Added essential JavaScript files for AR/VR functionality:
  - `ar-cursor.js`: Helps with clicking/touching objects in AR
  - `ar-shadow-helper.js`: Makes shadows look better in AR
  - `model-utils.js`: Helps with 3D model display and lighting
  - `simple-navmesh-constraint.js`: Helps with movement and navigation
  - `main.js`: Contains the main game/application logic

### External Dependencies
Added several important external libraries (CDN links):
- A-Frame (version 1.7.0): The main framework for creating VR/AR experiences
- PhysX (version 0.2.0): Handles physics (like gravity and collisions)
- Various other components for hand tracking and controls

### Core Features Implemented
1. **Hand Tracking System**
   - Added support for both left and right hand tracking
   - Implemented finger-tip tracking for precise interactions
   - Added visual feedback for hand positions

2. **Physics System**
   - Integrated PhysX for realistic physics simulation
   - Added support for:
     - Object collisions
     - Gravity effects
     - Dynamic and static objects
     - Physics-based interactions

3. **Navigation System**
   - Implemented teleportation controls
   - Added movement controls for smooth navigation
   - Created a navmesh system for proper movement constraints

4. **AR/VR Features**
   - Added support for both AR and VR modes
   - Implemented shadow casting and receiving
   - Added support for HTML overlays in AR/VR

### Known Issues
- PhysX WASM file is currently loaded from CDN, which might cause issues when running locally
- Need to download and include the PhysX WASM file locally for better development experience

### Technical Improvements
- Updated to latest versions of dependencies
- Improved code organization and documentation
- Added proper error handling for various scenarios

## Future Changes
This section will be updated as new changes are made to the project. Each entry will include:
- The date of the change
- What was changed
- Why it was changed
- How it affects the project
- Any technical details explained in simple terms

## How to Read This Document
- Each change is organized by date
- Technical terms are explained in simple language
- CDN updates are clearly marked
- Known issues and their solutions are documented
- The impact of each change is explained in non-technical terms

## Local Development Setup
For developers working on this project locally:
1. Download the PhysX WASM file from: https://cdn.jsdelivr.net/gh/c-frame/physx@v0.2.0/wasm/physx.release.wasm
2. Create a `lib` or `assets` directory in your project
3. Place the WASM file in that directory
4. Update the `wasmUrl` in `index.html` to point to your local file
5. Ensure your local server is configured to serve .wasm files with the correct MIME type 