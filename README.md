# SIML Worm Agent Release

![SIML Sample Video](images/siml-run.gif)

This release includes cross-platform binaries and a Godot visualizer for the SIML artificial worm simulation from the following paper:

[Artificial Intelligence is for Amateurs: SIML, Free Energy Principle and Cognogenics as the Foundations Toward the Birth of True Artificial Life](https://www.siml.life/research/Artificial-Intelligence-is-for-Amateurs)

---

## 🐛 Contents

You can download all the files in the [latest release](https://github.com/SIML-Life/siml-release/releases/tag/v.0.1).

- `siml-linux-x64` – Linux binary
- `siml-windows-x64.exe` – Windows binary
- `siml-apple-silicon` – macOS (M1+) binary
- `godot_visualizer.pck` – Godot 4.4.1 visualizer (platform-independent)
- `README.md` – You're reading it

---

# 🚀 Quick Start (Visualization Required)

--

### 🧠 Visualizer (Godot-based)

**macOS Only**
- Download and double click on `apple-silicon.zip`
- Right-click `.app` → "Open" → bypass Apple Gatekeeper if needed
- Extract both files
- In the command line, we need to set up sandbox to run the files with this command since we didn't pay $99 for an Apple Developer Account:
```
xattr -dr com.apple.quarantine siml-visualizer-macos.dmg
xattr -dr com.apple.quarantine siml-apple-silicon
```
- Double click the `siml-visualizer-macos.dmg` file, and click on the `godot-command` file that opens
- Requires macOS 12+ with Apple Silicon

**Linux and Windows**

#### Install [Godot 4.4.1](https://godotengine.org/download)

Make sure it's the **same version** used to export the `.pck` (e.g., Godot 4.4.1+).

| OS      | File                 | Instructions                       |
|---------|----------------------|------------------------------------|
| Linux   | `godot_visualizer.pck`     | `./path-to-Godot-executable --main-pack godot_visualizer.pck` |
| Windows | `godot_visualizer.pck` | `./path-to-Godot-executable.exe --main-pack godot_visualizer.pck` |

---

### ⚙️ SIML Binaries

Choose your platform and run the binary from the terminal:

| OS      | File                 | Instructions                       |
|---------|----------------------|------------------------------------|
| macOS   | `siml-apple-silicon` | `chmod +x siml-apple-silicon && ./siml-apple-silicon` |
| Linux   | `siml-linux-x64`     | `chmod +x siml-linux-x64 && ./siml-linux-x64` |
| Windows | `siml-windows-x64.exe` | Double-click to run or use PowerShell |

---

### Available Flags

| Flag               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `--record-mode`    | Output mode for recording simulation (`bit` or `rgb`). Default: `bit`.     |
| `--runs`           | Number of worms to simulate sequentially. Default: `1`.                    |
| `--use-memory`     | Load memory from previous agent run and persist schema learning.           |            |

#### Example: Run 10 worms with memory

```bash
./siml-[platform] --runs 10 --use-memory
```

The simulator will save a `.bin` file to record your runs, and start over with the saved `.bin` every time. If you want to start from scratch again, simply rename or remove the `.bin`. 


### Logs
You’ll see logs like:
```
[SIML] Starting Capsule…
[SIML] Run 0 spawned at (x, y, z)
...

```

### 📜 License

This is a binary-only research release for reviewers and collaborators. Can not be used currently for any commercial purposes. There are headless formats and other flags that can be added for research.

All source code is withheld under internal license.

### 🔗 More Info

For citations, papers, or future inquiries, contact:

Author: Richard Everts

[Deep SIML Labs](https://www.siml.life)
