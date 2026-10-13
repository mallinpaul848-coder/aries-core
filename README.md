# ARIES Core — test starter

This repository contains an initial RTL simulation test and a separate AI endpoint smoke-test script.

## RTL simulation (Windows or Linux)

Install Icarus Verilog from https://steveicarus.github.io/iverilog/ . From the repository root run:

```sh
iverilog -g2012 -Wall -s tb_aries_sub_ns -o sim/aries_tb src/aries_sub_ns_core.v sim/tb_aries_sub_ns.v
cd sim && vvp aries_tb
```

The testbench writes `aries_sub_ns.vcd`. Its clock is only a simulation timebase; it does not prove physical 4 GHz operation.

## Hosted CI

The GitHub Actions workflow compiles and runs the simulation on pushes, pull requests and manual dispatch. Check the Actions tab for the actual result; no passing result is claimed before a run completes.

## AI endpoint smoke test

Set `ARIES_API_URL` to an actual OpenAI-compatible chat-completions endpoint and optionally set `ARIES_API_KEY` and `ARIES_MODEL`, then run `python software/smoke_test.py`. A single request is only a connectivity check, not a leaderboard or performance benchmark. Never commit API keys.

See `docs/TEST_STATUS.md` for validation limits.
