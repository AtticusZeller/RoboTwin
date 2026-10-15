# RoboTwin Agent Guide

RoboTwin 2.0 is a SAPIEN-based bimanual manipulation benchmark (default embodiment: Aloha-AgileX). Read
`README.md` and the code under `envs/` before changing anything; the online documentation is authoritative
when it disagrees with the README.

This checkout is used as a simulator: other repositories import `envs/` and drive tasks through
`setup_demo`, `get_obs`, `take_action`, `check_success`, and `close_env`. Keep local changes minimal so the
`workspace` branch stays close to upstream `main`.

The simulator needs its own Python 3.10 environment (`scripts/requirements.txt`, NumPy 1.x ABI), a GPU
with Vulkan for rendering, and CuRobo for the expert planner. Assets (`assets/embodiments`,
`assets/objects`, `assets/background_texture`) are downloaded separately and are not tracked.

Do not treat a source checkout as evidence that rendering, planning, or evaluation works on the current
machine. Report the checks actually run, the machine, and the GPU used.
