Create a complete, self-contained interactive demo as exactly one HTML code block only. Name your file : {YOUR MODEL NAME}.html. 

Output rules:

Return only one fenced ```html code block.

Do not include any explanation before or after the code.

Put all HTML, CSS, and JavaScript in that single file.

Do not use React, JSX, build tools, npm, imports, modules, bundlers, or external dependencies.

The result must run by pasting it directly into a local .html file and opening it in a browser.

If a library would normally be needed, recreate the needed behavior manually in vanilla JavaScript and WebGL or Canvas.

Keep everything fully self-contained.

Build an interactive 3D paper receipt with cloth-style simulation, matching the following specifications as closely as possible in a single HTML file:

Visual layout and UI

The page background must be a light off-white/gray, such as #e5e5e5.

Center the interactive 3D scene on the page.

Below the scene, add simple HTML text that says: Grab and drag the receipt

That instruction text must be centered, cleanly styled, and light gray.

Receipt texture generated from a canvas

Programmatically create an HTML <canvas> and use it as the receipt texture.

Use a monospaced font.

The paper color should be slightly off-white.

The text color should be dark gray or black.

Render this exact receipt content onto the texture canvas:

[CENTERED, LARGE, BOLD]: THE FLORNRM SHOP
[CENTERED]: 42 Mesh Lane, WebGL City
[CENTERED]: Tel: (555) 042-1337
[LEFT ALIGNED]: Date: 2026-02-23  14:17
[LEFT ALIGNED]: Order: #00382
[DASHED LINE DIVIDER]
[LEFT & RIGHT ALIGNED COLUMNS]:
Vertex Shader          $4.20
Fragment Shader        $3.50
Normal Map             $2.80
UV Unwrap              $1.50
Cloth Simulation       $6.00
[DASHED LINE DIVIDER]
Subtotal              $18.00
Tax (8%)               $1.44
[THICK LINE DIVIDER]
[BOLD] TOTAL          $19.44
[CENTERED, BOTTOM]: Thank you for visiting!
[CENTERED, BOTTOM, SMALLER]: Made by {YOUR NAME}
3D scene setup
Create a receipt mesh using a subdivided rectangular grid with a high segment count comparable to 3 x 6 world units and about 25 x 50 subdivisions so it can bend smoothly.
Render both sides of the paper.
Shade it so the folds are visible and the material feels like rough paper.
Add ambient light and directional light so the folds and curvature read clearly.
Simulate realistic depth and shadowing visually, even if implemented approximately.
Cloth / paper physics
Do not use any external physics library.
Implement a custom mass-spring or Verlet-based simulation directly in vanilla JavaScript.
Represent the receipt as a grid of particles connected by structural constraints between adjacent points.
Apply gravity downward.
Pin the top row of particles so the receipt hangs naturally from the top.
Each animation frame should:
integrate particle motion,
satisfy constraints multiple times for stiffness,
update the rendered mesh vertices.
The receipt should bend, fold, swing, and settle like thin paper or light cloth.
Interaction

The receipt must be draggable with the pointer.

On pointer down, detect the closest particle to the hit position and mark it as grabbed.

While dragging, move that particle in 3D space based on pointer position.

The rest of the receipt should respond dynamically, folding and pulling through the constraints.

On release, let the receipt swing back and settle naturally.

Show a small semi-transparent circular grab indicator at the grabbed position.

Technical constraints

Use only standard browser APIs in one HTML file.

Prefer WebGL for the 3D rendering. You may implement the rendering manually or with raw WebGL.

The code must be robust, readable, and organized.

The demo must work immediately when saved as a single .html file and opened in a browser.

Quality bar

Make it visually polished and satisfying to interact with.

Keep the receipt legible.

Keep performance reasonable.

Do not simplify it into a flat 2D mockup. It must feel genuinely 3D and physically simulated.

Again: output exactly one single ```html code block and nothing else.
