NFT Marketplace
This project is a decentralized NFT Marketplace built with Solidity, Hardhat, and Next.js, allowing users to mint, buy, and sell NFTs.

Table of Contents
Overview
Tech Stack
Getting Started
Smart Contract Deployment
Frontend Setup
License
Overview
This decentralized application (dApp) enables users to list, buy, and mint NFTs on Ethereum or any compatible blockchain. The marketplace allows users to trade NFTs directly, with secure on-chain transactions and interactions.

Tech Stack
Frontend: Next.js, React.js
Backend: Hardhat (Solidity)
Blockchain: Ethereum (EVM-based networks)
Storage: IPFS (for storing metadata)
Additional Libraries: Web3.js, Ethers.js, OpenZeppelin, Hardhat Toolbox
Getting Started
Prerequisites
Ensure you have the following installed:

Node.js (v16.x or later)
npm or yarn
Hardhat
Installation
Clone the repository:

bash
Copy code
git clonehttps://github.com/Raviul-Islam/HackIndia-Spark-6-Tech-Warriors.git
cd nft-marketplace
Install the project dependencies:

bash
Copy code
npm install

Environment Setup
Create a .env file in the root directory with the following content:

bash
Copy code
NEXT_PUBLIC_INFURA_ID=<NFT Martketplace>
NEXT_PUBLIC_NETWORK=<infura>
NEXT_PUBLIC_PRIVATE_KEY=<d7e3f589240740b09e12da6b0e4effd3>
These environment variables are required for connecting to the Ethereum network.

Smart Contract Deployment
Compile the smart contracts:

npx hardhat compile

Deploy the contracts to a local blockchain:



npx hardhat node
npx hardhat ignition deploy ./ignition/modules/Lock.js --network localhost
After deployment, copy the contract address from the terminal and update it in the frontend code inside the file constants.js:

javascript
Copy code
export const NFTMarketplaceAddress = "YOUR_DEPLOYED_CONTRACT_ADDRESS";
Frontend Setup
Run the development server:



npm run dev


Troubleshooting
If you encounter issues like missing artifacts or module errors, try cleaning the cache and reinstalling dependencies:



npm install
npx hardhat clean
npx hardhat compile
