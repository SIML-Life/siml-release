# SIML Worm Agent Release

This release includes cross-platform binaries and a Godot visualizer for the SIML artificial worm simulation from the following paper:

[Artificial Intelligence is for Amateurs: SIML, Free Energy Principle and Cognogenics as the Foundations Toward the Birth of True Artificial Life](https://www.siml.life/research/Artificial-Intelligence-is-for-Amateurs)

---

## 🐛 Contents

- `siml-linux-x64` – Linux binary
- `siml-windows-x64.exe` – Windows binary
- `siml-apple-silicon` – macOS (M1+) binary
- `godot_visualizer.pck` – Godot 4.4.1 visualizer (platform-independent)
- `README.md` – You're reading it

---

# 🚀 Quick Start (Visualization Required)

## Step 1: Install [Godot 4.4.1](https://godotengine.org/download)

Make sure it's the **same version** used to export the `.pck` (e.g., Godot 4.4.1+).

## Step 2: Run the Visualizer

From terminal or PowerShell:

#### Linux
```bash
./Godot --main-pack godot_visualizer.pck
```
#### Windows
```
Godot.exe --main-pack godot_visualizer.pck
```
#### macOS
```
/Applications/Godot.app/Contents/MacOS/Godot --main-pack godot_visualizer.pck
```
You can also drag & drop `godot_visualizer.pck` onto the Godot executable.

## Step 3: Run the SIML Agent

### 🧠 SIML Command Line Usage

Once you've downloaded the correct `siml` binary for your platform, you can run the simulation via:

```bash
./siml-[platform] [OPTIONS]
```

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

For platform specific binaries, in a second terminal window:

#### Linux
```bash
./siml-linux-x64
```
#### Windows
```
.\siml-windows-x64.exe
```
#### macOS
```
chmod +x siml-apple-silicon
./siml-apple-silicon
```

### Logs
You’ll see logs like:
```
[SIML] Starting Capsule…
[SIML] Run 0 spawned at (x, y, z)
...

```

### 📜 License

This is a binary-only research release for reviewers and collaborators. Can not be used currently for an commercial purposes. There are headless formats and other flags that can be added for research.

All source code is withheld under internal license.

### 🔗 More Info

For citations, papers, or future inquiries, contact:

Author: Richard Everts

[Deep SIML Labs](https://www.siml.life)