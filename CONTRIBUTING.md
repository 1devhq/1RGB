# Contributing to 1RGB

Thank you for considering contributing to 1RGB! Developing this project has made me question my life choices multiple times. By contributing, you agree to question yours too. 

1RGB is designed as an open and performance-focused ecosystem. Contributions are welcome in all areas outlined in our `ROADMAP.md`.

---

## Development Areas

Our ecosystem is strictly divided into three distinct layers based on language and responsibility:

### 1. Core Engine (C & Assembly)
*   **Responsible for:** RGB processing, low-level OS/HID communication, device abstraction, and ultra-high performance.
*   **Guidelines:** No unchecked pointers (if you allocate it, you free it). If you write black magic in Assembly or low-level C to squeeze out frames, leave a clear comment explaining *why* and *how* it works.

### 2. Effects (Lua)
*   **Responsible for:** Lighting animations, visual effects, math-heavy curves, and user-created content.
*   **Guidelines:** Performance is king. RGB effects need to render at high refresh rates. Keep your Lua scripts tightly optimized and use the official Core Effect API.

### 3. Plugins (Python)
*   **Responsible for:** Game state telemetry (health, ammo, damage events), external applications, and third-party data providers.
*   **Guidelines:** Non-blocking logic. Python plugins must run asynchronously or in separate threads so they never stutter the main C rendering engine.

### 4. Platform Support & Documentation
*   We need help expanding across macOS, Windows, Linux, and other experimental platforms. Keep platform-specific code strictly isolated.

---

## Pull Requests

When opening a Pull Request against the `main` or `dev` branch, please make sure to include:

*   **Description:** A clear explanation of what changes you made and which Phase of the roadmap they address.
*   **Testing Information:** How you tested your code (and on what hardware/OS).
*   **Visuals:** Screenshots or videos if your changes affect the UI or introduce a new Lua lighting effect.

---

## General Guidelines, Ownership & License

*   Keep code readable and document all new features or APIs.
*   Avoid breaking existing core interfaces.
*   **Code Ownership:** By submitting a Pull Request, you grant the project owner a worldwide, non-exclusive, perpetual, royalty-free, irrevocable license to use, modify, distribute, and sublicense your contributions. The original project maintains overall ownership, intellectual property rights, and copyright control over the 1RGB codebase.
*   **License:** By contributing, you agree that your contributions will be licensed under the **GPLv3 License**.
