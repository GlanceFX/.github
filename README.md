# Glance FX Suite

**Glance FX Suite** is a modular set of libraries and tools designed to empower Minecraft developers with advanced display entity, particle, physics, and visualization capabilities. Built with performance, flexibility, and ease of use in mind, Glance FX allows developers to create immersive, high-quality visual effects, debug environments, and cinematic experiences.
It is not (yet) a "Model Engine"

## Overview

> **Note:** This is placeholder information - Glance is still unreleased!

The Glance FX Suite is organized into several interconnected projects:

### 1. **Glance API & Engine Runtime** (WIP)
   - The core library for the Glance FX Suite, consisting of:
     - **Glance API:** A platform-agnostic abstraction layer for spawning, managing, and rendering display entities. It allows developers to work with display entities through a consistent API, decoupled from specific server implementations.
     - **Engine Runtime:** The default implementation of the Glance API for supported platforms (e.g., **Spigot/Paper**, **Minestom**). This runtime handles the underlying processing required for rendering and managing entities.
   - Developers can:
     - Use the **Glance API** independently by creating their own custom implementation for a specific platform.
     - Leverage the **Engine Runtime** for out-of-the-box compatibility and functionality.
   - Features include:
     - Packet-based display entity management to reduce server thread load.
     - Optimized **asynchronous tracking** and **update handling** for entities, ensuring smooth performance even in high-demand scenarios.
     - Modular design allowing for platform-specific optimizations while remaining version-agnostic.
     - Support for both **Kotlin** and **Java**, with a functional programming approach for modern usability.

### 2. **Flare** (WIP)
   - A particle and VFX system built on **Glance API**.
   - Provides tools for creating stunning visual effects, including voxel based particles and effect models, and more.
   - Suitable for damage and other visual effects, environmental particles, and custom resource pack integrations.

### 3. **Impulse** (WIP)
   - A lightweight collision, mesh, and physics engine for display entities.
   - Enables realistic procedural animations, kinematics, and interactive collision mechanics.
   - Built to integrate seamlessly with Glance API and Flare.

### 4. **Visor** *(Name subject to change)* (WIP)
   - A debugging graphics framework for developers.
   - Offers tools to visualize lines, trajectories, 2D planes, collision boundaries, and other debugging visuals.
   - Includes potential for **real-time visual graphs** and **charts**, enabling developers to monitor and debug data, such as performance metrics, entity states, or gameplay mechanics, directly in-game.
   - Aims to simplify the development and troubleshooting of complex entity interactions and effects.

### 5. **Lens** *(Name subject to change)* (WIP)
   - A cinematics engine for creating immersive player and cutscene experiences.
   - Leverages Visor's debugging graphics and tools for designing camera paths, animations, and forced perspectives.
   - Enables developers to choreograph dynamic in-game cinematic scenes.

---

## Features

- **Version Agnostic:** Abstracts away server API specifics for compatibility across multiple platforms.
- **Performance Focused:** Optimized for async operations and minimal server thread load.
- **Modular Architecture:** Use only the libraries you need, with seamless integration between modules.
- **Extensible Design:** Build custom tools, visualizations, and systems using Glance FX as a foundation.
- **Developer-Friendly APIs:** Intuitive, modern APIs for both Java and Kotlin developers.

---

## Getting Started

### Requirements

- **Currently Supported Minecraft Server Platforms:** Paper, Spigot, or Minestom.
- **Minecraft Version:** 1.20.6+
- **Java Version:** Java 21+
- **Build Tools:** Gradle or Maven.

### Installation

> **Note:** This is placeholder information - Glance is still unreleased!

To integrate Glance FX Suite into your project, include the dependencies for the desired modules:

#### Gradle
```kotlin
dependencies {
    // Example 1: Glance API only (for custom implementations)
    implementation("com.glance:glance-api:1.0.0")

    // Example 2: Glance API with the Engine Runtime (default bundled package)
    implementation("com.glance:glance:1.0.0")

    // Optional Modules
    implementation("com.glance:flare:1.0.0") // Optional - For particle effects
    implementation("com.glance:impulse:1.0.0") // Optional - For physics and collisions
    implementation("com.glance:visor:1.0.0") // Optional - For debugging visuals
    implementation("com.glance:lens:1.0.0") // Optional - For cinematic tools
}
```

#### Maven
```xml
<dependencies>
    <!-- Example 1: Glance API only (for custom implementations) -->
    <dependency>
        <groupId>com.glance</groupId>
        <artifactId>glance-api</artifactId>
        <version>1.0.0</version>
    </dependency>

    <!-- Example 2: Glance API with the Engine Runtime (default bundled package) -->
    <dependency>
        <groupId>com.glance</groupId>
        <artifactId>glance</artifactId>
        <version>1.0.0</version>
    </dependency>

    <!-- Optional Modules -->
    <dependency>
        <groupId>com.glance</groupId>
        <artifactId>flare</artifactId>
        <version>1.0.0</version>
    </dependency>
    <dependency>
        <groupId>com.glance</groupId>
        <artifactId>impulse</artifactId>
        <version>1.0.0</version>
    </dependency>
    <dependency>
        <groupId>com.glance</groupId>
        <artifactId>visor</artifactId>
        <version>1.0.0</version>
    </dependency>
    <dependency>
        <groupId>com.glance</groupId>
        <artifactId>lens</artifactId>
        <version>1.0.0</version>
    </dependency>
</dependencies>
```

---

## Releases

The Glance FX Suite follows semantic versioning to provide clear and predictable updates. Check out the latest releases for each module below:

> **Note:** These are placeholder releases - Glance is still unreleased!

- **[Glance (API & Engine)](https://github.com/glance/glance/releases):** `v1.0.0`  
  - Initial release featuring the bundled API and Engine Runtime for Spigot/Paper and Minestom platforms.
  - Includes optimized asynchronous entity tracking and packet-based rendering.

- **[Flare](https://github.com/glance/flare/releases):** `v1.0.0`  
  - Particle and VFX system with configurable trails and custom resource pack support.

- **[Impulse](https://github.com/glance/impulse/releases):** `v1.0.0`  
  - Lightweight collision and physics system for display entities.

- **[Visor](https://github.com/glance/visor/releases):** `v1.0.0`  
  - Debugging graphics framework with support for lines, trajectories, collision visuals, and real-time graphs.

- **[Lens](https://github.com/glance/lens/releases):** `v1.0.0` *(Planned)*  
  - Cinematic engine for player-controlled camera paths and forced perspectives.
 
---

## Roadmap

### Current Development
- Focus on finalizing **Glance API** to provide a robust foundation.
- Create basic core features of **Visor** to assist in debugging of other module development
- Implement core features of **Flare**, including particle builder and configurable effects.

### Future Plans
- Expand **Impulse** to support dynamic physics-based interactions.
- Continue to develop **Visor** tools for visual debugging and collision visualization.
- Build basics for **Lens** to create cinematic experiences using advanced camera path animation.
- **In-Game Keyframing Editor**:
  - Develop an in-game keyframing editor initially tested and used for **Lens**, enabling developers to create and fine-tune camera paths and animations directly within the Minecraft environment.
  - Expand the keyframing system into a full-fledged in-game animation editor, combining its capabilities with the **Hephaestus Engine** for advanced procedural and custom animations.

---

## Contributing

Contributions are welcome! To get started:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with detailed information about your changes.

<!--Please refer to the [Contribution Guidelines](CONTRIBUTING.md) for more details.-->

---

## License

Glance FX Suite is licensed under the **MIT License**. <!--See the [LICENSE](LICENSE) file for more information.-->

---

## Contact

For questions, feature requests, or general discussions, join our community:
<!-- todo add twitter -->
- **Discord:** [Join Here](https://discord.gg/9Nz8GGG7b2)
- **GitHub Issues:** Open an issue in this repository.

We look forward to seeing the amazing creations you'll build with Glance FX!
