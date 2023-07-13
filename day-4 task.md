**1. Do the below programs in anonymous function & IIFE in js**

**a. Print odd numbers in an array:**

 **Using anonymous function:**
 
```js
let arr = [1,2,3,4,5,6,7,8,9];
arr.forEach(function(num){
  if(num%2 !== 0){
    console.log(num);
  }
});

```

**Using IIFE:**

```js
let arr = [1,2,3,4,5,6,7,8,9];
(function(){
  arr.forEach(function(num){
    if(num%2 !== 0){
      console.log(num);
    }
  });
})();

```


**b . Convert all the strings to title caps in a string array:**

**Using anonymous function:**

```js
let strArr = ['hello', 'world', 'javascript'];
let newStrArr = strArr.map(function(str){
  return str.charAt(0).toUpperCase() + str.slice(1).toLowerCase();
});
console.log(newStrArr);

```

**Using IIFE:**

```js
let strArr = ['hello', 'world', 'javascript'];
let newStrArr = (function(){
  return strArr.map(function(str){
    return str.charAt(0).toUpperCase() + str.slice(1).toLowerCase();
  });
})();
console.log(newStrArr);

```

**c . Sum of all numbers in an array:**

**Using anonymous function:**

```js
let arr = [1,2,3,4,5,6,7,8,9];
let sum = 0;
arr.forEach(function(num){
  sum += num;
});
console.log(sum);

```

**Using IIFE:**

```js
let arr = [1,2,3,4,5,6,7,8,9];
let sum = (function(){
  let result = 0;
  arr.forEach(function(num){
    result += num;
  });
  return result;
})();
console.log(sum);

```

**d. Return all the prime numbers in an array:**

**Using anonymous function:**

```js
let arr = [2,3,4,5,6,7,8,9];
let primeArr = [];
arr.forEach(function(num){
  let isPrime = true;
  for(let i=2; i<num; i++){
    if(num%i === 0){
      isPrime = false;
      break;
    }
  }
  if(isPrime && num > 1){
    primeArr.push(num);
  }
});
console.log(primeArr);

```

**Using IIFE:**

```js
let arr = [2,3,4,5,6,7,8,9];
let primeArr = (function(){
  let result = [];
  arr.forEach(function(num){
    let isPrime = true;
    for(let i=2; i<num; i++){
      if(num%i === 0){
        isPrime = false;
        break;
      }
    }
    if(isPrime && num > 1){
      result.push(num);
    }
  });
  return result;
})();
console.log(primeArr);

```

**e . Return all the palindromes in an array:**

**Using anonymous function:**

```js
let arr = ['hello', 'world', 'Nithish', 'javascript'];
let palindromeArr = [];
arr.forEach(function(str){
  let reversedStr = str.split('').reverse().join('');
  if(str === reversedStr){
    palindromeArr.push(str);
  }
});
console.log(palindromeArr);

```

**Using IIFE:**

```js
let arr = ['hello', 'world', 'Nithish', 'javascript'];
let palindromeArr = (function(){
  let result = [];
  arr.forEach(function(str){
    let reversedStr = str.split('').reverse().join('');
    if(str === reversedStr){
      result.push(str);
    }
  });
  return result;
})();
console.log(palindromeArr);

```

**f. Return median of two sorted arrays of the same size:**

**Using anonymous function:**

```js
let arr1 = [1, 3, 5, 7];
let arr2 = [2, 4, 6, 8];
let mergedArr = arr1.concat(arr2);
mergedArr.sort(function(a,b){
  return a-b;
});
let len = mergedArr.length;
let median = (len%2 !== 0) ? mergedArr[Math.floor(len/2)] : (mergedArr[len/2 - 1] + mergedArr[len/2]) / 2;
console.log(median);

```

**Using IIFE:**

```js
let arr1 = [1, 3, 5, 7];
let arr2 = [2, 4, 6, 8];
let median = (function(){
  let mergedArr = arr1.concat(arr2);
  mergedArr.sort(function(a,b){
    return a-b;
  });
  let len = mergedArr.length;
  return (len%2 !== 0) ? mergedArr[Math.floor(len/2)] : (mergedArr[len/2 - 1] + mergedArr[len/2]) / 2;
})();
console.log(median);

```

**g . Remove duplicates from an array:**

**Using anonymous function:**

```js
let arr = [1, 2, 2, 3, 4, 4, 5, 5];
let uniqueArr = [];
arr.forEach(function(num){
  if(uniqueArr.indexOf(num) === -1){
    uniqueArr.push(num);
  }
});
console.log(uniqueArr);

```

**Using IIFE:**

```js
let arr = [1, 2, 2, 3, 4, 4, 5, 5];
let uniqueArr = (function(){
  let result = [];
  arr.forEach(function(num){
    if(result.indexOf(num) === -1){
      result.push(num);
    }
  });
  return result;
})();
console.log(uniqueArr);

```

**h . Rotate an array by k times:**

**Using anonymous function:**

```js
let arr = [1, 2, 3, 4, 5];
let k = 3;
for(let i=0; i<k; i++){
  arr.unshift(arr.pop());
}
console.log(arr);

```

**Using IIFE:**

```js
let arr = [1, 2, 3, 4, 5];
let k = 3;
arr = (function(){
  for(let i=0; i<k; i++){
    arr.unshift(arr.pop());
  }
  return arr;
})();
console.log(arr);

```


**2 . Do the below programs in arrow functions.**

**a. Print odd numbers in an array:**

```js
let arr = [1, 2, 3, 4, 5];
let oddNumbers = arr.filter(num => num % 2 !== 0);
console.log(oddNumbers);

```

**b.  Convert all the strings to title caps in a string array:**

```js
let arr = ["hello", "world", "javascript"];
let titleCaps = arr.map(str => str.charAt(0).toUpperCase() + str.slice(1).toLowerCase());
console.log(titleCaps);

```

**c. Sum of all numbers in an array:**

```js
let arr = [1, 2, 3, 4, 5];
let sum = arr.reduce((acc, curr) => acc + curr);
console.log(sum);

```

**d. Return all the prime numbers in an array:**

```js
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let isPrime = num => {
  if(num <= 1) return false;
  for(let i=2; i<=Math.sqrt(num); i++){
    if(num % i === 0) return false;
  }
  return true;
}
let primeNumbers = arr.filter(isPrime);
console.log(primeNumbers);

```

**e. Return all the palindromes in an array:**

```js
let arr = ["Nithish", "javascript", "hello", "world"];
let isPalindrome = str => str === str.split("").reverse().join("");
let palindromes = arr.filter(isPalindrome);
console.log(palindromes);

```
