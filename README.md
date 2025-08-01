
Raydagana - The Raydium fork


![ByU76BuyQtH6LGYSo1igre536Veep8otY4mNCD6Rbonk](https://github.com/user-attachments/assets/d15e9033-7ec8-4211-86de-61405f53cca9)


Raydium is a decentralized, on-chain automated market maker (AMM) built on the Solana blockchain. It operates using the “constant product” model and functions in a permissionless manner. What sets Raydium apart is its unique approach to liquidity distribution — it shares liquidity following the Fibonacci sequence through limit orders placed on OpenBook, Solana’s main central limit order book (CLOB).

Audit and developer documentation are available for further review.

Raydium-Amm-v3 is an open-sourced concentrated liquidity market maker (CLMM) program built for the Solana ecosystem.

**Concentrated Liquidity Market Maker (CLMM)** pools allow liquidity providers to select a specific price range at which liquidity is active for trades within a pool. This is in contrast to constant product Automated Market Maker (AMM) pools, where all liquidity is spread out on a price curve from 0 to ∞. For LPs, CLMM design enables capital to be deployed with higher efficiency and earn increased yield from trading fees. For traders, CLMMs improve liquidity depth around the current price which translates to better prices and lower price impact on swaps. CLMM pools can be configured for pairs with different volatility.

## Environment Setup

1. Install `Rust`

   ```shell
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   rustup default 1.81.0
   ```

2. Install `Solana `

   ```shell
   sh -c "$(curl -sSfL https://release.anza.xyz/v2.1.0/install)"
   ```

   then run `solana-keygen new` to create a keypair at the default location.

3. install `Anchor`

   ```shell
   # Installing using Anchor version manager (avm)
   cargo install --git https://github.com/coral-xyz/anchor avm --locked --force
   # Install anchor
   avm install 0.31.1
   ```

## Quickstart

Clone the repository and enter the source code directory.

```
git clone https://github.com/raydium-io/raydium-amm-v3
cd raydium-amm-v3
```

Build

```
anchor build
```

After building, the smart contract files are all located in the target directory.

Deploy

```
anchor deploy
```

Attention, check your configuration and confirm the environment you want to deploy.

# CPI

An example of calling clmm can be found [here](https://github.com/raydium-io/raydium-cpi-example/tree/master/clmm-cpi)

# License

The source code is [licensed](https://github.com/raydium-io/raydium-clmm/blob/master/LICENSE) under Apache 2.0.
