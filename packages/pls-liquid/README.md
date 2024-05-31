# `pls-liquid`

O módulo `pls-liquid` é uma parte do projeto PLS que fornece funcionalidades para interagir com a rede Liquid. Ele usa a biblioteca `liquidjs-lib` para criar e assinar transações, entre outras operações relacionadas ao Liquid.

## Principais Funções

- `createLiquidMultisig`: Esta função é usada para criar um endereço multisig na rede Liquid.

- `startSpendFromLiquidMultisig`: Esta função inicia uma transação a partir de um endereço multisig, adicionando entradas e saídas à transação.

- `getUnblindedUtxoValue`: Esta função é usada para obter o valor não cego de um UTXO.

- `signTaprootTransaction`: Esta função é usada para assinar uma transação Taproot.

## Dependências

- `liquidjs-lib`: Usada para interagir com a rede Liquid.

- `ecpair`: Usada para criar pares de chaves EC.

- `pls-core`: Usada para definir esquemas de contrato e fornecer funções utilitárias.

- `zod`: Usada para a criação de esquemas de validação de dados.

## Como usar

Para usar este módulo, você pode importá-lo em seu projeto TypeScript ou JavaScript e usar suas funções para interagir com a rede Liquid. Por exemplo, você pode usar a função `createLiquidMultisig` para criar um endereço multisig, e então usar a função `startSpendFromLiquidMultisig` para iniciar uma transação a partir desse endereço.