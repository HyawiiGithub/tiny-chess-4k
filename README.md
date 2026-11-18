# tiny-chess-4k

A chess engine in fewer than 4 KB of Python. A 0x88 board, alpha-beta with a transposition table, null-move pruning, late move reductions, killers and history, aspiration windows and a quiescence search, playing through the make.fun chess environment.

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/HyawiiGithub/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/HyawiiGithub/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

## Run it

It talks to the env at `MAKEFUN_ENV_URL` (`POST /game`, `POST /move`):

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python main.py
```

`main.py` is a self-unpacking entrypoint: it holds an LZMA stream of the readable source and unpacks it with the standard library, so the whole engine fits the 4,096-byte cap.
