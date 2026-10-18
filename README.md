# BrainArk

BrainArk is an EVM blockchain (chain ID **1236**) with its own native coin **BAK**, and a set of apps built on it:
real-world-asset tokenisation, a meme-coin launchpad, a self-custody wallet and a token sale.

## Network
| | |
|---|---|
| Chain ID | `1236` (`0x4d4`) |
| Native coin | BAK (18 decimals) |
| Public RPC | `https://rpc.brainark.online` |
| Explorer | https://explorer.brainark.online |
| Website | https://brainark.online · [Whitepaper (PDF)](https://brainark.online/BrainArk_Whitepaper_v1.0.pdf) |

Add it to a wallet: see [brainark-developer-docs](https://github.com/brainarkofficial/brainark-developer-docs) or use
`addBrainArkToWallet()` from [brainark-sdk](https://github.com/brainarkofficial/brainark-sdk).

## Apps
| App | What it does | URL |
|---|---|---|
| **BrainArk RWA** | Tokenise real-world assets as NFTs backed by staked BAK; marketplace, claims, staking | https://rwa.brainark.online |
| **MecoMark** | Meme-coin launchpad with bonding curves that graduate to a liquidity pool | https://mecomark.brainark.online |
| **BAKvault** | Self-custody wallet (browser extension, web, Android) with optional passcode-protected vaults | https://bakvault.brainark.online/app/ |
| **EPO dapp** | BAK token sale, airdrop and bridge | https://dapp.brainark.online |

## Main contracts (BrainArk, chain 1236)
| Contract | Address |
|---|---|
| RWA AssetRegistry (NFTs) | `0xFf76Ea2EED588D0bFAF5466Bd0F20C3D980bd95D` |
| RWA Marketplace | `0x5C1A47d5E813211025e6653099BAAc89E8DeF9C3` |
| RWA StakingManager | `0x3071300Ee44211E3401925636f0D4F3F11eb13f5` |
| RWA ClaimSystem | `0xd7497c50FDdA2A568D385F5780779d079B70fECc` |
| RWA Extensions | `0x32e5896381E8084Cd9177e9EEa68Fbc0411A5715` |
| BAKvault Factory V2 | `0x6609bC2cFe7f07D0382e0C7c32769A2c4A7A76Ef` |
| BAKvault Registry | `0xeE522abE623697dd89d34Eda32994e03DCaf61E8` |
| MecoMark MemeFactory | `0x05e0B9f29b9D870FaeBEa45b5607678F8F5FE1C2` |
| EPO (token sale) | `0x1Df35D8e45E0192cD3C25B007a5417b2235642E5` |
| BUSDT (bridged USDT) | `0x66702Bb4A3346f12EbAc4D63A4Cf440b378Dfa07` |

On BNB Smart Chain (56): WBAK `0x7079B3414aAAf317547d06b10628bC15d5f39Fa3` · BAKvault Factory V2 `0xCF6673EE463f23Db734FC3D8027F3A264acCdea0`.

## Admin control
Admin roles of the RWA contracts, and ownership of the MecoMark MemeFactory and the EPO contract, are held by a
**2-of-3 multisig (Safe)**: `0xA1b028047E0977088E481b7256Ce6cBF9fd7fe01`. Upgrades or admin actions need two separate signers.

## Source code & security
- Verified contract source (rebuilt and compared byte for byte with the chain):
  [brainark-contracts](https://github.com/brainarkofficial/brainark-contracts).
- Found a vulnerability? Please report it privately: **Security → Report a vulnerability** on brainark-contracts.
