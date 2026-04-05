# Bingo Mixer — AI Onboarding

## Mandatory Dev Checklist

Before completing any task, verify all pass:

- [ ] `npm run lint` — no warnings or errors
- [ ] `npm run build` — clean TypeScript + Vite build
- [ ] `npm run test` — all tests green

## Tech Stack

React 19 · TypeScript 5.9 (strict) · Vite 8 · Tailwind CSS v4 (CSS-first `@theme` in `src/index.css`) · Vitest 4 + @testing-library/react · ESLint 9 · React hooks only (no state library)

## Architecture

`src/`: `App.tsx` (root) · `components/` (stateless) · `hooks/useBingoGame.ts` (all state + localStorage) · `utils/` (pure logic) · `data/questions.ts` · `types/index.ts` · `test/setup.ts`

**Data flow**: `useBingoGame` → `App` distributes via props → components render + fire `on*` callbacks upward.

## Conventions

- Functional components, named exports, props typed as `ComponentNameProps`
- Callbacks: `on*` prefix (`onSquareClick`, `onReset`, `onStart`, `onDismiss`)
- Utils are **pure & immutable** — never mutate, always return new arrays
- `useMemo` for computed values, `useCallback` for stable refs
- localStorage uses versioned schema (`STORAGE_VERSION`)
- PascalCase files/components, camelCase functions/hooks, UPPER_SNAKE_CASE constants
- Tailwind v4 utilities only (see `.github/instructions/tailwind-4.instructions.md`), tokens in `@theme` block
- Tests next to source, `describe`/`it` with Arrange-Act-Assert, mock `Math.random` for determinism

## Domain Model

- `BingoSquareData` — `{ id, text, isMarked, isFreeSpace }`
- `BingoLine` — `{ type: 'row'|'column'|'diagonal'|'corners', index, squares[] }`
- `GameState` — `'start' | 'playing' | 'bingo'`

**Flow**: start → 5×5 board (24 shuffled questions + center FREE SPACE) → mark squares → bingo on 5-in-a-row (rows, columns, diagonals) → modal → dismiss or reset

## Component Hierarchy

`App` → `StartScreen` | (`GameScreen` + `BingoModal` → `BingoBoard` → `BingoSquare[]`)
