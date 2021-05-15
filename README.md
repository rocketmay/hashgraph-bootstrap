# hashgraph-bootstrap

#### Summary:

A barebones javascript project to get you connected to the Testnet using the Hedera API as fast and painlessly as possible.

#### Requirements:

Node and NPM

#### Installation Instructions:

Clone this repository into a folder using git

Then run the following commands, just using the defaults in npm init is fine:
```
npm init
npm install --save @hashgraph/sdk
npm install --save dotenv
```
Next you need to create a .env file in your folder with the following lines:

__ file: .env _____________________________
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
```
Attempting to get token info from the Hedera API...
The token balance(s) for this account: {"0.0.574366":"999000"}
```

# ISSUES

May 12, 2021: There seems to have been an update to @hashgraph/proto between version 1.0.25 and 1.1.0 that causes the following error:
```(node:36840) UnhandledPromiseRejectionWarning: TypeError: Cannot read property 'encode' of undefined```

Until this gets fixed, you can use the previous version by doing the following steps:
```
Delete the folder 'node_modules' and delete package-lock.json
Rename package-lock-fix.json to 'package-lock.json'
Run the command:  npm ci
```

now 'node ./main.js' should work.

