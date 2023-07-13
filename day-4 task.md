1. Do the below programs in anonymous function & IIFE in js

a. Print odd numbers in an array:

Using anonymous function:


let arr = [1,2,3,4,5,6,7,8,9];
arr.forEach(function(num){
  if(num%2 !== 0){
    console.log(num);
  }
});
