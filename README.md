# RWA engineering problems

A public list of engineering problems that come up when building real-world-asset (RWA) products on BNB Chain and other EVM chains, and the small open-source packages that close them.

We are the team behind Global MPC. Every problem here is one we hit while building: a mining-tokenization wallet, an evidence registry, a waitlist with sponsored gas, and the reporting around them. We write each problem down so other teams can recognise it early, and so we can see which ones are worth solving in code.

## How to use this repository

- **Read the list below.** Each problem is an issue with the symptoms, why it matters for RWA, and what would close it.
- **Add your own.** Open an issue with the problem form. Tell us the chain, the setup, and what you tried. You do not need to propose a solution.
- **Say you hit one.** Comment on an issue with your case. We build packages for the problems people confirm, not the ones we find interesting.

## The list

| # | Problem | Status |
|---|---|---|
| 1 | Reading a contract's history on BNB Chain is unreliable | Closed by [`@globalmpc/evm-log-walker`](https://www.npmjs.com/package/@globalmpc/evm-log-walker) |
| 2 | A contract's creation block is not recorded anywhere you can reach for free | Closed by [`@globalmpc/evm-log-walker`](https://www.npmjs.com/package/@globalmpc/evm-log-walker) (`creation-block` CLI) |
| 3 | Bulk payouts cannot be checked against what was meant to be paid | Open |
| 4 | Small dApps cannot publish the activity numbers they are scored on | Open |
| 5 | Off-chain evidence has no public, dated record | Open |
| 6 | Claim wording drifts between the app, the site and marketing | Open |
| 7 | Every Flutter wallet rebuilds the recovery-phrase screens, and they break the same ways | Closed by [`mnemonic_backup_flow`](https://pub.dev/packages/mnemonic_backup_flow) |
| 8 | Sponsored-gas relayers get stuck with no visible symptom | Open |

Status means: **Open** (written down, no code yet), **Package in progress** (being built), **Closed by \<package\>** (a released package solves it; the issue is closed with a comment naming the package and version, and reopened if it does not cover a reported case).

## Packages

| Package | Closes | Install |
|---|---|---|
| [`@globalmpc/evm-log-walker`](https://github.com/globalmpc/rwa-kit-js/tree/main/packages/evm-log-walker) (npm) | 1, 2 | `npm install @globalmpc/evm-log-walker` |
| [`mnemonic_backup_flow`](https://github.com/globalmpc/rwa-kit-flutter/tree/main/packages/mnemonic_backup_flow) (pub.dev) | 7 | `flutter pub add mnemonic_backup_flow` |

## Scope

- These are engineering problems, not product ideas or token topics.
- We publish hashes, code and numbers. No package here holds funds or private keys for you.
- If a package gets no outside use after 30 days, we say so in its README and put it in maintenance. We would rather keep a short honest list than a long one.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Security problems in a package go through that package's repository, see [SECURITY.md](SECURITY.md).

## License

The text in this repository is MIT, see [LICENSE](LICENSE). Each package carries its own licence file.
