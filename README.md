# Outlawmallet

[Bloodmallet](https://bloodmallet.com/) is an amazing resource for aggregated simulation results comparing all aspects of a class in WoW. This uses the bloodmallet tools to produce a chart of talent builds ranked by dps with their "optimal" secondary distributions, to help fill the gap left by the lack of talent value simulations post-dragonflight.

This currently sims Dragonflight Season 4 talent builds and their secondary distributions - with currently comitted results visible [here](https://weswigham.github.io/outlawmallet).

How to use:
1. Ensure `docker` is installed, and there is a `bloodytools` tagged image containing [bloodytools](https://github.com/Bloodmallet/bloodytools) available in your environment.
2. Ensure `node` is installed (v14+, probably).
3. Run `node ./sim.js`
4. Wait paitently as thousands of simulation results and charts populate the `docs` folder - `docs/index.html` will update as new results roll in.

Configuration:
* `profile_gear.simc` contains the gear profile used for sims - since this does secondary distribution sims, these are just used to calculate total available stats (and apply unique effects like trinkets).
* `outlaw-talent-builds.simc` contains the talent builds that are "interesting" that we'll simulate and their human-readable name. This is by no means exhaustive - feel free to contribute more, so long as the variation is interesting (eg, makes a different dps talent choice than every other build).
These are in `simc` format mostly just so it's easy to copy & paste them into an advanced sim, and see how the results differ from what we calculate here with exhaustive secondary distribution sims.
