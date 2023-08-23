# IMigratable
[Git Source](https://github.com/smartcontractkit/destiny-next/blob/93e1115f8d7fb0029b73a936d125afb837306065/src/interfaces/IMigratable.sol)


## Functions
### setMigrationTarget

Sets the address this contract will be upgraded to


```solidity
function setMigrationTarget(address newMigrationTarget) external;
```
**Parameters**

|Name|Type|Description|
|----|----|-----------|
|`newMigrationTarget`|`address`|The address of the migration target|


### getMigrationTarget

Returns the current migration target of the contract


```solidity
function getMigrationTarget() external view returns (address);
```
**Returns**

|Name|Type|Description|
|----|----|-----------|
|`<none>`|`address`|address The current migration target|


### migrate

Migrates the contract


```solidity
function migrate(bytes calldata data) external;
```
**Parameters**

|Name|Type|Description|
|----|----|-----------|
|`data`|`bytes`|Optional calldata to call on new contract|


## Events
### MigrationTargetSet
This event is emitted when the migration target is set


```solidity
event MigrationTargetSet(address indexed oldMigrationTarget, address indexed newMigrationTarget);
```

## Errors
### InvalidMigrationTarget
This error is thrown when the owner tries to set the migration target to the
zero address or an invalid address as well as when the migration target is not set and owner
tries to migrate the contract.


```solidity
error InvalidMigrationTarget();
```
