# hashgraph-bootstrap

#### Summary:

A barebones javascript project to get you connected to the Testnet using the Hedera API as fast and painlessly as possible.

#### First Steps for Complete Beginners:

For complete beginners who just want to get into the code and try messing around, here are a few steps to help get you started. These instructions are for windows users. If a mac user can help me out with a step-by-step I'd be grateful.

1. Make a Github account and Download Github Desktop : https://desktop.github.com/
2. Download Windows Terminal: https://www.microsoft.com/en-us/p/windows-terminal

Github Desktop will let you download and manage this repository. Github repositories are how people share code, and so getting your feet wet and learning how they work is going to be super useful if you want to learn how to develop apps.

Windows Terminal is the command line interface. It lets you type in commands to do things. A basic command list is here: https://www.thomas-krenn.com/en/wiki/Cmd_commands_under_Windows

Specifically for this bootstrap you will just need to learn how to change directories, the "CD" command. All you need to do is type "cd <folder path>" to go to the directory of the project. For example, "cd C:\PROJECTS\hashgraph-bootstrap"

3. Clone the repository onto your computer. Basically this makes a copy of the files on your computer. Click the big green button that says "Code" in the top right of this page and select "Open in Github Desktop". This will launch Github desktop, let you choose a folder path for your files, and then clone it.
4. You will now need to install Node, which is a package manager that helps you to download the code requirements for the project. You can find it here: https://nodejs.org/en/download/

5. Now you can use the 'cd' command to navigate to the hashgraph-bootstrap/ folder and continue with the instructions below!

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

