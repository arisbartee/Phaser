# Phase: Text Scrambler Application

## Task Description
Create a fancy, ultra-cool text scrambler in a single HTML file (`index.html`) using vanilla JavaScript and CSS. The app should provide an input field, a "Scramble" button, and a "Reset" button. The styling should be playful and colorful. The scrambling effect should use an HTML5 `<canvas>` to animate the text characters in fantastic, silly ways (specifically bouncy letters and rapidly changing colors).

## Instructions for AI Execution
This is a self-contained phase file. If you are an AI assistant tasked with executing this file, you must follow these rules strictly:
1. **Sequential Execution**: Execute the prompts under `## Prompts to Execute` in numerical order. Skip prompts that already have an `***After Action***` section beneath them.
2. **After Action**: Immediately after successfully executing a prompt, append an `***After Action***` block directly beneath the prompt. This block should contain explanations of the work done, changes made, and any documentation instructions.
3. **Respect the Gate**: After writing the `***After Action***` block, look at the `Gate` defined for that prompt:
   - `STOP & COMMIT`: Stop execution, suggest a commit command to the user, and wait for them to confirm the commit before running the next prompt.
   - `NEEDS CLARIFICATION`: Stop execution and ask the user for the needed input.
   - `NONE`: Proceed to the next prompt.
4. **Final Documentation Evaluation**: Once all prompts have been executed (all have an `***After Action***` block), evaluate all the after-actions. If warranted, generate or update project documentation in the `./docs/` directory summarizing the completed work.

## Prompts to Execute

### 1. HTML Setup & Playful UI Styling
**Prompt:** Create `index.html` in the `text-scramble-sample/` directory. It should contain a playful, colorful, and visually stunning UI. Include a text input field, a "Scramble" button, and a "Reset" button. The styling must be written in vanilla CSS embedded in the file. Ensure the UI is centered, perhaps using a glassmorphism card effect on a colorful, animated background.
**Gate:** STOP & COMMIT

***After Action***
- Created `index.html` in the `text-scramble-sample/` directory.
- Built a visually stunning UI utilizing a centered glassmorphism card.
- Implemented a playfully animated gradient background and vibrant button colors.
- Used vanilla CSS within `<style>` tags to add all necessary styling, hover effects, and Google Fonts ('Outfit').

### 2. Canvas & JavaScript Setup
**Prompt:** In `index.html`, add an HTML5 `<canvas>` element below the input field and buttons to serve as the playground for our letters. Add a `<script>` tag at the bottom of the body. In this vanilla JavaScript, write the boilerplate to set up the canvas (handling device pixel ratio for sharp text, resizing to fill its container), set up a `requestAnimationFrame` loop, and capture the text from the input field when the "Scramble" button is clicked. For now, simply render the captured text normally on the canvas.
**Gate:** STOP & COMMIT

<!-- Add as many numbered prompts as necessary to complete the task -->

### 3. Bouncy Letters & Color Changing Effects
**Prompt:** Implement the fantastic and silly scrambling effects in the JavaScript. When the user clicks "Scramble", break the text into individual letter objects. Assign each letter a random starting velocity (x and y), a bouncy physics simulation (gravity and elasticity when hitting the canvas bounds), and logic to constantly change its color to random vibrant colors over time. Render each letter at its updated physics-driven position in the animation loop.
**Gate:** STOP & COMMIT

### 4. Reset Functionality
**Prompt:** Implement the functionality for the "Reset" button. When clicked, it should stop the chaotic bouncing and clear the input field and the canvas entirely, returning the UI to a clean state ready for the user to type a new phrase. Make sure the transition feels polished.
**Gate:** STOP & COMMIT

## Final Step: Documentation
Once all prompts above have been executed and have their corresponding `***After Action***` blocks, evaluate the accumulated work and create/update documentation in `./docs/` if warranted.
