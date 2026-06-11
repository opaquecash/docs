# Interface: UabDeployment

Defined in: packages/uab/dist/config.d.ts:14

A UAB deployment on one EVM chain.

## Properties

### chainId

> **chainId**: `number`

Defined in: packages/uab/dist/config.d.ts:15

***

### fromBlock

> **fromBlock**: `bigint`

Defined in: packages/uab/dist/config.d.ts:24

Block the UAB contracts were deployed at — never scan before this.

***

### sourceWhChain

> **sourceWhChain**: `number`

Defined in: packages/uab/dist/config.d.ts:22

Wormhole chain id of the trusted cross-chain source (the other chain).

***

### uabReceiver

> **uabReceiver**: `` `0x${string}` ``

Defined in: packages/uab/dist/config.d.ts:20

***

### uabSender

> **uabSender**: `` `0x${string}` ``

Defined in: packages/uab/dist/config.d.ts:19

***

### whChain

> **whChain**: `number`

Defined in: packages/uab/dist/config.d.ts:17

Wormhole chain id of THIS chain.

***

### wormholeCore

> **wormholeCore**: `` `0x${string}` ``

Defined in: packages/uab/dist/config.d.ts:18
