# Smart Contract Project of Train Scheduling
This Train schedule contract program tells about the scheduling of trains and if any accident happens using require(), assert(), and revert() statements techniques.

## Description

This program is a straightforward contract for railway schedules, it provides information on train scheduling and, in the event of an accident, the results are determined accordingly. It contains four functions that are: First Train, which calls TrainArrival(public variable) using the need approach and uses an assert statement to determine the finalCall value. If a train arrives, the finalCall value will be increased by 3, else it will remain unchanged and print another message; Second TrainCancelled, uses the TrainArrival variable to reverse the train schedule, Third getCal, for returning finalCall value, Fourth Accident, using the revert technique, the result of the Ambulance variable is returned depending on whether it is required or not.

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
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile trainVID.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "TrainScheduling" contract from the dropdown menu, and then click on the "Deploy" button. 

Once the contract is deployed, you can interact with it by clicking on various functions. Click on the "TrainScheduling" contract in the left-hand sidebar, and then click on the functions, getting the results accordingly. Finally, to reverse the outcomes and print-related messages, click on the functions once more.

## Authors
Vidhika Bajaj

## License
This project is licensed under the MIT License
