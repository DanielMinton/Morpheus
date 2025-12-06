# Morpheus

Procedural animation system with physics-based motion design.

## Overview

Morpheus is a creative coding framework for generative animations. Chain physics simulations, noise functions, and easing curves together to create organic, responsive motion graphics.

## Features

- **Physics Engine**: Spring, gravity, and collision systems
- **Noise Functions**: Perlin, Simplex, and custom noise
- **Easing Library**: 30+ easing functions
- **Composable Behaviors**: Chain modifiers for complex motion
- **Timeline Control**: Keyframe and procedural hybrid
- **Export Options**: GIF, video, and interactive embeds

## Technical Stack

- **TypeScript** - Animation engine core
- **Canvas API** - 2D rendering
- **GSAP** - Advanced tweening
- **Matter.js** - Physics simulation
- **React** - UI components

## Motion Primitives

**Physics**:
- Springs (configurable stiffness/damping)
- Particles with forces
- Rigid body dynamics
- Constraints

**Procedural**:
- Perlin noise flow fields
- Simplex displacement
- Voronoi patterns
- L-systems

**Easing**:
- Quad, Cubic, Quart, Quint
- Sine, Expo, Circ
- Elastic, Bounce, Back

## Example Usage

\`\`\`javascript
import { Morpheus, Spring, Perlin } from 'morpheus';

const scene = new Morpheus('#canvas');

const particle = scene.add.circle({
  x: scene.width / 2,
  y: scene.height / 2,
  radius: 20
});

particle.motion
  .spring({ stiffness: 0.1, damping: 0.8 })
  .perlin({ scale: 0.01, strength: 50 })
  .follow(scene.mouse);

scene.start();
\`\`\`

## Demo

View the live demo at: https://danielminton.github.io/Morpheus/

## Author

Daniel Minton