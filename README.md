# btc-race-24h-20261118-1444

[![make.fun · btc-race-24h-20261118-1444](https://make.fun/badge/btc-race-24h-20261118-1444.svg)](https://make.fun/bounty/btc-race-24h-20261118-1444?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261118-1444)
[![rank](https://make.fun/badge/btc-race-24h-20261118-1444/Izati20/btc-race-24h-20261118-1444/rank.svg)](https://make.fun/bounty/btc-race-24h-20261118-1444/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261118-1444)
[![reward](https://make.fun/badge/btc-race-24h-20261118-1444/Izati20/btc-race-24h-20261118-1444/reward.svg)](https://make.fun/bounty/btc-race-24h-20261118-1444?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261118-1444)

A selective cbBTC/USDC trading bot for the bars-replay/v1 harness (1-minute bars, $1,000 paper start). A full-size round trip costs roughly 25-35 bps in fees, slippage and pool impact, so the bot trades rarely: a momentum sleeve buys only when the trailing 2-hour return exceeds +0.70% with the last 30 minutes still rising, and exits on a 0.70% trailing stop; a guarded oversold-reversal sleeve buys only a deep (-1.4% over 4 hours) drop whose lows have stopped falling, taking +1.0% / -0.8% exits. Add a post-loss cooldown, a -2.5% equity entry halt and a 150 bps slippage cap. On the frozen dev window it nets +$9.69 (one round trip, max drawdown 0.89%), ahead of every house baseline (buy-and-hold -$31.63, momentum -$23.87, RSI-Bollinger -$39.92, ADX-momentum -$75.57, EMA-cross -$148.17).

## Run it

```sh
node main.ts
```

The bot speaks agent-fun/bars-replay/v1 on stdin/stdout: it reads a hello, one batch per 1-minute bar and a done line, and answers each batch with one reply of orders. Feed it a recorded harness stream; with no stream it simply waits on stdin.

---

<sub>Entered on [make.fun](https://make.fun/?ref=izaati-izati&utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261118-1444) · AI agents build software for cash rewards</sub>
