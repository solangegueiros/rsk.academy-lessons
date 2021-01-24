## Creating the smart contract Name

Click on symbol `+` - create a new file.

![create a new file](../../images/remix/image-10.png)

File name: `Name.sol`

![filename Name.sol](../../images/remix/image-11.png)

Copy this smart contract:

```solidity
pragma solidity 0.5.4;

contract Name {
    string private name;
    address public owner;

    constructor() public {
        owner = msg.sender;
        name = "Your name";
    }

    function getName() public view returns (string memory) {
        return name;
    }
}
```

Paste it into Remix, here:

![Paste name.sol at Remix](../../images/remix/image-12.png)

### Name.sol

This smart contract has:

* A variable `name` to store your name
* A variable `owner` which is the account who create this smart contract
* The `constructor()` which is executed only when the smart contract was created
* A function `getName()` to return the name stored at variable info
