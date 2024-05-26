# prodigyHackathon

“./jerichoProtocol” is a decentralized overcollateralized stableCoin that gives yield to the users just by holding the token thanks to putting the collateral on liquidStaking. It also offers other 3 ways of yield generation on the same invested capital, for up to a total of 4 methods.



# // "Idea" ////////////////////////////////////////////////////////////
The concept behind this project emerged in response to practices by Tether, the pioneering entity in centralized, fiat-backed stablecoins. 
Tether traditionally invests the fiat collateral in treasury bonds and various financial instruments, retaining the generated revenue rather than distributing it among the stablecoin holders. 
This project seeks to eliminate the centralized intermediary by directly distributing the revenue accrued from the stablecoin’s collateral to its holders, thereby fostering a more equitable and decentralized financial ecosystem.


# // "Architecture" ////////////////////////////////////////////////////
  * liquidStaking contract interacts with the parachainRuntime to enable runtime api calls from the contract.
 
  * liquidStablecoinVault contract locks the liquidStakingTokens collateral, controls the minting of the augmeaStablecoin and uses the diaPriceOracle to calculate how much     liquidStakingTokens equals to 2 usd to mint 1 augmeaStablecoin.
    
  * wrappedDot contract emits PSP22 tokens by locking dot asset.
    
  * augmeaLendingProtocol contract uses the augmeaStablecoin as asset that lenders use, wrappedDot that borrowers lock as collateral and diaPriceOracle to calculate the liquidation price of positions and borrowing power of the collateral.


  * Deployed smartContracts addresses on alephZero testnet:
    * liquidStaking: 5DopMs1Pw77C33faHXdmtu3D7w1PEDEoLBYu8p2KBWGkJ9kN
    * jerichoStablecoin: 5Cq7y4e55kXPkYpgVfSQZ8nJq8Ypa1SxbZJBLtrugAnaa8BS
    * liquidStablecoinVault: 5GjYSmTeEyDaG2TmdSdf2MAk6Kj4b5yYbo2Mb4nVPUCZUFbJ
    * wrappedDot: 5HJmYjCvUGEMMPWVMiFiwQkk9zck2dJv9nQ1D6rjtPvFk4vU
    * jerichoLendingProtocol: 5DzEbBGRqKURbiWggKs5kKMRaJT49y93KFDbXa8E4skT9L9r
    * sharesToken: 5HHxrtTXbXy7zpMVukeAMvNUg2JfAQYa4k4g1fqq7gVtpWAB
   


# // "importantTecnhicalDetails" ///////////////////////////////////////
* Uses the parachainRuntime exposed API to implement liquidStaking.
* The stablecoinVault issues one jerichotablecoin for every 2 usd in value used as collateral.
* Uses a wrappedPsp22Token for the dot asset in order to interact with smartContracts.
* The stablecoin has a fee on the staking and keeps it as extra collateral in order to try to keep the peg stable during extreme market volatily.


# // "projectGoals" ////////////////////////////////////////////////////
* Promote securing the blockchain and enhancing decentralization through liquid staking.
* Create a stablecoin with mechanics to preserve the peg in any type of market situation.
* Offer yield maximization on the invested capital.


# // "yieldMehods" /////////////////////////////////////////////////////
* liquidStaking
* liquidStakingToken flashLoans through vault
* Providing liquidity to lendingProtocol
* jerichoStablecoin flashloans through lendingProtocol available liquidity reserves


# // "potentialUsers" //////////////////////////////////////////////////
* Every single user on the dotSama ecosystem that seek to be protected from assets volatility.
* deFi projects that need the integration of a stable asset for their protocol mechanics: DEXs & lendingProtocols.


# // "How impactful and useful is the dotSama ecosystem?" //////////////
* Flow liquidity from the traditional investors to the blockchain ecosystem, which is measured by billions.
* Represent a really solid asset on the polkadot ecosystem that functions as a store of value, just like dot.
* Work as a deFi primitive that serves as one of the foundations to build mature deFi protocols and produce more use cases and models
 
