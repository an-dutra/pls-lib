# PLS Project

The PLS project is a comprehensive suite of TypeScript modules designed for creating and managing contracts and transactions on various blockchain networks, including Bitcoin and Liquid. It provides a robust set of tools for developers to build blockchain applications with support for advanced features like multisig addresses, Taproot transactions, and Nostr protocol communication.

## Key Modules

- `pls-core`: Core utilities and contract schema definitions.
- `pls-bitcoin`: Bitcoin network interaction and transaction management.
- `pls-liquid`: Liquid network-specific functionalities.
- `pls-nostr`: Nostr protocol communication tools.
- `pls-full`: A unified interface that combines all the above modules.

## Usage Examples

### Creating a Bitcoin Multisig Address

```javascript
import { createBitcoinMultisig } from 'pls-bitcoin';
const publicKeys = ['<publicKey1>', '<publicKey2>', '<publicKey3>'];
const quorum = 2; // Number of required signatures
const network = bitcoin.networks.bitcoin; // Use bitcoin.networks.testnet for testnet
const multisigAddress = createBitcoinMultisig(publicKeys, quorum, network);
console.log(multisigAddress);
```



### Initiating a Liquid Network Multisig Transaction

```javascript
import { createLiquidMultisig, startSpendFromLiquidMultisig } from 'pls-liquid';
const participants = ['<publicKey1>', '<publicKey2>'];
const arbitrators = ['<publicKeyArbitrator>'];
const arbitratorsQuorum = 1;
const network = liquid.networks.liquid; // Use liquid.networks.testnet for testnet
const { address, confidentialAddress } = createLiquidMultisig(participants, arbitrators, arbitratorsQuorum, network);
// Use the confidentialAddress to receive funds and then spend them with startSpendFromLiquidMultisig
```

### Working with Nostr Events

```javascript
import { nostrCommunicationSchema } from 'pls-nostr';
const nostrEvent = nostrCommunicationSchema.parse({
type: 'nostr',
identifiers: {
clients: ['<publicKey1>', '<publicKey2>'],
arbitrators: ['<publicKeyArbitrator>'],
},
});
console.log(nostrEvent);
```

### Building and Developing

To build all apps and packages, run the following command:

```shell
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```shell
pnpm dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```shell
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Tasks](https://turbo.build/repo/docs/core-concepts/monorepos/running-tasks)
- [Caching](https://turbo.build/repo/docs/core-concepts/caching)
- [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching)
- [Filtering](https://turbo.build/repo/docs/core-concepts/monorepos/filtering)
- [Configuration Options](https://turbo.build/repo/docs/reference/configuration)
- [CLI Usage](https://turbo.build/repo/docs/reference/command-line-reference)
