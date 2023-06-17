# Create a Token
This program demonstarte the creation of token using the Solidity programming language.

## Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This contract is used for the creation of token using various functions and variables. This contract has  public varaiables that stores the details of the token namely tokenName,tokenAbbrv and totalSupply. This contract has two function namely mint function  which is used fror creation of token  and burn function which works opposite to mint as it is use to destroy the token. This program gives best demonstration about the working of token and can be used for solving  more complex problem related to tokens.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName ="PRATI";
    string public tokenAbbrv ="PAT";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address=> uint) public balances;

    // mint function
    function mint(address _address, uint _value)public{
        totalSupply += _value;
        balances[_address] += _value;
    }


    // burn function
     function burn(address _address, uint _value)public{
        if(balances[_address]>=_value){
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

## Author

Atish Shah

## License

This project is licensed under the MIT License.


