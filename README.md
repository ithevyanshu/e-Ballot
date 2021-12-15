# e-Ballot

In a bid to address digital interfaces, this E-voting application serves as a solution for
anyone who is unable to reach the polling booth or prefers to cast his or her vote
remotely. The greater purpose of the application is that it makes use of blockchain
technology - hence this system is invulnerable to fraud and cyberattacks as the blocks
of data cannot be tampered with. Blockchain makes it more secure, crucial in an
electoral arena, where there could be a tendency to manipulate voting. The
application primarily aims at increasing trust, efficiency, and security within the
voting system of any kind.

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
near create-account evoting.YOUR-NAME.testnet --masterAccount YOUR-NAME.testnet.

Step 2: Set contract name in code
Modify the line in src/config.js that sets the account name of the contract. Set it to the
account id you used above.
const CONTRACT_NAME = process.env.CONTRACT_NAME || 'evoting.YOUR-NAME.testnet'

Step 3: Deploy!
npm deploy
1. This does two things: builds & deploys smart contract to NEAR TestNet
2. Builds & deploys frontend code to GitHub using gh-pages. This will only work if the
project already has a repository set up on GitHub.

![image](https://user-images.githubusercontent.com/69449944/146135510-b42a2381-3dc7-48b5-a756-fcf4a22cacbc.png)

![image](https://user-images.githubusercontent.com/69449944/146135531-3bb6a8f0-6b7e-481c-83cb-f2e89b17629a.png)

![image](https://user-images.githubusercontent.com/69449944/146135431-f029c2f0-dd5f-453d-84ee-427c6e39234d.png)

![image](https://user-images.githubusercontent.com/69449944/146135470-17a53a92-b2c5-445a-8de5-acfc739411fd.png)

![image](https://user-images.githubusercontent.com/69449944/146135634-07fab76d-c63e-4eb5-9d33-99ebf34be87e.png)

![image](https://user-images.githubusercontent.com/69449944/146135644-d61b9f62-dd81-4f8b-b97f-fd32d6c4750c.png)


