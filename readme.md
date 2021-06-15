# Iron.finance Vault Compounder

Calls the compound function of private vaults generated by [iron.finance](https://iron.finance)

## Installation

- Install [nodejs](https://nodejs.org/)
- Download the files
- Open a command prompt/terminal window in the directory and run `npm i`


## Usage

### Generating and filling out the config file
- Open a command prompt/terminal window in the same directory and run `node index.js` to generate the config file
- Fill out the "farms" section with the smart contract addresses of your farms, this should follow javascript syntax and addresses should be in double-quotes.
- Change the gas limit, gas price, and RPC URL if you wish
- The bot uses cron style scheduling to schedule compounding, cron style syntax generators can be found online. The default is set to run at mightnight every day. 
>- [Cron syntax helper](https://cron.help/) 
>- [Common Interval Examples](https://cron.help/examples)
### Generating a bot wallet and configuring farms
- Run `node index.js` again to generate a wallet for the bot to use, copy the wallet address of the newly generated wallet
- Navigate to the smart contract of your vault on [polygonscan.com](https://polygonscan.com) and click e contract tab
- Click "Write Contract" and connect the wallet of the **OWNER** of the farm
- Scroll down to "setHarvestor" and paste the previously copied address of the bot
- Click "Write" and confirm the transaction


#### You are done! Run the bot with `node index.js`