# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/on1force/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/on1force/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python: alpha-beta search with quiescence, a transposition table and null-move pruning, on a 10x12 board that turns around after every move. It searches to a fixed node budget, never a clock, so the same position always gets the same move.

## Why main.py looks garbled

It is packed: two lines of Python around an lzma-compressed copy of the readable source, so the whole engine fits the bounty's 4,096-byte cap. GitHub shows the compressed bytes as random characters. To print the source:

```sh
python3 -c "import ast,lzma;s=open('main.py',encoding='l1').read();print(lzma.decompress(ast.literal_eval(s.split('decompress(')[1].rsplit('.encode',1)[0]).encode('l1')).decode())"
```

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=mnrh6w1h&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
