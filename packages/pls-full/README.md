# `pls-full`

The `pls-full` module is the comprehensive package within the PLS project, encapsulating the functionalities of the entire suite. It integrates the core features from `pls-core`, `pls-bitcoin`, `pls-liquid`, and `pls-nostr`, providing a unified interface for blockchain contract management across different networks.

## Key Features

- Integrates with `pls-core` for contract schema creation and utility functions.
- Incorporates `pls-bitcoin` for Bitcoin network interactions.
- Includes `pls-liquid` for functionalities specific to the Liquid network.
- Utilizes `pls-nostr` for Nostr protocol communication.

## Dependencies

- `pls-core`: Core utilities and contract schema definitions.
- `pls-bitcoin`: Bitcoin network interaction and transaction management.
- `pls-liquid`: Liquid network-specific functionalities.
- `pls-nostr`: Nostr protocol communication tools.
- `zod`: Data validation schema creation.

## How to Use

To leverage the full capabilities of the PLS project, import `pls-full` into your TypeScript or JavaScript project. This module allows you to interact with various blockchain networks and manage contracts seamlessly.

For instance, you can create a unified contract schema that applies to both Bitcoin and Liquid networks, and handle Nostr communications, all through the interfaces provided by `pls-full`.