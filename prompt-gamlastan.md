Write a complete, production-ready, single-file HTML/JavaScript application that renders a highly detailed, photo-realistic, navigable 3D scene of the iconic medieval old town of Gamla Stan, Stockholm, Sweden using Three.js.
CRITICAL INSTRUCTIONS — NO LAZY CODE

* Do NOT use any external asset URLs (no external .gltf, .obj, .jpg, or .png files) as they can break or fail CORS. All textures, heights, and models must be generated dynamically and procedurally within the script (e.g., using HTML Canvas to draw textures, procedural noise algorithms for plaster and stone, or mathematical structures for 3D meshes).
* Do NOT write placeholder comments, truncated code blocks, "// TODO" markers, or "left as an exercise" shorthand. Every single function, shader, loop, and variable must be written out in its entirety.
* The output must be a single, copy-pasteable HTML file that runs perfectly immediately when opened in a browser.
TECHNICAL REQUIREMENTS & FEATURES

1. Libraries: Load Three.js and OrbitControls via a reliable CDN (cdnjs or unpkg).
2. Iconic Architecture (Gamla Stan Style):
   * Colorful Plastered Townhouses: Tall, narrow 17th-18th century townhouses (3-5 stories) in the classic Stockholm palette of warm ochre, falu red, mustard yellow, and burnt orange, standing shoulder-to-shoulder. Implement a procedural weathered plaster texture (low-frequency noise bump map with subtle patina and water-staining variation) applied to matte painted-render materials to mimic centuries-old facades.
   * Gabled Rooflines: Steep pitched roofs with terracotta clay tiles and stepped or curved Dutch-style gables on select buildings; add procedural chimneys and small dormer windows.
   * Ornamental Windows & Doors: Procedurally generate tall multi-paned windows with white-painted wooden frames and crossbars (drawn using canvas coordinates), some with small flower boxes. Create heavy arched wooden entry doors with black wrought-iron hinges and stud patterns, plus a few hanging wrought-iron shop signs and old-fashioned lanterns mounted on the walls.
3. Medieval Cobblestone Alleyway:
   * Establish a narrow, winding, gently sloped pedestrian alley inspired by streets like Prästgatan and Mårten Trotzigs gränd, where the facades lean close together, ending at a small open square (inspired by Stortorget) or a quayside viewpoint.
   * The street must use a procedural cobblestone texture (canvas-generated noise representing individual rounded granite setts with dark grout) applied as a displacement and roughness map.
   * Add worn stone steps, bollards, and a low granite curb along the alley edges.
4. The Baltic Waterfront Overlook (Background Water & Sky):
   * Provide a view of the Riddarfjärden / Baltic inlet at the end of the alley, with a distant silhouette suggestion of spires (a slender church spire like Riddarholmen's cast-iron spire as a simple procedural mesh on the horizon).
   * Water: Use a custom shader or a steel-blue MeshStandardMaterial with layered scrolling normal maps to simulate cold, gently rippling Nordic water reflecting the low sun.
   * Sky: A crisp, clear Scandinavian summer-evening sky with subtle atmospheric scattering and a low golden-hour sun source.
5. Procedural Flora (Window Boxes & Courtyard Greenery):
   * Climbing Ivy & Virginia Creeper: Create vines climbing select facades. Use instanced meshes for thousands of tiny green leaves (procedural alpha-masked shapes) clustered together.
   * Window Boxes & Potted Plants: Place flower boxes with red geraniums under windows, and a few wooden planters and small linden/birch trees near the square.
6. Nordic Golden-Hour Lighting & Shadows:
   * Setup a DirectionalLight representing the low Scandinavian evening sun, casting long, soft-edged shadows down the narrow alley (`THREE.PCFSoftShadowMap`).
   * Use a HemisphereLight with a cool pale-blue sky color and a warm ochre ground color to emulate realistic bounce light off the colorful plaster facades.
   * Add a few warm point lights from the wall-mounted lanterns for cozy accent lighting in shaded parts of the alley.
   * Configure ACESFilmicToneMapping to handle the contrast between sunlit ochre walls and the deep cool shadows of the narrow lane without blowing out the highlights.
7. Navigation & Exploration:
   * Implement OrbitControls or a first-person WASD/PointerLock setup. Restrict the camera height and boundary limits to keep the user at human scale (eye-level) as they navigate the winding, lantern-lit medieval alleyway toward the square and waterfront.
8. Optimization:
   * Maintain 60 FPS on standard desktop GPUs by employing instanced geometry for repeating architectural elements (cobblestones, window frames, roof tiles, leaves) and handling window resizing flawlessly.
Generate the full, un-truncated, single-file HTML code now.