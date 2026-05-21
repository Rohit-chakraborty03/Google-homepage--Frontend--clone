# Google-homepage--Frontend--clone
Building the google homepage clone to learn div positioning and basics of flexbox.

# Google Homepage Layout Clone 

**Live Demo:** [Insert your GitHub Pages link here]

## Why I built this
I built this project to master the fundamentals of CSS layouts. It’s easy to watch a tutorial on Flexbox, but I wanted to prove to myself that I could build a pixel-perfect layout from scratch without relying on a framework like Bootstrap or Tailwind. 

Plus, getting a `div` perfectly centered on a screen is a frontend rite of passage, so I figured recreating the most visited webpage in the world was the best place to start.

## The Tech Stack
* **HTML5:** Semantic structure.
* **CSS3:** Heavy use of Flexbox, viewport units (`vh`), and custom properties. 
* **Zero JavaScript:** Just raw styling and layout logic.

## The Biggest Roadblocks (and how I fixed them)

### 1. The "100vh" Flexbox Trap
I initially tried to center the logo and search bar using `justify-content: center` and `align-items: center`, but everything stayed stuck at the top of the screen. I realized the container was only as tall as the content inside it. Adding `height: 100vh` to the main wrapper forced the container to fill the screen, giving Flexbox the empty space it needed to actually center the items.

### 2. The Search Bar Sizing Nightmare
When I tried to add padding inside the search bar input so the text wouldn't touch the edges, the entire width of the bar stretched out and broke the layout. I learned about the CSS box model flaw and applied `box-sizing: border-box;`. This forced the browser to absorb the padding into the total width, keeping my 600px search bar exactly 600px wide.

### 3. Pinning the Navigation
I needed the Google Apps icon and the Gmail link to stay in the top right corner without disrupting the perfectly centered logo. I ended up using `position: absolute;` on the top nav to pull it out of the normal Flexbox flow and pin it to the edges.

## What I'd do next
If I were to expand this, I would add the actual Google Search API using JavaScript so the search bar returns real results, and build out the responsive layout for mobile screens.
