# hashgraph-bootstrap

Summary:

A barebones javascript project to get you connected to the Testnet using the Hedera API as fast and painlessly as possible.

Requirements:

Node and NPM

Installation Instructions:

Clone this repository into a folder using git

Then run the following commands, just using the defaults in npm init is fine:
```
npm init
npm install --save @hashgraph/sdk
npm install --save dotenv
```
Next you need to create a .env file in your folder with the following lines:

Sample .env

_____________________________
```
# Hedera Operator
# Used to pay for transaction fees for integration tests

# Hedera Operator Account ID
OPERATOR_ID="0.0.xxxxxx"

# Hedera Operator Private Key
OPERATOR_KEY="302e02010xxxxxxxxxxxxxxxxxxxxxxxxbxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```
______________________

For OPERATOR_ID and OPERATOR_KEY, you need to get a Hedera Portal Testnet Account
https://portal.hedera.com/?network=testnet

Fill in the details and place them in the root folder of the project.

______________________

Now just run

node ./main.js

And you should see it connect to the Testnet and get an account balance!
