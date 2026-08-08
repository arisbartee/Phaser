# Text Scrambler Application

## Overview
The Text Scrambler is a fun, interactive, single-file HTML application built with vanilla JavaScript and CSS. It takes user input and uses an HTML5 `<canvas>` element to playfully animate the text characters around the screen.

## Features
- **Visual Design**: The UI features a centered glassmorphism card over a seamlessly animated, vibrant gradient background.
- **Interactive Scrambling**:
  - Clicking the "Scramble" button breaks down the inputted text into individual characters.
  - Each character becomes a physics-enabled object bouncing around the screen with its own gravity, velocity, and elasticity.
  - The letters continuously cycle through vibrant HSL color hues for a dynamic and chaotic visual effect.
- **Device Support**: The canvas properly accounts for `devicePixelRatio` to ensure crisp text rendering on retina displays and responds to window resize events to remain full-screen.
- **Reset functionality**: A dedicated "Reset" button immediately stops the chaotic physics loop, clears the canvas, and resets the input field, creating a polished transition back to the default state for a new interaction.

## Technical Implementation
- **HTML/CSS**: Contains embedded vanilla CSS featuring Google Fonts ('Outfit'), glassmorphism styling (`backdrop-filter`), and CSS keyframe animations.
- **Canvas / JavaScript Engine**:
  - Implements a custom `Letter` class to manage the physics simulation (position, velocity, bounding box collision detection) and color state.
  - Uses a `requestAnimationFrame` loop to continuously update and render the character objects to the HTML5 Canvas.
