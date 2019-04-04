/*
    Return the length of the longest word in the provided sentence.!
*/

function findLongestWordLength(str) {
    let indexOfLatestSpace = 0;
    let longestWordLength = 0;
  for (let i = 0; i < str.length; i++){
      if(str[i] == " " && i - (indexOfLatestSpace + 1) >= longestWordLength){
      longestWordLength = i -  (indexOfLatestSpace + 1);
      indexOfLatestSpace = i;
      }
      else if (str[i] == " "){
          indexOfLatestSpace = i;
      }

  }
    let lastWordLength = str.length - (indexOfLatestSpace + 1)
      if(lastWordLength >= longestWordLength ){
          longestWordLength = lastWordLength;
      }
  return longestWordLength;
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");
console.log(findLongestWordLength("The quick brown fox jumped over the lazy dog"));

/*

    Return an array consisting of the largest number from each provided sub-array. For simplicity, the provided array will contain exactly 4 sub-arrays.

*/
function largestOfFour(arr) {
  // You can do this!
  let newArr = [];
  let biggestNum = 0;
  for (let i = 0; i < arr.length; i++){
      
      for( let j = 0; j < arr[i].length; j++){   
      if (arr[i][j] >= biggestNum){
         biggestNum = arr[i][j];
      }
      }
      newArr.push(biggestNum);
      biggestNum = 0;
  }
  return newArr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
console.log(largestOfFour([[13, 27, 18, 26], [4, 5, 1, 3], [32, 35, 37, 39], [1000, 1001, 857, 1]]));

/*

    Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.
    For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".

*/
function titleCase(str) {
  let newStr = str.charAt(0).toUpperCase();
  let latestSpace;
  for (let i = 1; i < str.length; i++){
   if (str[i] == " "){
     latestSpace = i;
     newStr += str[i];
     newStr += str.charAt(i+1).toUpperCase();
   }
   else if (latestSpace != undefined && i != latestSpace + 1 ){
     newStr += str.charAt(i).toLowerCase();
   }
   else if (i != latestSpace + 1) {
     newStr += str.charAt(i).toLowerCase();
   }

  }
  return newStr;
}

titleCase("I'm a little tea pot");
console.log(titleCase("I'm a little tea pot"));

/*

    You are given two arrays and an index.

    Use the array methods slice and splice to copy each element of the first array into the second array, in order.

    Begin inserting elements at index n of the second array.

    Return the resulting array. The input arrays should remain the same after the function runs.

*/

function frankenSplice(arr1, arr2, n) {
  // It's alive. It's alive!
  let newArr2 = [...arr2];
  newArr2.splice(n ,0 , arr1.slice(0));
  return newArr2;
}

frankenSplice([1, 2, 3], [4, 5, 6], 1);
console.log(frankenSplice(["claw", "tentacle"], ["head", "shoulders", "knees", "toes"], 2));

///// or ////

function frankenSplice(arr1, arr2, n) {
  // It's alive. It's alive!
  let newArr2 = [...arr2];
  newArr2.splice(n ,0 , ...arr1);
  return newArr2;
}

frankenSplice([1, 2, 3], [4, 5, 6], 1);
console.log(frankenSplice(["claw", "tentacle"], ["head", "shoulders", "knees", "toes"], 2));

/*

    Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

    For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).

    Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).

*/

function getIndexToIns(arr, num) {
  // Find my place in this sorted array.
   arr.sort((a, b)=> a - b);
   console.log(arr) 
  for (let i = arr.length - 1 ; i >= 0; i--){
    if (num > arr[i]){
      return i + 1;
    }
  }
  return 0;
}

console.log(getIndexToIns([2, 5, 10], 15));

/*

    Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

    For example, ["hello", "Hello"], should return true because all of the letters in the second string are present in the first, ignoring case.

    The arguments ["hello", "hey"] should return false because the string "hello" does not contain a "y".

    Lastly, ["Alien", "line"], should return true because all of the letters in "line" are present in "Alien".

*/

function mutation(arr) {
  let str1 = arr[0];
  let str2 = arr[1];
  let passCounter = 0;
  let newStr = "";
 for (let i = 0; i < str2.length; i++){
   for(let j = 0; j < str1.length; j++){
       if(str2.charAt(i).toUpperCase() == str1.charAt(j).toUpperCase()){
         passCounter++;
         newStr += str2.charAt(i);
         console.log(newStr)
       }
   }
 }
 if (passCounter >= str2.length){
   return true;
 }
 if (passCounter){
  
 }
  return false;
}

mutation(["hello", "hey"]);
console.log(mutation(["voodoo", "no"]));

    ////// or this, it works better!

function mutation(arr) {
  let str1 = arr[0].toUpperCase();
  let str2 = arr[1].toUpperCase();
  let passCounter = 0;
  for (let i = 0; i < str2.length; i++){
      if(str1.search(str2.charAt(i)) != -1){
        passCounter++;
        console.log(passCounter);
      }
  }
  if (passCounter == str2.length){
    return true;
  }
  return false;
}


console.log(mutation(["hello", "Hello"]));


/*

    Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.

*/

function chunkArrayInGroups(arr, size) {
  // Break it up.
  let newArr = [];
  for (let i = arr.length / size; i > 0; i--){
    newArr.push(arr.splice(0, size));
    console.log(arr)
  }

  return newArr;
}


console.log(chunkArrayInGroups(["a", "b", "c", "d"], 2));
