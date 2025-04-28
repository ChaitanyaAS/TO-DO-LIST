# TO-DO-LIST

## Overview
This is a decentralized **To-Do List** application built on the **Ethereum blockchain** using **Hardhat** and **Sepolia** for transactions. The application allows users to manage their tasks in a decentralized way, with tasks being stored on the blockchain.
The front end of the application is built using **JavaScript**, and interactions with the blockchain are handled via **Hardhat** and **ethers.js**.

## Features
- **Decentralized Task Management**: Tasks are added, updated, and removed from the Ethereum blockchain.
- **Sepolia Test Network**: The app uses the Sepolia testnet for deploying and interacting with smart contracts.
- **JavaScript Frontend**: The frontend is built using JavaScript and interacts with the blockchain via the **ethers.js** library.
  
## Technologies Used
- **Hardhat**: Development environment to compile, test, and deploy smart contracts.
- **Sepolia Test Network**: A test Ethereum network used to deploy the smart contract for transaction simulations.
- **Ethers.js**: A JavaScript library to interact with the Ethereum blockchain.
- **Solidity**: The language used to write the smart contract for the To-Do list.
- **HTML/CSS**: Frontend for user interface.
- **JavaScript**: Backend logic to interact with the smart contract.

## Prerequisites
Before you start, make sure you have the following installed:
- **Node.js**: Ensure that Node.js is installed on your system.
- **Hardhat**: Install Hardhat for smart contract development.
  
To check if you have Node.js installed, run:
```bash
node -v
```

If it's not installed, download and install it from [here](https://nodejs.org/).

## Setup Instructions

### 1. Install Dependencies
First, navigate to your project directory and install the necessary dependencies using npm:

```bash
npm install
```

### 2. Compile and Deploy the Smart Contract
Make sure your Hardhat environment is set up correctly.

- To compile the smart contract, run:
  ```bash
  npx hardhat compile
  ```

- To deploy to the Sepolia test network, make sure you have configured **Hardhat** for Sepolia. If you don't have the network configured, follow the instructions in the Hardhat documentation to set it up. Once done, deploy using:
  ```bash
  npx hardhat run scripts/deploy.js --network sepolia
  ```

### 3. Set Up the Frontend
Once the contract is deployed, configure the frontend to interact with the blockchain.

- Replace the contract's address and ABI in the `scripts.js` file with the deployed contract's address and ABI.

### 4. Run the Application
After setting everything up, you can run the application by opening the `index.html` file in a web browser.

Alternatively, you can use a local server like **Live Server** (VS Code extension) to serve the files.

## How to Interact with the App
- **Add a Task**: Users can add new tasks to the blockchain.
- **Mark Task as Completed**: Tasks can be marked as completed once finished.
- **Delete Task**: Tasks can be deleted from the blockchain.

The interactions are performed via the frontend, which communicates with the blockchain using **ethers.js**.

### Example Interactions:
1. **Add a new task**:
   - Input a task description and click "Add Task" to store it on the blockchain.

2. **Mark a task as completed**:
   - Click on a task to toggle its completion status.

3. **Delete a task**:
   - Click the "Delete" button next to a task to remove it from the blockchain.

## Configuration for Sepolia
Make sure to configure your **sepolia** network details in `hardhat.config.js`:

```javascript
module.exports = {
  solidity: "0.8.0",
  networks: {
    sepolia: {
      url: `https://sepolia.infura.io/v3/YOUR_INFURA_PROJECT_ID`,
      accounts: [`0x${YOUR_PRIVATE_KEY}`],
    },
  },
};
```

## Issues and Debugging
If you face any issues with transactions or contract interaction:
- Ensure your **Infura project ID** and **private key** are correctly set.
- Check for errors in the **console logs** for any issues with the smart contract or frontend interaction.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
