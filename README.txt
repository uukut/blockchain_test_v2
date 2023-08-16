This is an react app for cloning the Flowx.finance Swap and Liquidity.

There are 2 ways to start-up the project in your local:
1. Make sure you have installed visual studio code
 ->Make sure there is a lib called npm and node.js in the vs code (You can check by typing npm -v or node -v to see if they are existed)
 ->If no, here is the way to install: https://www.npmjs.cn/getting-started/installing-node/ or https://www.runoob.com/nodejs/nodejs-install-setup.html 
 ->Try to execute npm -v or node -v to see if they are successfully installed in the terminal of vs code
 ->Create a new react project by typing: npm create-react-app <name of the project> to the terminal
 ->Drag everything inside this zip into your app to make it work
 ->Also, please ensure there is framer-motion and web3 installed in the vs code using npm install framer-motion and npm install web3

2. Unzip this file and open the folder using vs code (but it probably cannot run)

Everything is settled expect the AddLiquidityETH. The code that need to be adjusted is from AddPosition.js inside the Liquidity folder.
The function name is called Apply. The function called from the smart contract is AddLiquidityETH.
The usage is same as the write contract on the pancakeswap website's contract.
You can either test locally or on BSCscan testnet (if you cannot open the react app properly ) since they should be the same.
Recently, the problem is execution reverted: PancakeLibrary: INSUFFICIENT_AMOUNT.
While you are testing locally, you can check the problem by clicking the Apply button and press F12 in the website and check the column named console.
There maybe some other problem poped out which can be neglected since there is just some difference between the react and HTML 5 which is not vital.

Btw, I have experienced lots of problem on the Apply button such as the OUT OF GAS problem which is you trying to limited the gasPrice or something else inside the contract_used which is not neccessary since the system will automatically calculated for you.
The second one is the execution reverted: PancakeLibrary: INSUFFICIENT_A/B_AMOUNT which means you are out of A/B tokens.
The third one is encoding error which means your number of tokens wanted to transfer or added does not fulfill it's type requirement.
The last one is expired problem which can be solved by adjusting the deadline to a larger value but this won't occur since I have been adjusted already.