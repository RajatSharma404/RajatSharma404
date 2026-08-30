# ChessEval ♟️⚡

> High-performance chess evaluation and board position analysis platform powered by Stockfish 17 (WASM) and AI engine.

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev/)
[![WebAssembly](https://img.shields.io/badge/WebAssembly-Stockfish_17_WASM-654FF0?style=for-the-badge&logo=webassembly&logoColor=white)](https://webassembly.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

## 📌 Overview

**ChessEval** is a browser-native chess analysis workstation that brings the computational depth of **Stockfish 17** directly to your browser via WebAssembly (WASM). Run grandmaster-grade positional evaluations, calculate principal variations, and analyze critical blunder checkpoints with zero server latency.

---

## ✨ Features

- **⚡ Client-Side Stockfish 17 WASM**: Runs directly on web workers using WebAssembly and SIMD acceleration — zero server compute needed, unlimited evaluations.
- **📊 Real-Time Dynamic Evaluation Bar**: Live centipawn (+/-) evaluation and forced mate depth calculations with smooth animations.
- **🎯 Move Quality & Blunder Detection**: Visual move categorization (Brilliant, Best, Good, Inaccuracy, Mistake, Blunder).
- **📋 FEN & PGN Import / Export**: Instant support for standard FEN positions, full PGN match parsing, and interactive move history scrubbers.
- **🧩 Interactive Analysis Board**: Flip board, customize piece sets/themes, visualize best-line arrows, and explore tactical branches in sandbox mode.

---

## 🖼️ Preview

<!-- Screenshot placeholder -->
```
+-------------------------------------------------------------------------------+
|  [+] +1.84 (Depth 22)                                                         |
|  [8] [r] [ ] [b] [q] [k] [b] [n] [r]   | Analysis & Best Line:                |
|  [7] [p] [p] [p] [ ] [p] [p] [p] [p]   | 1. e4 e5 2. Nf3 Nc6 3. Bb5 a6        |
|  [6] [ ] [ ] [n] [ ] [ ] [ ] [ ] [ ]   | Best Move: 4. Ba4 (Score: +0.45)     |
|  ...                                   | Stockfish 17 WASM · 1,420 kN/s       |
|  [1] [R] [N] [B] [Q] [K] [B] [ ] [R]   |                                      |
|      [a] [b] [c] [d] [e] [f] [g] [h]   | [Flip] [Reset] [Load FEN] [Export]   |
+-------------------------------------------------------------------------------+
```

---

## 🛠️ Tech Stack

- **Frontend Core**: React 19, TypeScript
- **Engine Core**: Stockfish 17 compiled to WebAssembly (`stockfish.js` / WASM)
- **Styling & UI**: Tailwind CSS, Lucide Icons, Chessboard UI primitives
- **Game Logic**: `chess.js` for rule validation, move generation, and legal state tracking

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm / pnpm / yarn

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/RajatSharma404/Chess-Eval.git
   cd Chess-Eval
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the development server**:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to `http://localhost:3000`.

---

## 📂 Architecture

```
Chess-Eval/
├── public/
│   ├── stockfish/        # Stockfish 17 WASM binaries & worker scripts
│   └── pieces/           # Vector piece graphics
├── src/
│   ├── components/       # Board, EvalBar, MoveHistory, EnginePanel
│   ├── engine/           # WASM Worker bridge & UCI protocol handler
│   ├── types/            # FEN, Move, and Eval types
│   └── App.tsx           # Main workspace layout
├── package.json
└── tsconfig.json
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Crafted with ❤️ by <a href="https://github.com/RajatSharma404">Rajat Sharma</a>
</p>
