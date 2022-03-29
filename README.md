# Hera-Docs
Documentation for the Hera Token Project 

Hera Smart Contract:
The Hera Smart Contract is a derivative of the Titano V1 contract. It implements new features while also adding efficiency and sustainability to the contract. This document outlines the changes that were made to the Titano V1 smart contract to produce the Hera Token contract.

Tockenomics::
Initial Supply: 	      280,000
Maximum Supply: 	2,800,000,000
Prelaunch:		          169,965
Liquidity: 		           77,999
Funding: 		              32036

Fee Structure::
Liquidity: 		      3.5%
Treasury: 		      3%
Risk Free Value: 	  4%
Blackhole:		      2.5%
Dividend Buy Fee: 	3%
Dividend Sell Fee: 	5%
Sell Fee: 		      2%	  Reduced the sell fee here as hodling will be incentivized by BUSD reward

Total Buy Tax = Liquidity + Treasury + RFV + Firepit + Dividend Buy Fee = 16%
Total Sell Tax = Liquidity + Treasury + RFV + Firepit + Dividend Sell Fee + Sell Fee = 20%

New and Updated Features::
1.	Autorebase Functionality
    •	Updated the contract to trigger rebasing automatically after 30min have passed since the last rebase
    •	Every time the token is transferred between two wallets the contract checks if the autorebase function should be triggered
    •	If more than 30 minutes pass without any transfers being made the next time a transfer is made the autorebase function can account for all the missed epochs and       rebases the appropriate amount 
2.	Dividend Reward System
    •	Implemented a dividend system that pays holders in BUSD
    •	The dividends are funded by the 3% and 5% dividend buy and sell fees respectively
    •	Since this incentivizes holders to hodl we can reduce the sell fee without having a significant impact on the sell behavior  
3.	Blackhole
    •	Implemented the blackhole system which will be used to control the expansion of the token supply 
    •	Since the impact of the blackhole reduces over time the contract has been designed in such a way that the blackhole fee will increase over time
    •	This will help mitigate unsustainable levels of inflation in the future  
4.	Removed External Mint Function 
    •	This removes the ability for anyone to mint any new tokens in the future
    •	All new tokens in the ecosystem will come from the rebase functionality 
    •	Thus guaranteeing not impact to future token price due to new tokens being minted unexpectedly

