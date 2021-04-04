# xSpaceFinance
Config files for my GitHub profile.
https://xspace.finance
We audited xSpace's token contract contract at 0xad90c05bc51672eedfee36e58b3ff1a78bbc146d on the Binance Smart Chain mainnet.
Overview of the Contract:
The total supply of the token is set to one quadrillion.
No mint or burn functions are present; though the circulating supply can be reduced by sending tokens to the 0x..dead address, if desired.
As of the date of this report, ~30% of the token's supply has been sent to the 0xdead address. Pancakeswap holds ~28% of the token's supply as liquidity. The next largest holder has ~3%.
92% of liquidity has been locked with DxSale.

xSpace's code implements and builds upon the fee-resitribution features pioneered by Reflect Finance.
Users who hold tokens will automatically receive a portion the fees from a transaction tax on each transfer.
A portion of the fee charged on transactions is stored in the contract and, once a threshold value is met, used to fund PancakeSwap liqudity.
Liquidity-adds are funded by selling half of the tokens collected as fees, pairing the received ETH with the token, and adding it as liquidity to the BNB pair.

There is a transfer limit of 5 tillion tokens per transaction.
The owner of the contract can exclude and include users from transfer fees, update the maximum transaciton amount, update the fee percentages and update how the fees are allocated.
Ownership has been renounced, so none of these variables can be changed from their current state.
Some functions could have been declared external instead of public to save some gas, but as this is already deployed this is merely informational.
The contract utilizes SafeMath libraries to prevent overflows along with following the BEP20 standard.

Audit Findings Summary
No security issues were identified in our analysis.
Date: April 1st, 2021
