# Unit 21: Martian Token Crowdsale

![alt=""](./Instructions/Images/application-image.png)

## Background

After waiting for years and passing several tests, the Martian Aerospace Agency selected a prominent fintech professional to lead a project developing a monetary system for the new Mars colony. Their decision was that the new system be based on blockchain technology and to define a new cryptocurrency named **KaseiCoin**. Kasei after the Japanese word for Mars.

KaseiCoin will be a fungible token that’s ERC-20 compliant. A crowdsale where people moving to Mars can convert their Earth fiat money to KaseiCoin.

## Evaluation Evidence

### Develop KaseiCoin.sol smart contract that will mint the KAI  

KaseiCoin inherits the following contracts from the OpenZeppelin library:  

    * `ERC20`  
    * `ERC20Detailed`  
    * `ERC20Mintable`  

Test compile failed due to `uint initial_supply` being an unused variable.  
Fig. 1  ![alt="Fig. 1"](evaluation-evidence/001-compile-error.png)  

To compile with no errors unused var `uint initial_supply` was commented. Screenshot of successful compilation of the Kasei constructor definition contract below.  
Fig. 2  ![alt="Fig. 2"](evaluation-evidence/002-compile-test-fix.png)  

Test compile of `KaseiCoinCrowdsale.sol` with errors. `KaseiCoin.sol` constructor contract was not in uploaded remix.ethereum.org.  
Fig. 3  ![alt="Fig. 3"](evaluation-evidence/003-compile-test-no-constuctor-contract.png)  

Complie error screenshot due to the above upload omission.  
Fig. 4  ![alt="Fig. 4"](evaluation-evidence/004-compile-test-note-pragma55.png)  

Screenshot of successful `KaseiCoinCrowdsale.sol` test compile contract below. 
Fig. 5  ![alt="Fig. 5"](evaluation-evidence/005-compile-test.png)  

`KaseiCoinCrowdsale.sol` test compile with errors. Errors due to commented line in Fig. 2. Expected argument count of 3. Only 2 due to test compile. Ln 38 was uncommented. Ln 38 was uncommented to attempt compile. 2nd compile error encountered due to Ln. 47. The `KaseiCoinCrowdsale` object was called, should have called the instance named `kasei_crowdsale`.   
Fig. 6  ![alt="Fig. 6"](evaluation-evidence/006-compile-test-args.png)  

Reference was changed to `kasei_crowdsale` - successful compile Fig. 7.  
Fig. 7  ![alt="Fig. 7"](evaluation-evidence/007-compile-test-fix.png)  

### Screen Recording of Local Blockchain Interactions  

Please download and view the interaction low-resoution .mp4 and as higher resolution .mov videos in the [Evaluation Evidence folder.](https://github.com/tiyub/unit-21-martian-token-crowdsale/tree/main/evaluation-evidence)


Ganache, Metamask, Remix connected  
Fig. 8  ![alt="Fig. 8"](evaluation-evidence/interaction-001-connect-ganache-metamask-remix.png)  

Deploy and input:  

    * Cryptocurrency name: kasei  
    * Symbol: kai   
    * Initial Supply  
Fig. 9  ![alt="Fig. 9"](evaluation-evidence/interaction-002-deploy-name-sym-iSupply.png)  

Additional interaction:  

    * addminter - Fig. 10  
    * isminter - Fig. 11  
    * mint coin  - Fig. 12  
        
Fig. 10  ![alt="Fig. 10"](evaluation-evidence/interaction-003-add-minter.png)  
Fig. 11  ![alt="Fig. 11"](evaluation-evidence/interaction-004-isminter.png)  
Fig. 12  ![alt="Fig. 12"](evaluation-evidence/interaction-005-minting.png)  