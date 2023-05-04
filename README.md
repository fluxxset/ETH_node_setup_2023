# ETH_node_setup_2023 Cloud / Local

## installing Packages

`sudo apt update`

`sudo add-apt-repository -y ppa:ethereum/ethereum`

`sudo apt-get update`

`sudo apt-get install ethereum`


## Connecting to Consensus Clients


`mkdir prysm && cd prysm`

`curl https://raw.githubusercontent.com/prysmaticlabs/prysm/master/prysm.sh --output prysm.sh && chmod +x prysm.sh`

`./prysm.sh beacon-chain generate-auth-secret`

## starting geth server/node

`geth --http --http.api eth,net,engine,admin --authrpc.jwtsecret /root/prysm/jwt.hex`

## starting Consensus Client

`./prysm.sh beacon-chain --execution-endpoint=http://localhost:8551 --jwt-secret=/root/prysm/jwt.hex --suggested-fee-recipient=0x01234567722E6b0000012BFEBf6177F1D2e9758D9`


add your address in above cmmand insted of "0x01234567722E6b0000012BFEBf6177F1D2e9758D9"


------------------------------------------------------------------------------------------------------------


if you dont have Vultr account use below link to create new onw and get 100$ free credit.
[https://m.do.co/c/8f7b157b0fa2](https://www.vultr.com/?ref=9418944)

<a href="https://www.vultr.com/?ref=9418944"><img src="https://www.vultr.com/media/logo_mono_ondark.png?_gl=1*c52ya5*_ga*NzE2NTMyMTc2LjE2ODA2MTQzMzc.*_ga_K6536FHN4D*MTY4MTA1OTkyMC4yOC4xLjE2ODEwNjA4MjYuNTkuMC4w" alt="Vultr Referral Badge" /></a>
