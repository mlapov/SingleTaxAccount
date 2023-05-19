# Project Description

## Background of the problem

In country "X", in order to optimize taxation for businessmen, a Single Tax Payment was introduced in place of several tax payments. That is, a businessman now has to make one payment to one tax account instead of several payments to several tax accounts. And already the tax service should distribute the payment received from businessman to different tax accounts of different budgetary institutions.
However, things did not go as smoothly as we would like. The tax service, either for technical reasons or for human reasons, could not cope with the innovation, as a result of which some businessmen had problems and tax debts -  that is, the businessman paid, and the tax service did not have time to distribute the money to different tax accounts.

## Problem

Unsatisfactory work of the tax service in spreading the Single tax payment from a businessman to different tax accounts in different government agencies.

## Solution

Creation of a Smart contract that will replace the tax service in terms of posting payments from businessmen to different tax accounts in different public institutions.

## Description of the project work

The launch of the project imitates the onset of a new tax period, when the tax service uploads tax data for businessmen into this smart contract - the Single Tax Smart-Contract.
A businessman enters his personal account - the interface of the Single Tax Smart Contract under his account connected to Metamask, and sees a list of taxes in the "Tax Notice" field with the amount of taxes to be paid. A businessman, having fiat money on his Bank account, converts them into special StateToken tokens (STT), through the "Convert $ to tokens" field. STT tokens appear on the businessman's account - "StateToken`s Account".
Further, a message appears in the Personal Account stating that the businessman partially or completely has enough STT tokens to pay the tax.
The "Pay" button pays the tax, which will be displayed in the "You paid taxes" field.
If the tax is paid in full, the "No tax arrears" overlay will appear.
Also, in the case of full payment of tax on the businessman's account, NFT is issued as proof of tax payment.

![Image alt](https://github.com/mlapov/Alchemy-University-Practics/blob/585a81f7d23d93cfbdef94b0e1c6b70dfdfa6d3b/2_EthDev/week_8/SingleTaxAccount/screen/current%20tax.png)

All NFTs issued to the entrepreneur's account can be viewed in the "Payment history".
At the same time, the tax number of the payment (#), the date and time of payment of the tax, the amount of tax, and the list of taxes paid are recorded in the NFT.

![Image alt](https://github.com/mlapov/Alchemy-University-Practics/blob/24ea866f0458f2308e8621b06b4e5898b8317033/2_EthDev/week_8/SingleTaxAccount/screen/history.png)

In the Personal Account, in the "Addresses" tab, all the addresses that are used in the project are listed. These are the address of the businessman himself, the address of the owner of the smart contract, the address of the smart contract itself, the address of the STT token, the address of the NFT, as well as the addresses of tax accounts of various budgetary institutions.

![Image alt](https://github.com/mlapov/Alchemy-University-Practics/blob/24ea866f0458f2308e8621b06b4e5898b8317033/2_EthDev/week_8/SingleTaxAccount/screen/addresses.png)

In the Personal Account there is a "Test" tab for manually assigning taxes to entrepreneurs.

![Image alt](https://github.com/mlapov/Alchemy-University-Practics/blob/24ea866f0458f2308e8621b06b4e5898b8317033/2_EthDev/week_8/SingleTaxAccount/screen/test.png)

The project is deployed on the Sepolia testnet.

## Launch of the project

1. Download Repository or ```git clone https://github.com/mlapov/SingleTaxAccount.git```
2. ```cd path/to/SingleTaxAccount && npm install && cd app && npm install```
3. The project simulates the situation for the accounts of 3 specific entrepreneurs, as it would be in real life, since the list of entrepreneurs in the country is limited and controlled by the tax service.
If you want to substitute your own invoices, to do this, in the files ```app/src/init.js``` and ```app/src/assigntax.js``` you must insert one or all of the invoices:
* ```const bisnessmen1 = "..."```
* ```const bisnessmen2 = "..."```
* ```const bisnessmen3 = "..."```

4. Create ```.env``` files in ```/SingleTaxAccount``` and ```/SingleTaxAccount/src```
Do not forget to specify ```STATE_PRIVATE_KEY``` - the private key of the address, in case you deploy your contracts in the project yourself (this is like an account in the tax service or the state), it must be different from your businessman account (the account that will pay tax)
and ```ALCHEMY_SEPOLIA_URL``` in ```.env``` files
5. ```cd app && npm start```

**IMPORTANT!!! To deploy your own contracts with new addresses use in ```/SingleTaxAccount npx hardhat run scripts/deploy.js --network sepolia```**

## Contracts Architecture

contracts/
* ```SingleTaxContract.sol```: Contract containing the main functionality of the project
* ```StateToken.sol```: Contract StateToken (STT)
* ```NFTContract.sol```: NFT contract for proof of tax payment

## Tech Stack

* [Solidity](https://docs.soliditylang.org/en/v0.8.18/)
* [Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [Hardhat](https://hardhat.org/docs)
* [OpenZeppelin](https://docs.openzeppelin.com)
* [Alchemy](https://www.alchemy.com/)
* [React](https://react.dev/)
* [Chakra UI](https://chakra-ui.com/)


