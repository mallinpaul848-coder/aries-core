# ARIES test status

- RTL and testbench files committed: this commit sequence.
- Hosted simulation: status must be checked in the GitHub Actions tab after workflow file is added.
- AI endpoint smoke test: NOT RUN until a real endpoint URL/model ID is configured.
- Physical 4 GHz operation: NOT VERIFIED; requires a target device, synthesis, timing constraints and static timing analysis.
- External certification/public leaderboard result: none claimed.

A passing simulation checks RTL behavior against a cycle-by-cycle reference model. It is not hardware certification.
