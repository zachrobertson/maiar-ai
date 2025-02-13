[@maiar-ai/core](../index.md) / Runtime

# Class: Runtime

Defined in: [packages/core/src/runtime/index.ts:52](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L52)

Runtime class that manages the execution of plugins and agent state

## Constructors

### new Runtime()

> **new Runtime**(`config`): [`Runtime`](Runtime.md)

Defined in: [packages/core/src/runtime/index.ts:215](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L215)

#### Parameters

##### config

[`RuntimeConfig`](../interfaces/RuntimeConfig.md)

#### Returns

[`Runtime`](Runtime.md)

## Properties

### operations

> `readonly` **operations**: `object`

Defined in: [packages/core/src/runtime/index.ts:65](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L65)

Operations that can be used by plugins

#### getObject()

> **getObject**: \<`T`\>(`schema`, `prompt`, `config`?) => `Promise`\<`TypeOf`\<`T`\>\>

##### Type Parameters

• **T** *extends* `ZodType`\<`unknown`, `unknown`\>

##### Parameters

###### schema

`T`

###### prompt

`string`

###### config?

`OperationConfig`

##### Returns

`Promise`\<`TypeOf`\<`T`\>\>

#### getText()

> **getText**: (`prompt`, `config`?) => `Promise`\<`string`\>

##### Parameters

###### prompt

`string`

###### config?

`GetObjectConfig`

##### Returns

`Promise`\<`string`\>

#### getBoolean()

> **getBoolean**: (`prompt`, `config`?) => `Promise`\<`boolean`\>

##### Parameters

###### prompt

`string`

###### config?

`GetObjectConfig`

##### Returns

`Promise`\<`boolean`\>

## Accessors

### llm

#### Get Signature

> **get** **llm**(): [`LLMService`](LLMService.md)

Defined in: [packages/core/src/runtime/index.ts:80](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L80)

Access to the LLM service for plugins

##### Returns

[`LLMService`](LLMService.md)

***

### memory

#### Get Signature

> **get** **memory**(): [`MemoryService`](MemoryService.md)

Defined in: [packages/core/src/runtime/index.ts:87](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L87)

Access to the memory service for plugins

##### Returns

[`MemoryService`](MemoryService.md)

***

### context

#### Get Signature

> **get** **context**(): `undefined` \| [`AgentContext`](../interfaces/AgentContext.md)

Defined in: [packages/core/src/runtime/index.ts:94](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L94)

Access to the current context

##### Returns

`undefined` \| [`AgentContext`](../interfaces/AgentContext.md)

## Methods

### registerPlugin()

> **registerPlugin**(`plugin`): `Promise`\<`void`\>

Defined in: [packages/core/src/runtime/index.ts:225](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L225)

Register a plugin with the runtime

#### Parameters

##### plugin

[`Plugin`](../interfaces/Plugin.md)

#### Returns

`Promise`\<`void`\>

***

### start()

> **start**(): `Promise`\<`void`\>

Defined in: [packages/core/src/runtime/index.ts:254](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L254)

Start the runtime

#### Returns

`Promise`\<`void`\>

***

### stop()

> **stop**(): `Promise`\<`void`\>

Defined in: [packages/core/src/runtime/index.ts:280](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L280)

Stop the runtime

#### Returns

`Promise`\<`void`\>

***

### getPlugins()

> **getPlugins**(): [`Plugin`](../interfaces/Plugin.md)[]

Defined in: [packages/core/src/runtime/index.ts:291](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L291)

Get all registered plugins

#### Returns

[`Plugin`](../interfaces/Plugin.md)[]

***

### pushContext()

> **pushContext**(`context`): `void`

Defined in: [packages/core/src/runtime/index.ts:298](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L298)

Push a new context to the event queue

#### Parameters

##### context

[`AgentContext`](../interfaces/AgentContext.md)

#### Returns

`void`

***

### pushToContextChain()

> **pushToContextChain**(`item`): `void`

Defined in: [packages/core/src/runtime/index.ts:305](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L305)

Context management methods for plugins

#### Parameters

##### item

[`BaseContextItem`](../interfaces/BaseContextItem.md)

#### Returns

`void`

***

### createEvent()

> **createEvent**(`initialContext`, `platformContext`?): `Promise`\<`void`\>

Defined in: [packages/core/src/runtime/index.ts:326](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L326)

#### Parameters

##### initialContext

[`UserInputContext`](../interfaces/UserInputContext.md)

##### platformContext?

###### platform

`string`

###### responseHandler

(`response`) => `void`

###### metadata

`Record`\<`string`, `unknown`\>

#### Returns

`Promise`\<`void`\>

***

### subscribeToContext()

> **subscribeToContext**(`callback`): () => `void`

Defined in: [packages/core/src/runtime/index.ts:587](https://github.com/UraniumCorporation/maiar-ai/blob/main/packages/core/src/runtime/index.ts#L587)

Subscribe to context changes
Returns an unsubscribe function

#### Parameters

##### callback

(`context`) => `void`

#### Returns

`Function`

##### Returns

`void`
