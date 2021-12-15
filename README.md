# e-Ballot
**
Steps to run this project locally:**

**Prerequisites:**
1. Make sure you've installed Node.js ≥ 12
2. Install dependencies: npm install
3. Run the local development server: npm run dev (see package.json for a full list of scripts
you can run with yarn)

**Exploring The Code:**
1. The backend code lives in the /contract folder.
2. The frontend code lives in the /src folder. /src/index.html loads in /src/index.js,
where you can learn how the frontend connects to the NEAR blockchain.

**Deploy:**
Every smart contract in NEAR has its own associated account. When you run npm run dev,
your smart contract gets deployed to the live NEAR TestNet with a throwaway account.
When you're ready to make it permanent, here's how.
Step 1: Create an account for the contract
Each account on NEAR can have at most one contract deployed to it. If you've already
created an account such as your-name.testnet, you can deploy your contract to
evoting.your-name.testnet. Assuming you've already created an account on NEAR Wallet,
here's how to create evoting.your-name.testnet:
1. Authorize NEAR CLI, following the commands it gives you: near login
2. Create a subaccount (replace YOUR-NAME below with your actual account name):
near create-account evoting.YOUR-NAME.testnet --masterAccount YOUR-NAME.testnet
Step 2: Set contract name in code
Modify the line in src/config.js that sets the account name of the contract. Set it to the
account id you used above.
const CONTRACT_NAME = process.env.CONTRACT_NAME || 'evoting.YOUR-NAME.testnet'
Step 3: Deploy!
npm deploy
1. This does two things: builds & deploys smart contract to NEAR TestNet
2. Builds & deploys frontend code to GitHub using gh-pages. This will only work if the
project already has a repository set up on GitHub.
