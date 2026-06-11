Write a complete, production-ready, single-file HTML/JavaScript application that renders a highly detailed, photo-realistic, navigable 3D scene of Götgatan in Södermalm, Stockholm, Sweden using Three.js — with an interactive BEFORE/AFTER toggle showing the street as car-dominated today versus a fully pedestrianized, people-first redesign.
CRITICAL INSTRUCTIONS — NO LAZY CODE

* Do NOT use any external asset URLs (no external .gltf, .obj, .jpg, or .png files) as they can break or fail CORS. All textures, heights, and models must be generated dynamically and procedurally within the script (e.g., using HTML Canvas to draw textures, procedural noise algorithms for plaster and asphalt, or mathematical structures for 3D meshes).
* Do NOT write placeholder comments, truncated code blocks, "// TODO" markers, or "left as an exercise" shorthand. Every single function, shader, loop, and variable must be written out in its entirety.
* The output must be a single, copy-pasteable HTML file that runs perfectly immediately when opened in a browser.
TECHNICAL REQUIREMENTS & FEATURES

1. Libraries: Load Three.js and OrbitControls via a reliable CDN (cdnjs or unpkg).
2. The Core Feature — BEFORE/AFTER Toggle:
   * Implement a prominent, beautifully styled UI toggle button (fixed overlay, large and video-friendly, e.g., "TODAY 🚗 / REIMAGINED 🌳") that smoothly cross-transitions the street between two states.
   * The transition must be animated (1-2 seconds): cars fade/sink away, asphalt lanes morph into paving, trees and furniture scale up from the ground. No hard cuts — the morph itself is the money shot for video capture.
   * Both states share the same buildings, camera position, and lighting so the comparison reads instantly.
3. Iconic Architecture (Södermalm / Götgatan Style):
   * Early 20th-century Stockholm apartment blocks (5-6 stories) lining both sides: plastered facades in muted ochre, dusty pink, beige, and grey-green, with regular grids of tall windows, ground-floor shopfronts with large display windows, awnings, and hanging signs.
   * Implement procedural weathered plaster textures (low-frequency noise bump maps with subtle staining) and procedural shopfront details (canvas-drawn signage, window frames, door surrounds).
   * Add rooftop details: tin roofs, chimneys, and a few dormers.
4. STATE A — "TODAY" (Car-Dominated):
   * A wide asphalt roadway with two traffic lanes plus parallel parking lanes on both sides, procedural asphalt texture with lane markings, manhole covers, and patch repairs.
   * 10-15 procedurally modeled parked cars (simple but recognizable low-poly sedans/SUVs in realistic muted colors with metallic materials) plus 2-3 cars positioned in the lanes.
   * Narrow, cramped sidewalks squeezed against the buildings, traffic signs, parking meters, and a traffic light.
   * Muted, slightly grey ambiance grading for this state.
5. STATE B — "REIMAGINED" (Pedestrianized):
   * The full street width converted to high-quality paving: procedural granite sett and smooth slab textures with a distinct material band marking a two-way cycle path down one side.
   * Rows of street trees (procedural lindens with instanced leaves), planted beds, benches, and classic Stockholm-style lamp posts.
   * Outdoor café seating zones spilling from the shopfronts: tables, chairs, parasols, planter boxes.
   * Procedural low-poly people (15-20 simple stylized figures: walking, sitting at cafés) and a few parked bicycles plus 1-2 cyclists on the cycle path.
   * Slightly warmer, greener ambiance grading for this state.
6. Nordic Lighting & Shadows:
   * Setup a DirectionalLight representing a clear Stockholm late-afternoon sun casting long soft shadows down the street canyon (`THREE.PCFSoftShadowMap`).
   * Use a HemisphereLight with a pale-blue sky color and neutral ground bounce.
   * Configure ACESFilmicToneMapping for balanced contrast between sunlit facades and shaded street level.
7. Navigation & Exploration:
   * Implement OrbitControls or a first-person WASD/PointerLock setup. Restrict the camera height and boundary limits to keep the user at human scale (eye-level) walking down the street, with the toggle usable from any position.
   * Set the initial camera to a slightly elevated, down-the-street hero angle that frames the transformation perfectly for screen recording.
8. Optimization:
   * Maintain 60 FPS on standard desktop GPUs by employing instanced geometry for repeating elements (windows, cobble setts, leaves, people, cars) and handling window resizing flawlessly. Both states should be pre-built and toggled via visibility/animation, not rebuilt at runtime.
Generate the full, un-truncated, single-file HTML code now.