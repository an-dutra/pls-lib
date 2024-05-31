# `pls-bitcoin`

The `pls-bitcoin` module is a part of the PLS project that provides functionalities for interacting with the Bitcoin network. It uses the `bitcoinjs-lib` library to create and sign transactions, among other Bitcoin-related operations.

## Key Functions

- `createBitcoinMultisig`: This function is used to create a multisig address on the Bitcoin network.

- `startTxSpendingFromMultisig`: This function initiates a transaction from a multisig address, adding inputs and outputs to the transaction.

- `combine`: This function is used to combine items in an array.

- `getTapscriptSigsOrdered`: This function is used to get ordered tapscript signatures.

## Dependencies

- `bitcoinjs-lib`: Used for interacting with the Bitcoin network.

- `ecpair`: Used to create EC key pairs.

- `pls-core`: Used to define contract schemas and provide utility functions.

- `zod`: Used for creating data validation schemas.

## How to Use

To use this module, you can import it into your TypeScript or JavaScript project and use its functions to interact with the Bitcoin network. For example, you can use the `createBitcoinMultisig` function to create a multisig address, and then use the `startTxSpendingFromMultisig` function to initiate a transaction from that address.