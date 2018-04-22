# dapps-token
dapps-token is sample token on ethereum network.

### Create dapps-token
* Init
  ```sh
  $ truffle init
  $ npm init -f
  $ npm install zeppelin-solidity
  ```
* Add files
  * contracts/DappsToken.sol 
  * migrations/2_deploy_dapps_token.js
  * test/DappsToken.js

### Run in truffle development network
```sh
$ truffle develop
$ truffle(develop)> test
$ truffle(develop)> compile
$ truffle(develop)> migrate
```

### dapps-token command
```sh
$ dappsToken=DappsToken.at(<address>)
$ dappsToken.name()
$ dappsToken.symbol()
$ dappsToken.balanceOf(web3.eth.accounts[0])
$ dappsToken.balanceOf(web3.eth.accounts[1])
$ dappsToken.transfer(web3.eth.accounts[1], 200)
```

### Run in external network
Migrate to development network in truffle.js, for example, [go-ethreum](https://ethereum.github.io/go-ethereum/).
```sh
$ truffle migrate --network development
$ truffle console --network development
```

### Run in Ropsten network
Install [MetaMask](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn) and sign up for [Infura](https://infura.io). Then, edit the following variables:
```js:truffle.js
// truffle.js
var mnemonic = $MNEMONIC;
var accessToken = $INFURA_ACCESS_TOKEN;
```
Install module
```sh
# Can't install in python3. Use python2 by pyenv local 2.*.*.
$ npm install truffle-hdwallet-provider
```
```sh
$ truffle migrate --network ropsten
$ truffle console --network ropsten
```
