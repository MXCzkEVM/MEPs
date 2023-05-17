# MEP-20: **Tokens on MXC zkEVM Chain**

**Created**: 2023-04-20

## **Abstract**

The MEP20 standard is a basic standard that follows the ERC20 format. MEP20 provides an interface for tokens on the MXC zkEVM chain

## **Motivation**

The motivation behind the MEP20 token standard is to promote the brand identity and recognition of the MXC blockchain and its ecosystem. The MEP20 token standard provides a clear connection between tokens and the MXC zkEVM chain, allowing anyone examining the contract code to identify that the token is part of the MXC ecosystem. This is important for promoting the growth and adoption of the MXC blockchain, as well as strengthening the overall brand identity and recognition of the platform.

## **Specification**

### Token

### Methods

**NOTES**:

- The following specifications use syntax from Solidity `0.4.17` (or above)
- Callers MUST handle `false` from `returns (bool success)`. Callers MUST NOT assume that `false` is never returned!

#### name

Returns the name of the token - e.g. `"MyToken"`.

OPTIONAL - This method can be used to improve usability,
but interfaces and other contracts MUST NOT expect these values to be present.

```js
function name() public view returns (string)
```

#### symbol

Returns the symbol of the token. E.g. "HIX".

OPTIONAL - This method can be used to improve usability,
but interfaces and other contracts MUST NOT expect these values to be present.

```js
function symbol() public view returns (string)
```

#### decimals

Returns the number of decimals the token uses - e.g. `8`, means to divide the token amount by `100000000` to get its user representation.

OPTIONAL - This method can be used to improve usability,
but interfaces and other contracts MUST NOT expect these values to be present.

```js
function decimals() public view returns (uint8)
```

#### totalSupply

Returns the total token supply.

```js
function totalSupply() public view returns (uint256)
```

#### balanceOf

Returns the account balance of another account with address `_owner`.

```js
function balanceOf(address _owner) public view returns (uint256 balance)
```

#### transfer

Transfers `_value` amount of tokens to address `_to`, and MUST fire the `Transfer` event.
The function SHOULD `throw` if the message caller's account balance does not have enough tokens to spend.

_Note_ Transfers of 0 values MUST be treated as normal transfers and fire the `Transfer` event.

```js
function transfer(address _to, uint256 _value) public returns (bool success)
```

#### transferFrom

Transfers `_value` amount of tokens from address `_from` to address `_to`, and MUST fire the `Transfer` event.

The `transferFrom` method is used for a withdraw workflow, allowing contracts to transfer tokens on your behalf.
This can be used for example to allow a contract to transfer tokens on your behalf and/or to charge fees in sub-currencies.
The function SHOULD `throw` unless the `_from` account has deliberately authorized the sender of the message via some mechanism.

_Note_ Transfers of 0 values MUST be treated as normal transfers and fire the `Transfer` event.

```js
function transferFrom(address _from, address _to, uint256 _value) public returns (bool success)
```

#### approve

Allows `_spender` to withdraw from your account multiple times, up to the `_value` amount. If this function is called again it overwrites the current allowance with `_value`.

**NOTE**: To prevent attack vectors like the one [described here](https://docs.google.com/document/d/1YLPtQxZu1UAvO9cZ1O2RPXBbT0mooh4DYKjA_jp-RLM/) and discussed [here](https://github.com/ethereum/EIPs/issues/20#issuecomment-263524729),
clients SHOULD make sure to create user interfaces in such a way that they set the allowance first to `0` before setting it to another value for the same spender.
THOUGH The contract itself shouldn't enforce it, to allow backwards compatibility with contracts deployed before

```js
function approve(address _spender, uint256 _value) public returns (bool success)
```

#### allowance

Returns the amount which `_spender` is still allowed to withdraw from `_owner`.

```js
function allowance(address _owner, address _spender) public view returns (uint256 remaining)
```

### Events

#### Transfer

MUST trigger when tokens are transferred, including zero value transfers.

A token contract which creates new tokens SHOULD trigger a Transfer event with the `_from` address set to `0x0` when tokens are created.

```js
event Transfer(address indexed _from, address indexed _to, uint256 _value)
```

#### Approval

MUST trigger on any successful call to `approve(address _spender, uint256 _value)`.

```js
event Approval(address indexed _owner, address indexed _spender, uint256 _value)
```

## Implementation

#### Example implementations

```solidity
pragma solidity ^0.5.0;

/**
 * @title MEP20 interface
 */
interface IMEP20 {
  function totalSupply() external view returns (uint256);

  function balanceOf(address who) external view returns (uint256);

  function allowance(address owner, address spender)
    external view returns (uint256);

  function transfer(address to, uint256 value) external returns (bool);

  function approve(address spender, uint256 value)
    external returns (bool);

  function transferFrom(address from, address to, uint256 value)
    external returns (bool);

  event Transfer(
    address indexed from,
    address indexed to,
    uint256 value
  );

  event Approval(
    address indexed owner,
    address indexed spender,
    uint256 value
  );
}
```

## References

- EIP-20: [https://eips.ethereum.org/EIPS/eip-20](https://eips.ethereum.org/EIPS/eip-20)
