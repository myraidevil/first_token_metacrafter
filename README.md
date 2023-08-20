# first_token_metacrafter
 first token
This Solidity program is a mint and burn token program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a simple smart contract that is succesfully deployed in remix and understanding minting and burining of tokens.

Description -
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that "mint" and "burn" tokens and store them in balances and total supply. This program serves as a simple smart contreact in Solidity programming, and can be used as a stepping stone for more complex projects in the future.

Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

pragma solidity ^0.8.18;
contract MyToken {
    string public tokenName = "FIRSTTOKEN";
    string public tokenAbbrv = "FT";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint (address _address, uint _value) public{
        totalSupply += _value;
        balances[_address] += _value;
    }
    
     function burn (address _address, uint _value) public{
         if (balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
    }
     }
}


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken/firstToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the "mint" function to mint the tokens
-by calling the "burn" function u can burn the tokens
by calling the total supply & balances we can check the balances and the available total supply of tokens 
