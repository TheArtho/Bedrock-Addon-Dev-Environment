# Minecraft Bedrock Addon NodeJS Environment

This repository is a NodeJS project made to compile your **Typescript** and **Jsonc** code and deploy your addon code into MCBE.

---

## ⚙️ Requirements

- [Node.js](https://nodejs.org/) v18 or higher
- Minecraft Bedrock Edition (1.21.70+)
- Enable experimental gameplay & scripting in Minecraft
- A code editor like VS Code is recommended

---

## 📁 Project Structure

```
/Project
├── packs/
│   ├── Behavior/            → Output Behavior Pack files
│   ├── Resource/            → Output Resource Pack files
├── src/                     → TypeScript source code
├── ui/                      → Jsonc source code
├── buildconfig.json         → Contains the mod name (e.g., MyMod)
├── tsconfig.json
├── build.js                 → Build script
└── release.js               → Build release script
```

---

### 🛠 Compile & Deploy to Minecraft

```bash
# Install dependencies
npm install

# Compile TypeScript and copy output packs to the Minecraft dev folders
npm run build
```

### 🧹 Clean and full rebuild

```bash
npm run build:clean
```

### 🛠 Compile and build the mcaddon

```bash
npm run release
```

> The build script copies the packs into:
>
> ```
> %LOCALAPPDATA%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\
>     LocalState\games\com.mojang\
>         development_behavior_packs\Witchcraft BP
>         development_resource_packs\Witchcraft RP
> ```
