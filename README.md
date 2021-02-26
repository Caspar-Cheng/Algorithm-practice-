# Algorithm Practice
This is a record of practice on Algorithm


1. Algorithm question one -- two number sum
Write a function to take two number from a non-empty intergers array, numbers in array are not repeatable, set the target number, if any two number sum equals to the target number, return the output as an array with those two numbers inside. Example test input: 
array = [3, 5, -4, 8, 11, 1, -1, 6]
targetNum = 10
example output: [-1, 11]

Solution in JS: 

function sumTwoNum(array, targetNum){

    for(let i=0; i<array.length-1; i++){ 
  
      const firstNum = array[i];   
    
      for(let j=i+1; j<array.length; j++){  
    
        const secondNum = array[j];      
      
        if(firstNum + secondNum === targetNum){  
      
          return [firstNum, secondNum];
        
      }
    }
  } 
    return [ ]; 
}

exports.sumTwoNum = sumTwoNum;





2. Algorithm question two: validate subsequence. Given two non-empty int arrays, write a function to check whether the second array is the subsquence of the first array. If the second array belongs to the first array, return true, the order doesn't need to be as same as the first one. 
Sample input: 
array = [5, 1, 22, 25, 6, -1, 8, 10]
sequence = [1, 6, -1, 10]
Output: true

function isSubsequence(array, sequence){

    let arrIndex = 0;
    
    let seqIndex = 0;
    
    while(arrIndex < array.length && seqIndex < sequence.length){
    
        if(array[arrIndex] === sequence[seqIndex]){
            
            seqIndex++;
            arrIndex++;
        }
    
    return seqIndex === sequence.length
    
    }
    
}

exports.isSubsequence = isSubsequence
