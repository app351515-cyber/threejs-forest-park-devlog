# Technical notes — Three.js forest park

A historical implementation summary, **not a reproducible source-code release**.

## Renderer

- Archived implementation used **Three.js r185**, **WebGPURenderer**, and **TSL**.
- Shader/node work appears for materials, vertex deformation, water, and light shafts; WGSL also appears in mist experiments.
- Equivalent production-grade WebGL results were not established by the saved tests.

## Terrain and vegetation

- An approximately **11 m** small scene was the visual reference; it was preserved during later expansion.
- Procedural forms for trunks, branches and roots were combined with sourced PBR textures and vegetation detail. **Not all assets were AI-generated.**
- Fixed seeds and stable placement preserved accepted scenery while new areas were added.
- The finite 1,000 × 1,000 m layout was organized in 50 m cells, 20 × 20; **not** a verified infinite streaming world.

## Rendering experiments

- Compatible vegetation batching and grouping.
- Distance LOD and proxy representations.
- Reducing unnecessary GPU transfers when placement data was unchanged.
- Experimental distant-tree multi-view atlas approach.

**Important trade-offs:** fewer triangles can increase draw calls. Caching on the CPU can be slower. Neither change proves improved frame time by itself.

## Visual atmosphere

- Iterative sunlight, shadow, material, ambient light and God Rays work.
- PCSS, SSGI and wind-related normal adjustment were tried then removed from the normal configuration.
- Water visuals involved depth-related attenuation, Fresnel and localized reflection; they **do not** imply a full 3D fluid simulation.

Experiments and settings were not necessarily all used together in one build. See [Performance and limitations](PERFORMANCE_AND_LIMITATIONS.md).
