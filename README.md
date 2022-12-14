## Compiling the ECR20.sol file ##
## In ECR20.sol file  updated the SHB_1559 then by selecting environment as  Inject Provider-Metamask and by selecting the compiler need to ##
## Compile the code present in ERC20.sol file ##


## Deploying the code ##

To deploy the code we need to select deploy button on Remix and then it will diplay Etherscan page link. Need to go to Etherscan page link there it will give the update about the deployment. 

## Etherscan ##

It will show pending when the deployment is in progress .And then if the deployment is successful it will show successfull status.And this gereates a contract number .The contract page need to be verified and publish. 

## ABI

The ABI code need to be copy from Contract and then to be pasted on token_transfer.py, web3helpers.py and eth_transfer.py file.

## Importing the tokens in MetaMask ##

Contract address need to be used to generate the Imported token.  A million Shibi tokens would be imported with the unique name (Here it is "SHB_1559").

## Update the .env file ##
Update the following things in the .env file:
CONTRACT_ADDRESS = The new generated contact from etherscan has been updated on .env file.
OWNER_ADDRESS= This is my metamask address i copied from metamask account.
SUPER_SECRET_PRIVATE_KEY = Generated Private Key from metamask account and pasted on .env file

## Build an Image ##

docker build --tag 21215995 .

## Run an image ##

docker run --name 21215995 -p 8090:8080 21215995

## Run the curl command to transfer the token ##

curl --header "Content-Type: application/json" --request POST --data '{"address":"0x6332937B6E67cC5fD008C2EFc6C4ABc720c5D884"}' http://localhost:8090/token

A token would be transferred from your account to the account mentioned in the curl command (0x1DfFa18c1C2C1dE13177707E582B6d15DC4473D6).