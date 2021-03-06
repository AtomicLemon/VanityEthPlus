# Vanity ETH+

NodeJS based tool to generate vanity ethereum addresses

# Features!

  - Generate multiple addresses
  - Supports Multi-core processors
  - vanity contract address
  - log to file
  - checksum based vanity address

### Installation
```sh
$ npm install -g vanity-eth
$ vanityeth -i deadbeef
```
### Examples

Generate ethereum address:
```sh
$ vanityeth
```

generate 10 ethereum addresses:
```sh
$ vanityeth -n 10
```

generate 10 ethereum addresses with deadbeef as starting characters:
```sh
$ vanityeth -n 10 -i deadbeef
```
generate 10 ethereum addresses with DEADBEEF as the checksum address (case sensitive):
```sh
$ vanityeth -n 10 -i DEADBEEF -c
```
generate ethereum address with vanity contract address:
```sh
$ vanityeth -i deadbeef --contract
```
log to file
```sh
$ vanityeth -n 10 -l
```
help me
```sh
$ vanityeth -h
```
### Docker usage

Get the image
```sh
# Build image locally after cloning repository
$ docker build -t vanityeth .

# or download image
docker pull myetherwallet/vanityeth
```

Usage
```
$ docker run -it vanityeth

# Pass additional arguments
$ docker run -it myetherwallet/vanityeth -i deadbeef
```

Sample output:
```
atomiclemon@lemonnode:~/VanityEth$ node index.js -i B00B5
✔ {"account":{"address":"0xb00b5728f3931ad9a8fa5ae4806da437c6d0d4b0","privKey":"8436f1bc115b1d8a41532c9be2fd17776bcb7c0b86dd89b36b302564bcefdd27"}}
```

### Running Locally
To run from source:
```sh
git clone git@github.com:MyEtherWallet/VanityEth.git
cd VanityEth
npm install
node index.js
```

License
----

MIT

