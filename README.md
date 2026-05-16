# Watt — The Lean Desktop Project

A meta-landing page for the two sister desktop suites by Geir Isene:

- **[CHasm](https://github.com/isene/chasm)** — x86_64 assembly: shell,
  terminal, tiling WM, status bar, file viewer, font rasterizer,
  screen locker. The bedrock.
- **[Fe₂O₃](https://github.com/isene/fe2o3)** — Rust on a shared TUI
  library (`crust`): editor, file manager, web browser, messaging
  hub, calendar, astronomy, movies, music, color picker, battery
  triage. The application layer.

Together they form a complete Linux desktop that idles at ~3.6 W
on a Dell XPS 14 — roughly 19 hours on a 70 Wh battery, screen on.

## Why "Watt"?

Because a watt is the unit being optimised. Every loop, every timer,
every fork-on-a-timer is measured in watts the battery doesn't give
back. Watt is the umbrella under which both suites enforce the same
three rules, in priority order:

1. **No wasted CPU cycles.** Gate every feature so its code path is
   fully cold when not in use.
2. **Lightning fast.** Microsecond startup, instantaneous user
   feedback. No interpreters in the hot path.
3. **More battery life.** Polling, waking, and forking on a timer
   are suspect. Prefer filesystem watches, `select`, blocking reads.

## Live page

<https://isene.org/watt/>

## License

Unlicense (public domain). Borrow or steal whatever you want.
