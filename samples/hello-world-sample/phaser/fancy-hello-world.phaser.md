# Phase: Fancy Hello World

## Task Description
Create an interactive, visually engaging "Hello World" web application contained within a single HTML file (incorporating all necessary CSS and vanilla JavaScript). The project should reside in the `web-sample` directory. The application must feature a fancy animation, respond to user clicks, and be runnable simply by opening it in a browser.

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

### 1. Setup HTML Structure and Aesthetics
**Prompt:** Create the `index.html` file in the `hello-world-sample` directory. Set up a modern, visually stunning HTML structure. Include a rich CSS design system within `<style>` tags. Use modern web design principles like dark mode, smooth gradients, glassmorphism, and a modern typography font. Center a "Hello World" heading on the screen. Give it a continuous, subtle CSS-based animation (e.g., a slow gradient pulse, floating effect, or glow). Do not use any external dependencies besides fonts.
**Gate:** STOP & COMMIT

***After Action***
Created `index.html` in the `hello-world-sample` directory.
- Implemented a dark mode theme with an ambient radial gradient background.
- Added a glassmorphism container using `backdrop-filter` and semi-transparent borders.
- Applied the Google Font "Outfit" for modern typography.
- Designed a vibrant gradient text effect for the "Hello World" heading.
- Added continuous CSS animations: a floating effect on the container, a background-position animation for the text gradient pulse, and an ambient glowing orb in the background.

### 2. Implement Interactive Animation (JavaScript)
**Prompt:** Enhance `index.html` by adding interactivity using vanilla JavaScript in a `<script>` tag. When the user clicks anywhere on the screen or on the text itself, trigger an eye-catching, dynamic visual effect. You might implement a particle burst using a dynamically created `<canvas>`, or creative DOM manipulations causing the letters to scatter and reform. Ensure the JavaScript logic is entirely contained within the file and works smoothly in the browser.
**Gate:** STOP & COMMIT

***After Action***
Updated `index.html` with vanilla JavaScript interactivity.
- Added a full-screen, pointer-events-none `<canvas>` element for rendering effects.
- Implemented a `Particle` class with physics (velocity, decay, size variation) and vibrant colors matching the design system.
- Added an `animate` loop to continuously draw and fade out particles with a glowing lighter composition effect.
- Bound a `click` event listener to the document that spawns a burst of 60 particles at the cursor coordinates.
- Added a subtle CSS transform scale effect to the "Hello World" heading on click for tactile feedback.
- Set the body cursor to `pointer` to indicate the interactive nature of the page.

### 3. Final Polish and Responsiveness
**Prompt:** Review and refine the `index.html` file. Ensure that the layout adapts perfectly to different window sizes (responsiveness). Verify that the micro-animations are smooth and that interactive elements provide clear feedback (like `cursor: pointer` on hover). Ensure all SEO and meta tags are present for a complete HTML document structure.
**Gate:** STOP & COMMIT

***After Action***
Finalized the responsiveness and SEO of `index.html`.
- Added essential SEO meta tags including `description`, `author`, `keywords`, and Open Graph tags for better discoverability.
- Implemented CSS media queries for tablets (`max-width: 768px`) and mobile devices (`max-width: 480px`), adjusting the container padding and font sizes appropriately.
- Verified that all interactive UI micro-animations and elements function smoothly across different screen sizes.

## Final Step: Documentation
Once all prompts above have been executed and have their corresponding `***After Action***` blocks, evaluate the accumulated work and create/update documentation in `./docs/` if warranted.
