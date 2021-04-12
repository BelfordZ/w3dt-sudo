# [Zondax/filecoin-signing-tools](https://github.com/Zondax/filecoin-signing-tools)

## Maturity

Used as the Filecoin Signing Library across several filecoin ecosystem libraries, such as:
- `filecoin.js`
- `ceramicnetwork/cli`
  - A CLI that allows you to interact with the Ceramic protocol.
- `@nodefactory/filsnap`
  - Metamask snap (plugin) to enable Metamask users interaction with filecoin dapps.
- `@glif/local-managed-provider`

This library has been actively maintained over the last months. The [documentation site](https://zondax.ch/updating-documentation) is on maintenance, which makes it difficult to understand what methods are supported unless we check the code/tests. They provide several working examples which helps. Per the available issues, it seems that there are some problems with bundlers that should be addressed as well as compatibility with some browsers.

## What it includes

1. Rust Native Library
  - Secp256k1
  - BLS
  - Filecoin transactions (CBOR <> JSON serialization)
  - Multisig (in progress)
2. WASM Library (Browser and Node.js)
  - Secp256k1
  - BLS
  - Filecoin transactions (CBOR <> JSON serialization)
  - Multisig (in progress)
3. JSON RPC Server
  - Exposes most of the functions available in the signing library

## Cryptographic primitives

1. `generateMnemonic`
2. `keyDerive`
3. `keyDeriveFromSeed`
4. `keyRecover`
5. `transactionSerialize`
6. `transactionSerializeRaw`
7. `transactionParse`
8. `transactionSign`
9. `transactionSignLotus`
10. `transactionSignRaw`
11. `verifySignature`
12. `addressAsBytes`
13.  `bytesToAddress`

All available via Rust, Wasm (browser and Node.js) and JSON RPC Server.

## Overall

This library looks up to date and offers all the needed cryptographic primitives to interact with a Lotus node.