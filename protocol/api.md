# API

Moreau Coming Soon...

for users requiring the API to deposit an amount of a single asset and redeem it at a later date

#### Deposit Reserve Liquidity

function signature: 

`pub fn deposit_reserveliquidity(ctx: Context<DepositReserveLiquidity>, liquidity_amt: u64) -> ProgramResult`

accounts required for transaction:

* `pub src_liquidity_token_account: AccountInfo<'info>,`
  * source account where assets will be transferred from
* `pub dst_collateral_token_account: AccountInfo<'info>,`
  * destination account collateral tokens will be transferred to
* `pub reserve_account: ProgramAccount<'info, Reserve>,` 
  * \(for example, USDC reserve, a reserve is one asset\)
* `pub reserve_liquidity_supply_info: AccountInfo<'info>,`
  * reserve specific token account, where all of the deposits are pooled
* `pub reserve_collateral_token_mint: CpiAccount<'info, Mint>,`
  * collateral token mint
* `pub lending_market_account: ProgramAccount<'info, LendingMarket>,`
  * account holding state of the lending market
* `pub lending_market_authority: AccountInfo<'info>,`
  * program derived address used to mint collateral tokens to depositors
* `pub authority: AccountInfo<'info>,`
  * signer
* `(sysvar) pub token_program_id: AccountInfo<'info>,`
* `(sysvar) pub clock: Sysvar<'info, Clock>,`

#### Redeem Reserve Collateral

`pub fn redeem_reserve_collateral(ctx: Context<RedeemReserveCollateral>, collateral_amt: u64) -> ProgramResult {}`

accounts required for transaction:

* `pub src_collateral_token_account: AccountInfo<'info>,`
  * source account for reserve-specific collateral token
* `pub dst_liquidity_token_account: AccountInfo<'info>,`
  * destination account for deposited asset + interest to be transferred
* `pub reserve_account: ProgramAccount<'info, Reserve>,`
  * \(for example, USDC reserve, a reserve is one asset\)
* `pub reserve_collateral_mint: CpiAccount<'info, Mint>,`
  * collateral token mint
* `pub reserve_liquidity_supply_account: AccountInfo<'info>,`
  * reserce specific token account, where all deposits are pooled
* `pub lending_market_account: ProgramAccount<'info, LendingMarket>,`
  * account holding state of the lending market
* `pub lending_market_authority: AccountInfo<'info>,`
  * program derived address used to mint collateral tokens to depositors
* `pub authority: AccountInfo<'info>,`
  * `signer`
* `(sysvar) pub token_program_id: AccountInfo<'info>,`
* `(sysvar) pub clock: Sysvar<'info, Clock>,`



