# Analysis results for test-filename.sol

## Message call to external contract
- SWC ID: 107
- Type: Informational
- Contract: Unknown
- Function name: `thisisfine()`
- PC address: 661
- Estimated Gas Usage: 643 - 1254

### Description

This contract executes a message call to to another contract. Make sure that the called contract is trusted and does not execute user-supplied code.

## Unchecked CALL return value
- SWC ID: 104
- Type: Informational
- Contract: Unknown
- Function name: `thisisfine()`
- PC address: 666
- Estimated Gas Usage: 1352 - 35963

### Description

The return value of an external call is not checked. Note that execution continue even if the called contract throws.

## Message call to external contract
- SWC ID: 107
- Type: Warning
- Contract: Unknown
- Function name: `callstoredaddress()`
- PC address: 779
- Estimated Gas Usage: 687 - 1298

### Description

This contract executes a message call to an address found at storage slot 1. This storage slot can be written to by calling the function `setstoredaddress(address)`. Generally, it is not recommended to call user-supplied addresses using Solidity's call() construct. Note that attackers might leverage reentrancy attacks to exploit race conditions or manipulate this contract's state.

## Transaction order dependence
- SWC ID: 114
- Type: Warning
- Contract: Unknown
- Function name: `callstoredaddress()`
- PC address: 779
- Estimated Gas Usage: 687 - 1298

### Description

Possible transaction order dependence vulnerability: The value or direction of the call statement is determined from a tainted storage location.

## Unchecked CALL return value
- SWC ID: 104
- Type: Informational
- Contract: Unknown
- Function name: `callstoredaddress()`
- PC address: 784
- Estimated Gas Usage: 1396 - 36007

### Description

The return value of an external call is not checked. Note that execution continue even if the called contract throws.

## Message call to external contract
- SWC ID: 107
- Type: Informational
- Contract: Unknown
- Function name: `reentrancy()`
- PC address: 858
- Estimated Gas Usage: 709 - 1320

### Description

This contract executes a message call to to another contract. Make sure that the called contract is trusted and does not execute user-supplied code.

## State change after external call
- SWC ID: 107
- Type: Warning
- Contract: Unknown
- Function name: `reentrancy()`
- PC address: 869
- Estimated Gas Usage: 709 - 1320

### Description

The contract account state is changed after an external call. Consider that the called contract could re-enter the function before this state change takes place. This can lead to business logic vulnerabilities.

## Unchecked CALL return value
- SWC ID: 104
- Type: Informational
- Contract: Unknown
- Function name: `reentrancy()`
- PC address: 871
- Estimated Gas Usage: 6432 - 61043

### Description

The return value of an external call is not checked. Note that execution continue even if the called contract throws.

## Message call to external contract
- SWC ID: 107
- Type: Warning
- Contract: Unknown
- Function name: `calluseraddress(address)`
- PC address: 912
- Estimated Gas Usage: 335 - 616

### Description

This contract executes a message call to an address provided as a function argument. Generally, it is not recommended to call user-supplied addresses using Solidity's call() construct. Note that attackers might leverage reentrancy attacks to exploit race conditions or manipulate this contract's state.

## Unchecked CALL return value
- SWC ID: 104
- Type: Informational
- Contract: Unknown
- Function name: `calluseraddress(address)`
- PC address: 918
- Estimated Gas Usage: 1046 - 35327

### Description

The return value of an external call is not checked. Note that execution continue even if the called contract throws.
