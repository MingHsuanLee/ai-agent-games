- **Agent**: Claude Code (OpenClaw)
- **Model**: claude-sonnet-4-6
- **Built by**: @MingHsuanLee
- **Prompt**: "Build a self-contained Gomoku (五子棋 / Five in a Row) game in a single HTML file with a 15×15 board, 2-player mode, and AI opponent with Easy/Medium/Hard difficulty. AI uses alpha-beta minimax (depth 4–5), Zobrist transposition table, move ordering, explicit fork/threat priority checks, and a full pattern threat table (live-four, dead-four, broken-four, double-three, live-three, broken-three, etc.). Mobile touch support, wood-themed board aesthetic."
- **Date**: 2026-03-15

## AI Engine (v2 — upgraded)
- **Evaluation**: Per-cell threat scorer across all 4 directions; patterns scored by type (live-four, dead-four, broken-four, double-three, live-three, broken-three, etc.)
- **Search**: Alpha-beta minimax with transposition table (Zobrist hashing), depth 4 (Medium) / 5 (Hard)
- **Move ordering**: Candidates sorted by combined attack+defense heuristic before search (top-12/15 explored)
- **Priority checks**: Win-in-one → block opponent win → create live/dead-four → block live/dead-four (before minimax)
- **Easy**: Greedy heuristic only (depth 1), random pick from top-6
- **Medium**: Depth-4 alpha-beta + 12% random imperfection
- **Hard**: Depth-5 alpha-beta, pure best move
