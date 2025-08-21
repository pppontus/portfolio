# Paper Shaders Library Documentation

## Overview

Paper Shaders is a zero-dependency HTML canvas shader library designed to create dynamic visual backgrounds and textures for web applications. The library's primary mission is to "Give designers a visual way to use common shaders in their designs" while providing "directly exportable as lightweight code that works in any codebase."

## Key Features

- **Zero Dependencies**: Pure HTML canvas shaders with no external dependencies
- **Multi-Framework Support**: Currently supports Vanilla JavaScript and React
- **High Performance**: Optimized for maximum performance across devices
- **Wide Compatibility**: Broad browser and device support
- **Lightweight**: Minimal bundle size impact
- **Highly Customizable**: Extensive configuration options for each shader
- **Animation Support**: Both static and animated shader effects

## Installation

### React
```bash
npm install @paper-design/shaders-react
```

### Vanilla JavaScript
```bash
npm install @paper-design/shaders
```

**Important Note**: The library is currently in pre-1.0 development. Pin your dependency version as breaking changes may occur under 0.0.x versioning.

## Usage

### React Implementation

```jsx
import { MeshGradient, DotOrbit } from '@paper-design/shaders-react';

// MeshGradient Example
<MeshGradient
  colors={['#5100ff', '#00ff80', '#ffcc00', '#ea00ff']}
  distortion={1}
  swirl={0.8}
  speed={0.2}
  style={{width: 200, height: 200}}
/>

// DotOrbit Example
<DotOrbit
  colors={['#5100ff', '#00ff80']}
  colorBack="#000000"
  scale={0.3}
  style={{width: 200, height: 200}}
/>
```

### Vanilla JavaScript Implementation

The library exports a `ShaderMount` class and utility functions for vanilla JavaScript usage.

## Available Shaders

The library includes 25+ different shader effects:

### Core Shaders
- **MeshGradient**: Dynamic color-blending background with distortion and swirl effects
- **DotOrbit**: Animated dot-based visual effects
- **SmokeRing**: Smoke-like particle effects
- **NeuroNoise**: Neural network-inspired noise patterns
- **SimplexNoise**: Classic Simplex noise implementation
- **Metaballs**: Fluid blob-like effects

### Visual Effects
- **GodRays**: Dramatic light ray effects
- **LiquidMetal**: Metallic fluid simulation
- **Voronoi**: Voronoi diagram-based patterns
- **Water**: Water surface simulation
- **Waves**: Wave pattern generation
- **Swirl**: Swirling motion effects

### Texture Generators
- **PaperTexture**: Paper-like texture generation
- **GrainGradient**: Grainy gradient effects
- **Dithering**: Dithering pattern effects
- **ImageDithering**: Image-based dithering
- **FlutedGlass**: Glass-like distortion effects

### Geometric Patterns
- **ColorPanels**: Color panel arrangements
- **DotGrid**: Dot-based grid patterns
- **PulsingBorder**: Animated border effects
- **Spiral**: Spiral pattern generation
- **Warp**: Warping distortion effects

### Static Variants
- **StaticMeshGradient**: Non-animated mesh gradient
- **StaticRadialGradient**: Static radial gradient patterns

## API Structure

### Core Components

#### ShaderMount
The main class for mounting and managing shader instances in vanilla JavaScript.

#### Component Props (React)

**Common Props:**
- `colors`: Array of hex color codes
- `style`: CSS styling object (width, height, etc.)

**MeshGradient Specific:**
- `distortion`: Numeric value controlling distortion intensity
- `swirl`: Numeric value controlling swirl effect
- `speed`: Animation speed (numeric value)

**DotOrbit Specific:**
- `colorBack`: Background color hex code
- `scale`: Numeric scaling factor

### Utility Functions
- `getShaderColorFromString`: Convert color strings to shader-compatible format
- `getShaderNoiseTexture`: Generate noise textures for shader use
- `isPaperShaderElement`: Check if element is a Paper Shader component

## Technical Implementation

### WebGL Foundation
The library is built on WebGL technology using fragment shaders for efficient GPU-accelerated rendering.

### Framework Architecture
- **Vanilla JS**: Core `ShaderMount` class with direct WebGL integration
- **React**: Wrapper components that utilize the core shader functionality
- **Future Frameworks**: Designed to accept community PRs for Vue and other frameworks

### Performance Considerations
- Zero external dependencies reduce bundle size
- GPU-accelerated rendering for optimal performance
- Efficient memory management
- Broad device compatibility

## Configuration and Customization

### Color Management
Colors are specified as hex strings in arrays, allowing for complex multi-color effects.

### Animation Control
Animation parameters like `speed` allow fine-tuning of motion effects.

### Sizing and Layout
Standard CSS styling through the `style` prop enables flexible layout integration.

## Development Status and Roadmap

### Current Status
- Stable Vanilla JavaScript and React implementations
- 25+ shader effects available
- Zero-dependency architecture

### Future Plans
- Community-driven expansion to additional frameworks
- Continued shader effect library expansion
- Performance optimizations
- Enhanced documentation and examples

### Version Management
The library is currently in pre-1.0 development phase. Users should pin dependency versions to avoid unexpected breaking changes during rapid development cycles.

## Use Cases

### Background Textures
Perfect for creating dynamic, visually appealing website backgrounds that respond to user interaction or animate automatically.

### Design System Integration
Easily integrate into existing design systems with customizable color palettes and sizing options.

### Interactive Applications
Create engaging visual experiences for web applications, games, and interactive media.

### Masking and Effects
Use for shape and text masking to create sophisticated visual effects.

## Browser Support

The library is designed for broad browser compatibility, leveraging standard WebGL implementations available in modern browsers.

## Community and Contributions

The Paper Shaders project welcomes community contributions, particularly for expanding framework support beyond the current Vanilla JS and React implementations.