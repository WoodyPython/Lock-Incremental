# Lock Incremental

Lock Incremental is an active incremental browser game inspired by the _Pop the Lock_ arcade game. Time each input to hit targets around a spinning lock, earn Points, buy upgrades, and complete increasingly difficult runs for Medals.

## [Play Lock Incremental](https://woodypython.github.io/Lock-Incremental/)

The game runs entirely in the browser. Progress is saved locally, with save import and export tools available from the Settings tab.

## Gameplay loop

The core loop combines a timing challenge with incremental progression:

1. **Start a run.** Click or tap the lock—or press <kbd>Space</kbd> or <kbd>Enter</kbd> while it is focused or hovered—to place the first target. Starting does not count as a hit.
2. **Hit the target.** Activate the lock when the rotating bar overlaps the colored target on the ring.
3. **React to the reversal.** A successful hit awards Points, moves the target, and reverses the bar's direction. As the run continues, the bar accelerates and targets appear closer together.
4. **Avoid a miss.** Activating too early or letting the bar pass the target ends the run. After a short cooldown, the lock returns to its idle state and is ready for another attempt.
5. **Hit the Jackpot.** Land all 50 targets to complete the run. A Jackpot awards a bonus equal to 25% of the run's base target value and grants a Medal.
6. **Invest and repeat.** Spend Points on various upgrades.

**Lifetime Point goals reveal more of the game as you progress.** You dont start with all features unlocked!

## Controls

| Action        | Mouse / touch         | Keyboard                             |
| ------------- | --------------------- | ------------------------------------ |
| Start a run   | Click or tap the lock | <kbd>Space</kbd> or <kbd>Enter</kbd> |
| Attempt a hit | Click or tap the lock | <kbd>Space</kbd> or <kbd>Enter</kbd> |

## Progression and saves

- Buy repeatable and one-time upgrades with Points.
- Reach lifetime Point goals to reveal new content.
- Save manually or configure autosaving from Settings.
- Export saves to the clipboard or a file, and import them on another browser.
- No account, server, or offline rewards are required; save data stays in browser storage unless exported.

## Development

This project uses Vite, strict vanilla TypeScript, plain CSS, Canvas 2D, `break_infinity.js`, Vitest, and Playwright.

```bash
npm install
npm run dev
```

Useful validation commands:

```bash
npm run format:check
npm run lint
npm run typecheck
npm run test
npm run build
npm run test:e2e
```

Production builds are deployed to GitHub Pages from the `main` branch through GitHub Actions.
