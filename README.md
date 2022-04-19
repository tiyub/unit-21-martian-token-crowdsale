# Unit 21: Martian Token Crowdsale

![alt=""](./Instructions/Images/application-image.png)

## Background

After waiting for years and passing several tests, the Martian Aerospace Agency selected a prominent fintech professional to lead a project developing a monetary system for the new Mars colony. Their decision was that the new system be based on blockchain technology and to define a new cryptocurrency named **KaseiCoin**. Kasei after the Japanese word for Mars.

KaseiCoin will be a fungible token that’s ERC-20 compliant. A crowdsale where people moving to Mars can convert their Earth fiat money to KaseiCoin.

## Evaluation Evidence

#### Develop KaseiCoin.sol smart contract that will mint the KAI

KaseiCoin inherits the following contracts from the OpenZeppelin library:

    * `ERC20`  
    * `ERC20Detailed`
    * `ERC20Mintable`

Test compile failed due to `uint initial_supply` being an unsed variable.  
![alt=""](evaluation-evidence/001-compile-error.png)  

To compile with no errors unused var `uint initial_supply` was commented. Screenshot of successful compilation of the Kasei constructor definition contract below.  
![alt=""](evaluation-evidence/002-compile-test-fix.png)  

Test compile of `KaseiCoinCrowdsale.sol` with errors. `KaseiCoin.sol` constructor contract was not in uploaded remix.ethereum.org.  
![alt=""](evaluation-evidence/003-compile-test-no-constuctor-contract.png)  

Complie error screenshot due to the above upload omission.  
![alt=""](evaluation-evidence/004-compile-test-note-pragma55.png)  

Screenshot of successfulest compile of `KaseiCoinCrowdsale.sol` contract below. 
![alt=""](evaluation-evidence/005-compile-test.png)  





