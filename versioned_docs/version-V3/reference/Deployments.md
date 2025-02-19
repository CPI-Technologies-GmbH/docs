---
id: deployments
title: Deployment Addresses
---

# Uniswap Contract Deployments

The latest version of `@uniswap/v3-core`, `@uniswap/v3-periphery`, `@uniswap/swap-router-contracts`, and  `@uniswap/v3-staker` are deployed at the addresses listed below. They are deployed at the same address on Ethereum mainnet, Optimism, Arbitrum, Polygon, and all testnets.

These addresses are final and were deployed from these npm package versions:

- [`@uniswap/v3-core@1.0.0`](https://github.com/Uniswap/uniswap-v3-core/tree/v1.0.0)
- [`@uniswap/v3-periphery@1.0.0`](https://github.com/Uniswap/uniswap-v3-periphery/tree/v1.0.0)
- [`@uniswap/swap-router-contracts@1.1.0`](https://github.com/Uniswap/swap-router-contracts/tree/v1.1.0)
- [`@uniswap/v3-staker@1.0.2`](https://github.com/Uniswap/v3-staker/tree/v1.0.2)

| Contract                           | Address                                      | Source Code                                                                                                                   |
| ---------------------------------- | -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| UniswapV3Factory                   | `0x1F98431c8aD98523631AE4a59f267346ea31F984` | https://github.com/Uniswap/uniswap-v3-core/blob/v1.0.0/contracts/UniswapV3Factory.sol                                         |
| Multicall2                         | `0x5BA1e12693Dc8F9c48aAD8770482f4739bEeD696` | https://etherscan.io/address/0x5BA1e12693Dc8F9c48aAD8770482f4739bEeD696#code                                                  |
| ProxyAdmin                         | `0xB753548F6E010e7e680BA186F9Ca1BdAB2E90cf2` | https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v3.4.1-solc-0.7-2/contracts/proxy/ProxyAdmin.sol                  |
| TickLens                           | `0xbfd8137f7d1516D3ea5cA83523914859ec47F573` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/lens/TickLens.sol                                       |
| Quoter                             | `0xb27308f9F90D607463bb33eA1BeBb41C27CE5AB6` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/lens/Quoter.sol                                         |
| SwapRouter                         | `0xE592427A0AEce92De3Edee1F18E0157C05861564` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/SwapRouter.sol                                          |
| SwapRouter02 (1.1.0)               | `0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45` | https://github.com/Uniswap/swap-router-contracts/blob/v1.1.0/contracts/SwapRouter02.sol                                          |
| NFTDescriptor                      | `0x42B24A95702b9986e82d421cC3568932790A48Ec` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/libraries/NFTDescriptor.sol                             |
| NonfungibleTokenPositionDescriptor | `0x91ae842A5Ffd8d12023116943e72A606179294f3` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/NonfungibleTokenPositionDescriptor.sol                  |
| TransparentUpgradeableProxy        | `0xEe6A57eC80ea46401049E92587E52f5Ec1c24785` | https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v3.4.1-solc-0.7-2/contracts/proxy/TransparentUpgradeableProxy.sol |
| NonfungiblePositionManager         | `0xC36442b4a4522E871399CD717aBDD847Ab11FE88` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/NonfungiblePositionManager.sol                          |
| V3Migrator                         | `0xA5644E29708357803b5A882D272c41cC0dF92B34` | https://github.com/Uniswap/uniswap-v3-periphery/blob/v1.0.0/contracts/V3Migrator.sol                                          |
| UniswapV3Staker (1.0.2)                     | `0xe34139463bA50bD61336E0c446Bd8C0867c6fE65` | https://github.com/Uniswap/v3-staker/blob/v1.0.2/contracts/UniswapV3Staker.sol                                          |

# Uniswap Pool Deployments

Every Uniswap pool is a unique instance of the `UniswapV3Pool` contract and is deployed at its own unique address. The contract source code of the pool will be auto-verified on etherscan. For example, here is the [ETH/USDC 0.3% pool](https://etherscan.io/address/0x8ad599c3a0ff1de082011efddc58f1908eb6e6d8) on Ethereum mainnet.

You can look up the address of an existing pool on [Uniswap Info](https://info.uniswap.org/#/) or by calling the [`getPool`](https://docs.uniswap.org/protocol/reference/core/interfaces/IUniswapV3Factory#getpool) function on the `UniswapV3Factory` contract.

```solidity
getPool("0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48", "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2", 3000)
```

# Wrapped Native Token Addresses

The Uniswap Protocol supports trading of ERC20 tokens. In order to swap a native asset like ETH (or MATIC on Polygon), the Uniswap protocol wraps these assets in an ERC20 wrapped native token contract. The protocol uses the following WETH9 addresses on Ethereum and WMATIC addresses on Polygon.

| Network          | ChainId   | Wrapped Native Token | Address                                      |
|------------------|-----------|----------------------|----------------------------------------------|
| Ethereum         | `1`       | WETH                 | `0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2` |
| Ropsten          | `3`       | WETH                 | `0xc778417E063141139Fce010982780140Aa0cD5Ab` |
| Rinkeby          | `4`       | WETH                 | `0xc778417E063141139Fce010982780140Aa0cD5Ab` |
| Goerli           | `5`       | WETH                 | `0xB4FBF271143F4FBf7B91A5ded31805e42b2208d6` |
| Kovan            | `42`      | WETH                 | `0xd0A1E359811322d97991E03f863a0C30C2cF029C` |
| Optimism         | `10`      | WETH                 | `0x4200000000000000000000000000000000000006` |
| Optimistic Kovan | `69`      | WETH                 | `0x4200000000000000000000000000000000000006` |
| Arbitrum One     | `42161`   | WETH                 | `0x82aF49447D8a07e3bd95BD0d56f35241523fBab1` |
| Arbitrum Rinkeby | `421611`  | WETH                 | `0xB47e6A5f8b33b3F17603C83a0535A9dcD7E32681` |
| Polygon          | `137`     | WMATIC               | `0x0d500B1d8E8eF31E21C99d1Db9A6444d3ADf1270` |
| Polygon Mumbai   | `80001`   | WMATIC               | `0x9c3C9283D3e44854697Cd22D3Faa240Cfb032889` |
