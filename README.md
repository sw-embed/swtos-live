# SWTOS live terminal demo (stable)

The **stable public build** of the SWTOS terminal demo:

### https://swtos.softwarewrighter.com/

SWTOS is a preemptively multitasking microkernel for small CPUs, inspired by
MINIX IPC principles. This demo runs it on an emulated MakerLisp COR24 -- a
24-bit RISC soft CPU for Lattice FPGAs -- driven from a tiled terminal
frontend, entirely in your browser (WebAssembly). No server, nothing to
install.

Press `Ctrl-B` then `?` for the command list. Panes, zoom, focus and
copy-mode scrolling are all prefix commands, exactly as on a real terminal.

If your browser claims the prefix key, the **commands** button above the
screen offers the same commands to a mouse.

## What this repository is

This repo holds ONLY the built, deployed site for the stable channel, so the
public URL stays put while development continues. It is published deliberately
from the source repository, not on every push:

- **Source code:** https://github.com/sw-embed/web-sw-tos
- **Nightly build:** https://sw-embed.github.io/web-sw-tos/ (moves on every
  push -- for development, not for sharing)
- **Stable build (here):** https://swtos.softwarewrighter.com/ (moves only when
  a release is cut)

Each deploy is produced by `scripts/release-stable.sh` in the source
repository, which runs the full test gate and refuses a dirty tree before it
builds. `build-info.json` records the source commit this build was cut from,
the SWTOS image it runs, and marks the channel `stable`.

The site is rebuilt for this repository rather than copied: the nightly build
bakes the `/web-sw-tos/` project-pages subpath into every asset URL, and this
one serves from the domain root.

## Copyright

Copyright (c) 2026 Michael A Wright

## License

MIT. See [`LICENSE`](LICENSE) and [`COPYRIGHT`](COPYRIGHT).
