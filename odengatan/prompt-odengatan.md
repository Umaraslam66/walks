Build a complete, production-ready, single-file HTML/JavaScript application that renders a highly detailed, photo-realistic, navigable 3D scene of Odengatan in Vasastan, Stockholm, Sweden using Three.js — experienced from the perspective of a CYCLIST riding the ~350m hero segment from Odenplan square to Stadsbiblioteket (Stockholm Public Library).

You are working in Claude Code, so build this iteratively: scaffold the scene first, then add architecture, then street life, then the camera systems. Test your assumptions as you go and keep refining until every feature below is fully implemented. The final deliverable is ONE self-contained HTML file.

CRITICAL INSTRUCTIONS — NO LAZY CODE

* Do NOT use any external asset URLs (no external .gltf, .obj, .jpg, or .png files) as they can break or fail CORS. All textures and models must be generated dynamically and procedurally within the script (HTML Canvas-drawn textures, procedural noise for plaster/asphalt/stone, mathematical geometry for all meshes).
* Do NOT write placeholder comments, truncated code, "// TODO" markers, or simplified stand-ins. Every function, shader, loop, and variable must be fully written out.
* The output must be a single, copy-pasteable HTML file that runs perfectly immediately when opened in a browser.

TECHNICAL REQUIREMENTS & FEATURES

1. Libraries: Load Three.js and any needed controls via a reliable CDN (cdnjs or unpkg).

2. TWO CAMERA MODES (toggle with a styled on-screen button and the 'C' key):
   * MODE 1 — CYCLIST RIDE (default, video-friendly): The camera follows a smooth spline path along the cycle lane from Odenplan to the library steps at realistic cycling speed (~18-20 km/h), at handlebar/eye height (~1.6m). Add subtle realism: gentle handlebar sway, slight lean into the path's curves, a faint vertical bob, and procedurally modeled handlebars + front wheel visible at the bottom of the frame. The ride should take roughly 60-75 seconds, slow down and stop smoothly at a red signal mid-route (timed so the light turns green after ~4 seconds, then the ride resumes), and end with a graceful slowdown facing the library rotunda. Include a 'restart ride' button.
   * MODE 2 — FREE ROAM (WASD + mouse look, PointerLock): Walk freely at human eye-level within the street boundaries to explore details. Restrict camera height and bounds to human scale.

3. The Hero Landmark — Stadsbiblioteket:
   * Gunnar Asplund's library is the climax of the ride and must be unmistakable: the great orange-red plastered cylindrical rotunda rising from a rectangular base block, tall narrow vertical window strips around the rotunda, the broad front steps, and the tall dark entrance portal. Model this with real care using procedural geometry — it is the money shot.
   * Place it correctly at the end of the route at the Sveavägen corner, slightly elevated, so it reveals progressively as the cyclist approaches.

4. Odenplan & Street Architecture (Vasastan Style):
   * Start the ride at Odenplan: an open square with the Gustav Vasa kyrka suggested as a pale neo-baroque domed mass on one side, the modern glass Odenplan station entrance pavilion, bike racks full of parked bicycles, and a bus stop with shelter.
   * Line Odengatan with grand turn-of-the-century apartment blocks (5-6 stories): plastered facades in ochre, terracotta, beige, and grey-green with procedural weathered plaster bump maps, regular tall window grids, ornamented entrance portals, and corner towers/bay windows on select buildings.
   * Ground floors must feel alive: procedurally drawn shopfronts — a café with outdoor terrace (tables, chairs, parasols), a bakery, a bookshop, a grocery with fruit crates outside, a florist — each with canvas-drawn signage, awnings in varied colors, and lit display windows.

5. Street Layout & Cycling Infrastructure:
   * Cross-section: building — sidewalk — painted/separated cycle lane — car lanes with median trees — cycle lane — sidewalk — building. The cyclist rides in a proper lane, not on the road.
   * Procedural asphalt for car lanes (with markings, manholes, patches), distinct reddish or painted surface for cycle lanes with bike symbols, and concrete slab sidewalks with granite curbs.
   * Rows of mature street trees (procedural lindens with instanced leaves) along the median and sidewalks.

6. Street Life & Signals:
   * One fully functional signalized intersection mid-route: traffic lights for cars AND separate small cyclist signals, cycling through red/green phases on a timer, with a zebra crossing. The cyclist ride mode must obey it (the scripted red-light stop).
   * Procedural low-poly people: pedestrians walking the sidewalks, people at the café terrace, someone locking a bike. 2-3 other cyclists passing in the opposite lane on simple spline paths. 2-4 cars driving the car lanes on loops, and one blue Stockholm city bus pulling away from the Odenplan stop at ride start.

7. Nordic Lighting & Atmosphere:
   * Clear late-afternoon Stockholm sun: a warm DirectionalLight casting long soft shadows across the street canyon (THREE.PCFSoftShadowMap), HemisphereLight with pale-blue sky and neutral ground bounce, ACESFilmicToneMapping.
   * Subtle depth/atmospheric fog so the far end of the street and the library reveal feels cinematic.

8. Optimization:
   * Maintain 60 FPS on standard desktop GPUs: instanced geometry for all repeating elements (windows, leaves, cobbles, people, bikes), frustum-friendly object grouping, and flawless window-resize handling.
   * Animated objects (cars, cyclists, pedestrians, signals) must run on simple parametric loops, not physics.

Build it step by step, verify the file is complete and self-contained, and deliver the final single HTML file.