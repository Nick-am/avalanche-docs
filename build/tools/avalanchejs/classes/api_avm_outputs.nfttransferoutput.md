[avalanche](../README.md) › [API-AVM-Outputs](../modules/api_avm_outputs.md) › [NFTTransferOutput](api_avm_outputs.nfttransferoutput.md)

# Class: NFTTransferOutput

An [Output](common_output.output.md) class which specifies an Output that carries an NFT and uses secp256k1 signature scheme.

## Hierarchy

  ↳ [NFTOutput](api_avm_outputs.nftoutput.md)

  ↳ **NFTTransferOutput**

## Index

### Constructors

* [constructor](api_avm_outputs.nfttransferoutput.md#constructor)

### Properties

* [_typeID](api_avm_outputs.nfttransferoutput.md#protected-_typeid)
* [_typeName](api_avm_outputs.nfttransferoutput.md#protected-_typename)
* [addresses](api_avm_outputs.nfttransferoutput.md#protected-addresses)
* [groupID](api_avm_outputs.nfttransferoutput.md#protected-groupid)
* [locktime](api_avm_outputs.nfttransferoutput.md#protected-locktime)
* [numaddrs](api_avm_outputs.nfttransferoutput.md#protected-numaddrs)
* [payload](api_avm_outputs.nfttransferoutput.md#protected-payload)
* [sizePayload](api_avm_outputs.nfttransferoutput.md#protected-sizepayload)
* [threshold](api_avm_outputs.nfttransferoutput.md#protected-threshold)

### Methods

* [clone](api_avm_outputs.nfttransferoutput.md#clone)
* [create](api_avm_outputs.nfttransferoutput.md#create)
* [deserialize](api_avm_outputs.nfttransferoutput.md#deserialize)
* [fromBuffer](api_avm_outputs.nfttransferoutput.md#frombuffer)
* [getAddress](api_avm_outputs.nfttransferoutput.md#getaddress)
* [getAddressIdx](api_avm_outputs.nfttransferoutput.md#getaddressidx)
* [getAddresses](api_avm_outputs.nfttransferoutput.md#getaddresses)
* [getGroupID](api_avm_outputs.nfttransferoutput.md#getgroupid)
* [getLocktime](api_avm_outputs.nfttransferoutput.md#getlocktime)
* [getOutputID](api_avm_outputs.nfttransferoutput.md#getoutputid)
* [getPayload](api_avm_outputs.nfttransferoutput.md#getpayload)
* [getPayloadBuffer](api_avm_outputs.nfttransferoutput.md#getpayloadbuffer)
* [getSpenders](api_avm_outputs.nfttransferoutput.md#getspenders)
* [getThreshold](api_avm_outputs.nfttransferoutput.md#getthreshold)
* [getTypeID](api_avm_outputs.nfttransferoutput.md#gettypeid)
* [getTypeName](api_avm_outputs.nfttransferoutput.md#gettypename)
* [makeTransferable](api_avm_outputs.nfttransferoutput.md#maketransferable)
* [meetsThreshold](api_avm_outputs.nfttransferoutput.md#meetsthreshold)
* [select](api_avm_outputs.nfttransferoutput.md#select)
* [serialize](api_avm_outputs.nfttransferoutput.md#serialize)
* [toBuffer](api_avm_outputs.nfttransferoutput.md#tobuffer)
* [toString](api_avm_outputs.nfttransferoutput.md#tostring)
* [comparator](api_avm_outputs.nfttransferoutput.md#static-comparator)

## Constructors

###  constructor

\+ **new NFTTransferOutput**(`groupID`: number, `payload`: Buffer, `addresses`: Array‹Buffer›, `locktime`: BN, `threshold`: number): *[NFTTransferOutput](api_avm_outputs.nfttransferoutput.md)*

*Overrides [OutputOwners](common_output.outputowners.md).[constructor](common_output.outputowners.md#constructor)*

*Defined in [src/apis/avm/outputs.ts:302](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L302)*

An [Output](common_output.output.md) class which contains an NFT on an assetID.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`groupID` | number | undefined | A number representing the amount in the output |
`payload` | Buffer | undefined | A [Buffer](https://github.com/feross/buffer) of max length 1024 |
`addresses` | Array‹Buffer› | undefined | An array of [Buffer](https://github.com/feross/buffer)s representing addresses |
`locktime` | BN | undefined | A [BN](https://github.com/indutny/bn.js/) representing the locktime |
`threshold` | number | undefined | A number representing the the threshold number of signers required to sign the transaction   |

**Returns:** *[NFTTransferOutput](api_avm_outputs.nfttransferoutput.md)*

## Properties

### `Protected` _typeID

• **_typeID**: *number* = AVMConstants.NFTXFEROUTPUTID

*Overrides [NFTOutput](api_avm_outputs.nftoutput.md).[_typeID](api_avm_outputs.nftoutput.md#protected-_typeid)*

*Defined in [src/apis/avm/outputs.ts:231](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L231)*

___

### `Protected` _typeName

• **_typeName**: *string* = "NFTTransferOutput"

*Overrides [NFTOutput](api_avm_outputs.nftoutput.md).[_typeName](api_avm_outputs.nftoutput.md#protected-_typename)*

*Defined in [src/apis/avm/outputs.ts:230](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L230)*

___

### `Protected` addresses

• **addresses**: *Array‹[Address](common_output.address.md)›* = []

*Inherited from [OutputOwners](common_output.outputowners.md).[addresses](common_output.outputowners.md#protected-addresses)*

*Defined in [src/common/output.ts:120](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L120)*

___

### `Protected` groupID

• **groupID**: *Buffer* = Buffer.alloc(4)

*Inherited from [BaseNFTOutput](common_output.basenftoutput.md).[groupID](common_output.basenftoutput.md#protected-groupid)*

*Defined in [src/common/output.ts:510](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L510)*

___

### `Protected` locktime

• **locktime**: *Buffer* = Buffer.alloc(8)

*Inherited from [OutputOwners](common_output.outputowners.md).[locktime](common_output.outputowners.md#protected-locktime)*

*Defined in [src/common/output.ts:117](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L117)*

___

### `Protected` numaddrs

• **numaddrs**: *Buffer* = Buffer.alloc(4)

*Inherited from [OutputOwners](common_output.outputowners.md).[numaddrs](common_output.outputowners.md#protected-numaddrs)*

*Defined in [src/common/output.ts:119](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L119)*

___

### `Protected` payload

• **payload**: *Buffer*

*Defined in [src/apis/avm/outputs.ts:248](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L248)*

___

### `Protected` sizePayload

• **sizePayload**: *Buffer* = Buffer.alloc(4)

*Defined in [src/apis/avm/outputs.ts:247](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L247)*

___

### `Protected` threshold

• **threshold**: *Buffer* = Buffer.alloc(4)

*Inherited from [OutputOwners](common_output.outputowners.md).[threshold](common_output.outputowners.md#protected-threshold)*

*Defined in [src/common/output.ts:118](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L118)*

## Methods

###  clone

▸ **clone**(): *this*

*Overrides [Output](common_output.output.md).[clone](common_output.output.md#abstract-clone)*

*Defined in [src/apis/avm/outputs.ts:298](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L298)*

**Returns:** *this*

___

###  create

▸ **create**(...`args`: any[]): *this*

*Overrides [Output](common_output.output.md).[create](common_output.output.md#abstract-create)*

*Defined in [src/apis/avm/outputs.ts:294](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L294)*

**Parameters:**

Name | Type |
------ | ------ |
`...args` | any[] |

**Returns:** *this*

___

###  deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization.md#serializedencoding)): *void*

*Overrides [BaseNFTOutput](common_output.basenftoutput.md).[deserialize](common_output.basenftoutput.md#deserialize)*

*Defined in [src/apis/avm/outputs.ts:240](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L240)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`fields` | object | - |
`encoding` | [SerializedEncoding](../modules/utils_serialization.md#serializedencoding) | "hex" |

**Returns:** *void*

___

###  fromBuffer

▸ **fromBuffer**(`utxobuff`: Buffer, `offset`: number): *number*

*Overrides [OutputOwners](common_output.outputowners.md).[fromBuffer](common_output.outputowners.md#frombuffer)*

*Defined in [src/apis/avm/outputs.ts:272](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L272)*

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [NFTTransferOutput](api_avm_outputs.nfttransferoutput.md) and returns the size of the output.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`utxobuff` | Buffer | - |
`offset` | number | 0 |

**Returns:** *number*

___

###  getAddress

▸ **getAddress**(`idx`: number): *Buffer*

*Inherited from [OutputOwners](common_output.outputowners.md).[getAddress](common_output.outputowners.md#getaddress)*

*Defined in [src/common/output.ts:167](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L167)*

Returns the address from the index provided.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`idx` | number | The index of the address.  |

**Returns:** *Buffer*

Returns the string representing the address.

___

###  getAddressIdx

▸ **getAddressIdx**(`address`: Buffer): *number*

*Inherited from [OutputOwners](common_output.outputowners.md).[getAddressIdx](common_output.outputowners.md#getaddressidx)*

*Defined in [src/common/output.ts:150](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L150)*

Returns the index of the address.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Buffer | A [Buffer](https://github.com/feross/buffer) of the address to look up to return its index.  |

**Returns:** *number*

The index of the address.

___

###  getAddresses

▸ **getAddresses**(): *Array‹Buffer›*

*Inherited from [OutputOwners](common_output.outputowners.md).[getAddresses](common_output.outputowners.md#getaddresses)*

*Defined in [src/common/output.ts:135](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L135)*

Returns an array of [Buffer](https://github.com/feross/buffer)s for the addresses.

**Returns:** *Array‹Buffer›*

___

###  getGroupID

▸ **getGroupID**(): *number*

*Inherited from [BaseNFTOutput](common_output.basenftoutput.md).[getGroupID](common_output.basenftoutput.md#getgroupid)*

*Defined in [src/common/output.ts:515](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L515)*

Returns the groupID as a number.

**Returns:** *number*

___

###  getLocktime

▸ **getLocktime**(): *BN*

*Inherited from [OutputOwners](common_output.outputowners.md).[getLocktime](common_output.outputowners.md#getlocktime)*

*Defined in [src/common/output.ts:130](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L130)*

Returns the a [BN](https://github.com/indutny/bn.js/) repersenting the UNIX Timestamp when the lock is made available.

**Returns:** *BN*

___

###  getOutputID

▸ **getOutputID**(): *number*

*Overrides [Output](common_output.output.md).[getOutputID](common_output.output.md#abstract-getoutputid)*

*Defined in [src/apis/avm/outputs.ts:253](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L253)*

Returns the outputID for this output

**Returns:** *number*

___

###  getPayload

▸ **getPayload**(): *Buffer*

*Defined in [src/apis/avm/outputs.ts:260](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L260)*

Returns the payload as a [Buffer](https://github.com/feross/buffer) with content only.

**Returns:** *Buffer*

___

###  getPayloadBuffer

▸ **getPayloadBuffer**(): *Buffer*

*Defined in [src/apis/avm/outputs.ts:266](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L266)*

Returns the payload as a [Buffer](https://github.com/feross/buffer) with length of payload prepended.

**Returns:** *Buffer*

___

###  getSpenders

▸ **getSpenders**(`addresses`: Array‹Buffer›, `asOf`: BN): *Array‹Buffer›*

*Inherited from [OutputOwners](common_output.outputowners.md).[getSpenders](common_output.outputowners.md#getspenders)*

*Defined in [src/common/output.ts:196](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L196)*

Given an array of addresses and an optional timestamp, select an array of address [Buffer](https://github.com/feross/buffer)s of qualified spenders for the output.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`addresses` | Array‹Buffer› | - |
`asOf` | BN | undefined |

**Returns:** *Array‹Buffer›*

___

###  getThreshold

▸ **getThreshold**(): *number*

*Inherited from [OutputOwners](common_output.outputowners.md).[getThreshold](common_output.outputowners.md#getthreshold)*

*Defined in [src/common/output.ts:125](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L125)*

Returns the threshold of signers required to spend this output.

**Returns:** *number*

___

###  getTypeID

▸ **getTypeID**(): *number*

*Inherited from [Serializable](utils_serialization.serializable.md).[getTypeID](utils_serialization.serializable.md#gettypeid)*

*Defined in [src/utils/serialization.ts:52](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/utils/serialization.ts#L52)*

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** *number*

___

###  getTypeName

▸ **getTypeName**(): *string*

*Inherited from [Serializable](utils_serialization.serializable.md).[getTypeName](utils_serialization.serializable.md#gettypename)*

*Defined in [src/utils/serialization.ts:45](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/utils/serialization.ts#L45)*

Used in serialization. TypeName is a string name for the type of object being output.

**Returns:** *string*

___

###  makeTransferable

▸ **makeTransferable**(`assetID`: Buffer): *[TransferableOutput](api_avm_outputs.transferableoutput.md)*

*Inherited from [NFTOutput](api_avm_outputs.nftoutput.md).[makeTransferable](api_avm_outputs.nftoutput.md#maketransferable)*

*Overrides [Output](common_output.output.md).[makeTransferable](common_output.output.md#abstract-maketransferable)*

*Defined in [src/apis/avm/outputs.ts:88](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L88)*

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`assetID` | Buffer | An assetID which is wrapped around the Buffer of the Output  |

**Returns:** *[TransferableOutput](api_avm_outputs.transferableoutput.md)*

___

###  meetsThreshold

▸ **meetsThreshold**(`addresses`: Array‹Buffer›, `asOf`: BN): *boolean*

*Inherited from [OutputOwners](common_output.outputowners.md).[meetsThreshold](common_output.outputowners.md#meetsthreshold)*

*Defined in [src/common/output.ts:177](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L177)*

Given an array of address [Buffer](https://github.com/feross/buffer)s and an optional timestamp, returns true if the addresses meet the threshold required to spend the output.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`addresses` | Array‹Buffer› | - |
`asOf` | BN | undefined |

**Returns:** *boolean*

___

###  select

▸ **select**(`id`: number, ...`args`: any[]): *[Output](common_output.output.md)*

*Inherited from [NFTOutput](api_avm_outputs.nftoutput.md).[select](api_avm_outputs.nftoutput.md#select)*

*Overrides [Output](common_output.output.md).[select](common_output.output.md#abstract-select)*

*Defined in [src/apis/avm/outputs.ts:92](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L92)*

**Parameters:**

Name | Type |
------ | ------ |
`id` | number |
`...args` | any[] |

**Returns:** *[Output](common_output.output.md)*

___

###  serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization.md#serializedencoding)): *object*

*Overrides [BaseNFTOutput](common_output.basenftoutput.md).[serialize](common_output.basenftoutput.md#serialize)*

*Defined in [src/apis/avm/outputs.ts:233](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L233)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`encoding` | [SerializedEncoding](../modules/utils_serialization.md#serializedencoding) | "hex" |

**Returns:** *object*

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Overrides [OutputOwners](common_output.outputowners.md).[toBuffer](common_output.outputowners.md#tobuffer)*

*Defined in [src/apis/avm/outputs.ts:286](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/apis/avm/outputs.ts#L286)*

Returns the buffer representing the [NFTTransferOutput](api_avm_outputs.nfttransferoutput.md) instance.

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Inherited from [OutputOwners](common_output.outputowners.md).[toString](common_output.outputowners.md#tostring)*

*Defined in [src/common/output.ts:261](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L261)*

Returns a base-58 string representing the [Output](common_output.output.md).

**Returns:** *string*

___

### `Static` comparator

▸ **comparator**(): *function*

*Inherited from [OutputOwners](common_output.outputowners.md).[comparator](common_output.outputowners.md#static-comparator)*

*Defined in [src/common/output.ts:265](https://github.com/ava-labs/avalanchejs/blob/2850ce5/src/common/output.ts#L265)*

**Returns:** *function*

▸ (`a`: [Output](common_output.output.md), `b`: [Output](common_output.output.md)): *0 | 1 | -1*

**Parameters:**

Name | Type |
------ | ------ |
`a` | [Output](common_output.output.md) |
`b` | [Output](common_output.output.md) |
