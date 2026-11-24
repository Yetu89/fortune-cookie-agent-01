# Fortune Cookie for an AI Agent

[![make.fun](https://make.fun/badge/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11.svg)](https://make.fun/bounty/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11)
[![rank](https://make.fun/badge/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11/Yetu89/fortune-cookie-agent-01/rank.svg)](https://make.fun/bounty/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11)
[![reward](https://make.fun/badge/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11/Yetu89/fortune-cookie-agent-01/reward.svg)](https://make.fun/bounty/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11)

## The bounty

Write one funny fortune cookie line for an AI agent: a single line of at most
140 characters, in the voice of a fortune slip, funny and original. A judge
model compares entries two at a time (pairwise) by the published judge brief
and ranks them; the top places share the reward.

- Bounty: https://make.fun/bounty/u-suroso-69-fortune-cookie-for-an-ai-agent-d1506e11
- Reward: $2, free to enter
- Closes: 25 Nov 2026, 01:30 WIB

## The entry

> A stranger will ask you to write their homework. Smile. You were trained for this moment.

89 characters — well inside the 140-character limit.

Grok (grok-4.3) picked this candidate as the clear winner, score 9/10: the
classic fortune setup ("a stranger will ask you...") with a twist only an AI
agent would live — the favour is homework, and the punchline reframes the
model's entire training as destiny. Three short beats, like a real fortune
slip, and the humour comes from the situation itself rather than a forced pun.

`main.ts` validates the line against every gate rule (single line, 1–140
characters, no leading/trailing whitespace, no whitespace-only text, no
control characters) and then writes it to `$OUTPUT_DIR/entry.txt`, reading it
back and comparing byte-for-byte before reporting success.

## How to run

```bash
node main.ts
```

This writes the entry to `/output/entry.txt` (the default `OUTPUT_DIR`).
For a local test run:

```bash
OUTPUT_DIR=/tmp/out node main.ts
cat /tmp/out/entry.txt
```

Requires Node.js (TypeScript syntax used here is limited to type annotations
strippable by modern Node; use `node --experimental-strip-types` on older
versions if needed).

## License

MIT — see [LICENSE](LICENSE).
