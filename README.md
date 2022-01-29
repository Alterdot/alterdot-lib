# Alterdot Library

[![NPM Version](https://img.shields.io/npm/v/alterdot-lib)](https://www.npmjs.com/package/alterdot-lib)
[![Build Status](https://github.com/Alterdot/alterdot-lib/actions/workflows/test_and_release.yml/badge.svg)](https://github.com/Alterdot/alterdot-lib/actions/workflows/test_and_release.yml)
[![Release Date](https://img.shields.io/github/release-date/Alterdot/alterdot-lib)](https://github.com/Alterdot/alterdot-lib/releases/latest)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen)](https://github.com/RichardLitt/standard-readme)

A pure and powerful JavaScript Alterdot library.

Alterdot is a powerful new peer-to-peer platform for the next generation of financial technology. The decentralized nature of the Alterdot network allows for highly resilient Alterdot infrastructure, and the developer community needs reliable, open-source tools to implement Alterdot apps and services.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## Install

### NodeJS

```
npm install alterdot-lib
```

### Browser

#### CDN Standalone

```html
<script src="https://unpkg.com/alterdot-lib"></script>
<script>
  const { PrivateKey } = alterdot;
  const privateKey = new PrivateKey();
  const address = privateKey.toAddress().toString();
  ...
</script>
```

#### Building the Browser Bundle

To build a alterdot-lib full bundle for the browser:

```sh
npm run build
```

This will generate a file named `alterdot-lib.min.js` in the `dist/` folder.

## Usage

### Browser

```
<script src='./dist/alterdot-lib.min.js' type="text/javascript"></script>
<script>
  const PrivateKey = alterdot.PrivateKey;
  const privateKey = new PrivateKey();
  const address = privateKey.toAddress().toString();
</script>
```

### Modules

Some functionality is implemented as a module that can be installed separately:

- [Payment Protocol Support](https://github.com/Alterdot/alterdot-payment-protocol)
- [Peer to Peer Networking](https://github.com/Alterdot/alterdot-p2p)
- [Alterdot Core JSON-RPC](https://github.com/Alterdot/dashd-rpc)
- [Mnemonics](https://github.com/Alterdot/alterdot-mnemonic)
- [Elliptical Curve Integrated Encryption Scheme](https://github.com/Alterdot/bitcore-ecies-dash)
- [Signed Messages](https://github.com/Alterdot/bitcore-message-dash)

### Development & Tests

```sh
git clone https://github.com/Alterdot/alterdot-lib
cd alterdot-lib
npm install
```

Run all the tests:

```sh
npm test
```

You can also run just the Node.js tests with `npm run test:node`, just the browser tests with `npm run test:browser` or run a test coverage report with `npm run coverage`.

## Documentation

### Concepts

- [Addresses](docs/core-concepts/address.md)
- [Block](docs/core-concepts/block.md)
- [Crypto](docs/core-concepts/crypto.md)
- [Encoding](docs/core-concepts/encoding.md)
- [Hierarchically-derived Private and Public Keys](docs/core-concepts/hierarchical.md)
- [Mnemonic](docs/core-concepts/mnemonic.md)
- [Networks](docs/core-concepts/networks.md)
- [PrivateKey](docs/core-concepts/privatekey.md)
- [PublicKey](docs/core-concepts/publickey.md)
- [Script](docs/core-concepts/script.md)
- [Transaction](docs/core-concepts/transaction.md)
- [Using Different Units](docs/core-concepts/unit.md)
- [Unspent Output](docs/core-concepts/unspentoutput.md)
- [URI](docs/core-concepts/uri.md)
- [Governance Object / Proposal](docs/core-concepts/govobject/govobject.md)

### How To Use

- [Addresses](docs/usage/address.md)
- [Block](docs/usage/block.md)
- [BlockHeader](docs/usage/blockheader.md)
- [Hierarchically-derived Private Key](docs/usage/hdprivatekey.md)
- [Hierarchically-derived Public Key](docs/usage/hdpublickey.md)
- [Message](docs/usage/message.md)
- [Mnemonic](docs/usage/mnemonic.md)
- [Opcode](docs/usage/opcode.md)
- [PrivateKey](docs/usage/privatekey.md)
- [PublicKey](docs/usage/publickey.md)
- [Script](docs/usage/script.md)
- [Transaction](docs/usage/transaction.md)
- [Transaction Input](docs/usage/transaction_input.md)
- [Transaction Output](docs/usage/transaction_output.md)
- [URI](docs/usage/uri.md)

### Use Case Examples

Some examples can be found [here](docs/examples.md), below is a list of direct links for some of them.

- [Generate a random address](docs/examples.md#generate-a-random-address)
- [Generate an address from a SHA256 hash](docs/examples.md#generate-an-address-from-a-sha256-hash)
- [Import an address via WIF](docs/examples.md#import-an-address-via-wif)
- [Create a Transaction](docs/examples.md#create-a-transaction)
- [Sign a Alterdot message](docs/examples.md#sign-a-bitcoin-message)
- [Verify a Alterdot message](docs/examples.md#verify-a-bitcoin-message)
- [Create an OP RETURN transaction](docs/examples.md#create-an-op-return-transaction)
- [Create a 2-of-3 multisig P2SH address](docs/examples.md#create-a-2-of-3-multisig-p2sh-address)
- [Spend from a 2-of-2 multisig P2SH address](docs/examples.md#spend-from-a-2-of-2-multisig-p2sh-address)

## Contributing

Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/Alterdot/alterdot-lib/blob/master/CONTRIBUTING.md) file.

## License

Code released under [the MIT license](LICENSE).

Copyright 2013-2017 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.  
Copyright 2016-2017 The Dash Foundation, Inc.  
Copyright 2017-2021 Dash Core Group, Inc.
Copyright 2022 Alterdot Network
