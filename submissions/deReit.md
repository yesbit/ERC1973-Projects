# Project Name: Decentralized REIT

# Authors and Github username: Abiel Villarosa (@abielvillarosa)

# Description of the Project 

A decentralized REIT application enables investors to own shares of real estate properties similar to REIT. These shares will be represented by ERC 1400 Security tokens. 

One of the requirements of REIT is to have 150 shareholders (Canada requirements on REIT) on the second year of the operations. To be able to entice investors to participate on getting shares of REIT to be able to start the REIT project, 'n' number of ERC1400 Security token reward will be given every 6 months starting from the issuance of shares until the third year of the operation. This is to ensure that investor retains their investment until the REIT is fully approved after the second year. Investors who get in early will also be rewarded more since there will be fewer participants at the start and can earn more if he retains his investment until the third year of the operation.

# Problem specification related to ERC 1973

Every 6 months a reward will be distributed to all investor who has shares. However, as the number of investors grow, this can cause some problems on the application
1) The number of investors going in and out differs throughout the period making the calculation of the rewards a challenge
2) Once there are substantial number of investors who have joined, the application will have a challenge on distributing the rewards over time.

# Solution in relation to ERC 1973 

Application of ERC 1973 allows ERC 1400 reward distribution in a scalable manner to all the participating investors throughout the reward period. Every six months the rewards are minted as ERC 1400 security tokens and the amount of rewards will be calculated per investors at the time the reward is minted depending on how many investors participated. Once the investor withdraws his share, the total rewards will be calculated depending on when he started his investment together with the investment amount.

A sample of rewards distribution is as per below based on 1,000 tokens minted for each round:

6th Month (100 participants) - Rewards per participant: 10 (100,000/100)

12th Month (500 participants) - Rewards per participant: 2 (100,000/500)

18th Month (2000 participants) - Rewards per participant: .5 (100,000/2000)

24th Month (5000 participants) - Rewards per participant: .2 (100,000/5000)

30th Month (10000 participants) - Rewards per participant: .1 (100,000/10000)

36th Month (20000 participants) - Rewards per participant: .05 (100,000/20000)


# Related Links

* Github repo: https://github.com/abielvillarosa/dereit
* Wesbite link: https://abielvillarosa.github.io/dereit/
* Canadian REIT Documentation - http://www.sfu.ca/~poitras/417_REITS_14-2.pdf

# Additional Notes 
* Testing Instructions:
  
  TestNet Deployed: Ropsten
  
  Token Contract Address: 0x9F83fe7891429e1D674E8C0bfbC6A7Fc9EdA2B0B
  
  Main Contract Address: 0x563f1B58BD6f91B30F0f16A9767B3989DA8BF3Cb
  
  Steps:
  1) Register as Investor - This button registers the account as minter
  2) Claim Reward - This button will trigger the trigger() function to calculate round mask
  3) Withdraw Investment - This button triggers the withdraw() function to transafer the reward from the contract owner to the investor
