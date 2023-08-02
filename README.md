# Smart Contract Project of Train Scheduling
This Train schedule contract program tells about the scheduling of trains and if any accident happens using require(), assert(), and revert() statements techniques.

## Description

This program is a simple contract for cricket matches, providing the details of match scheduling and injuries during the match, getting the results accordingly. It contains four functions that are: First Match, that is responsible for the finalCall value using assert statement means if there will be a match then the finalCall value will get incremented by 3 and if not then it will remain the same and print one message too along with the calling of Matchtoday(public variable) using require technique, Second CancelledMatch, is responsible for reverting the match schedule using Matchtoday variable, Third getCal, for returning finalCall value, Fourth InjuryHappened for returning the result of the Medical variable if it is needed or not using revert technique.

## Getting Started
### Executing program
       
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract TrainScheduling {
    bool public TrainArrival = true;
    bool public Ambulance = false;
    uint finalCall = 0;

    function Train () public {
        require(TrainArrival,"No Train!!!");
        finalCall += 3;
    
        assert (finalCall != 0);
    }
    function TrainCancelled() public{
        TrainArrival = !TrainArrival;
    }
    function getCal() public view returns(uint) {
        return finalCall;
    }
    function Accident () public {
        if(TrainArrival){
            Ambulance = true;
        }else{
            revert("Accident doesn't happened!!!");
        }
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile evax1.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Cricketmatch" contract from the dropdown menu, and then click on the "Deploy" button. 

Once the contract is deployed, you can interact with it by clicking on various functions. Click on the "Cricketmatch" contract in the left-hand sidebar, and then click on the functions, getting the results accordingly. Finally, click on the functions again to revert back the results and print related messages.

## Authors
Vidhika Bajaj

## License
This project is licensed under the MIT License
