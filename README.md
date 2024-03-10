# Project: Create a Token

Its a way of creating a token for aspiring crypto enthusiast who wants to make their own coin or token.

## Description

This software is a basic program coded in Solidity, a programming language designed for creating smart contracts on the Ethereum blockchain. This application acts as a clear and uncomplicated initiation into Solidity programming, providing a foundation for more intricate projects down the line.

## Getting Started

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

### Executing program

* How to run the program
* Step-by-step bullets
```
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;

then add the following code for Mapping

   // mapping variable here
    mapping(address => uint) public balances;

After mapping the code now you include the Mint and Burn function

   // mint function
    function mint (address _address, uint _value)public {
    totalSupply += _value;
    balances[_address] += _value;

}
    // burn function
    function burn (address _address, uint _value)public {
        if(balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
        }  
    }
}

```

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
