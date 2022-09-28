# wSAFE
### Putting the less back in permissionless.

Gnosis Safe recently launched the SAFE token, allowing users to claim tokens to Gnosis safe multisignature contract wallets, although these tokens are non-transferable until the DAO decides to allow transfers, as all tokens are unable to be sent from these contract wallets once claimed. The tokens are so locked until such a proposals executed, but this is Crypto, and we dont like being told what we can or can't do with our money, and so, we welcome you to wSAFE.

wSAFE is a simple to use wrapper for the multisignature contract addresses which takes ownership for the safe from the signers, with it's SAFE token balance, and represents the locked SAFE tokens with wSAFE. As the safe wallets are controlled by the wSAFE tokens main wrapper contract, and only spendable by the wSAFE wrapper contract as the only owner for the safe and it's locked tokens, these wSAFE tokens can be freely traded on the market as if they were the unlocked SAFE tokens, and will be redeemable for SAFE once it's unlocked.

## Steps to mint wSAFE
1. Signers to the safe (also known as owners) must claim the SAFE tokens to the safe, the details for which can be found at:
https://gnosis-safe.io/app/share/safe-app?appUrl=https://apps.gnosis-safe.io/safe-claiming-app&chainId=1

2. Signers must set the gnosis safe with the locked SAFE token balance to have a signature threshold for executing transactions set to 1.

3. Signers must set the address `0x0` as an owner for the safe.

4. A signer must then go to etherscan and use the `mintWSAFE(address target)` fn, setting the target as the desired location to send wSAFE to. This may be another gnosis safe address.

## Redemption
Tokens may be exchanged for SAFE with the wrapper once transfers for SAFE tokens are enabled. Steps will come later, but the fn redeem() may be used directly rather than needing a front end, once transfers are enabled, to burn wSAFE tokens for SAFE tokens.

## Use
These tokens may be used just like any ERC20 token, and may be swapped, used in lending markets, transfered to cold wallets or used for any other purpoe you see fit. We believe in people being able to spend their money, and so when people build walls, we build hot air balloons.

### A note on SAFE voting with wrapped SAFE balance
All safes will keep their selected representatives for their token balances. This allows the voting to be unaffected by trading and markets. Be aware this does allow nothing at stake risks, but given the allocations we feel this wont really be a problem. This has been chosen rather than us choosing as it allows the same decentralization as if there had been no wrapper and has lower risk.
