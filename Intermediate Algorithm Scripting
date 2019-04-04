/*

    Make a function that looks through an array of objects (first argument) and returns an array of all objects that have matching name and value pairs (second argument). Each name and value pair of the source object has to be present in the object from the collection if it is to be included in the returned array.

    For example, if the first argument is [{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], and the second argument is { last: "Capulet" }, then you must return the third object from the array (the first argument), because it contains the name and its value, that was passed on as the second argument.

*/
function whatIsInAName(collection, source) {
  // What's in a name?
  var arr = [];
  let arr2 = Object.entries(source);
     console.log(arr2);
     let pass = 0;
  for (let i = 0; i < collection.length; i++){
       for(let j = 0; j < arr2.length; j++){
         if(collection[i][arr2[j][0]] == arr2[j][1]){
           pass++;
         }


       }
       if (pass == arr2.length)
        arr.push(collection[i]);
        pass = 0;
      }
  
  return arr;
}


console.log(JSON.stringify(whatIsInAName([{ "apple": 1, "bat": 2 }, { "apple": 1 }, { "apple": 1, "bat": 2, "cookie": 2 }], { "apple": 1, "cookie": 2 })));

/*

    Convert a string to spinal case. Spinal case is all-lowercase-words-joined-by-dashes.

*/

function spinalCase(str) {
  // "It's such a fine line between stupid, and clever."
  // --David St. Hubbins
    let arr1 = str.split(/\s?(?=[A-Z])|\W|[^a-zA-Z0-9\s]/);
     console.log(arr1);
    let myStr1 = arr1.join("-");
    return myStr1.toLowerCase();
  // let arr = str.split(/\W/)
  // let myStr = arr.join("-")
  // return myStr.toLowerCase();
}

spinalCase('This Is Spinal Tap');

console.log(spinalCase("The_Andy_Griffith_Show"));

/*

    Translate the provided string to pig latin.

    Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay".

    If a word begins with a vowel you just add "way" to the end.

    Input strings are guaranteed to be English words in all lowercase.

*/

function translatePigLatin(str) {

  let newStr = str;
  if(str.charAt(0) == "a" || str.charAt(0) == "e" || str.charAt(0) == "i" || str.charAt(0) == "o" || str.charAt(0) == "u"){
    return newStr + 'way';
  }
  else {
    let arr = newStr.split(/(?=a|e|i|o|u)/)
    let firstpart = arr.shift();
    newStr = arr.join("");
    console.log(arr);
    return newStr + firstpart + "ay";
  }
}

// translatePigLatin("consonant");
console.log(translatePigLatin("california"))

/*

    "DNA Pairing"
    The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

    Base pairs are a pair of AT and CG. Match the missing element to the provided character.

    Return the provided character as the first element in each array.

    For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

    The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.

*/

function pairElement(str) {
let mainArr = [];
let inArr = [];
let arr = str.split("");
console.log(arr);
for (let i = 0; i < arr.length; i++){
  inArr.push(arr[i])
  switch(arr[i]){
    case "G":
    inArr.push("C");
    mainArr.push(inArr);
    inArr = [];
    break;
    case "C":
    inArr.push("G");
    mainArr.push(inArr);
    inArr = [];
    break;
    case "A":
    inArr.push("T");
    mainArr.push(inArr);
    inArr = [];
    break;
    case "T":
    inArr.push("A");
    mainArr.push(inArr);
    inArr = [];
    break;
    default:
    console.log("nothing");
  }
}
  return mainArr;
}

pairElement("GCG");
console.log(JSON.stringify(pairElement("GCG")));

/*

    "Missing letters"
    Find the missing letter in the passed letter range and return it.
    If all letters are present in the range, return undefined.

*/

function fearNotLetter(str) {
  let missing = [];
  let strArr = str.split("");
  // console.log(JSON.stringify(strArr));
  let criteria = "abcdefghijklmnopqrstuvwxyz".split("");
  // console.log(JSON.stringify(criteria));
  let miniArr = criteria.splice(criteria.indexOf(strArr[0]), strArr.length + 1);
  // console.log(miniArr);
  for(let i = 0; i < strArr.length; i++){
    if(miniArr.indexOf(strArr[i]) >= 0)
    miniArr.splice(miniArr.indexOf(strArr[i]), 1);
    // console.log(miniArr);
  }

  return miniArr[0];
}

fearNotLetter("abce");
console.log(fearNotLetter("abce"))

/*

    "Sorted Union"
    Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.
    In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.
    The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.
    
*/

function uniteUnique(...arr) {
  let mainArr = [];
  mainArr = mainArr.concat(arr);
  let newArr = [];
  for (let i = 0; i < mainArr.length; i++){
    for(let j = 0; j < mainArr[i].length; j++){
      if(newArr.indexOf(mainArr[i][j]) == -1)
      newArr.push(mainArr[i][j]);
      console.log(newArr);
    }
  }
  return newArr;
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);

/*

    "Convert HTML Entities"
    Convert the characters &, <, >, " (double quote), and ' (apostrophe), in a string to their corresponding HTML entities.

*/

function convertHTML(str) {
  // &colon;&rpar;
  let newStr = str;
  if (newStr.search("&") >= 0){
  newStr = newStr.replace(/&/g, "&​amp;")
  }
  if (newStr.search("<") >= 0){
  newStr = newStr.replace(/</g, "&​lt;")
  }
  if (newStr.search(">") >= 0){
  newStr = newStr.replace(/>/g, "&​gt;")
  }
  if (newStr.search('"') >= 0){
  newStr = newStr.replace(/"/g, "&​quot;")
  }
  if (newStr.search("'" ) >= 0){
  newStr = newStr.replace(/'/g, "&​apos;")
  }

  
  return newStr;
}

convertHTML("Dolce & Gabbana");
console.log(convertHTML('Stuff in "quotation marks"'));

/*

    "Sum All Primes"
    Sum all the prime numbers up to and including the provided number.
    A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two.
    The provided number may not be a prime.

*/

function sumPrimes(num) {
  let primes = [2]
  let pass = 0;
  let sum = 0;
  for (let i = 3; i <= num;i++){
    console.log(i + ' first loop')
    for(let j = 0; j < primes.length; j++){
       if(i % primes[j] == 0 && i != j){
         pass++;
         console.log(pass + ' is not a prime')
       }

    }
    if (pass == 0){
    primes.push(i);
    console.log(primes + 'here')
    }

    else{
     pass = 0;
    } 
   

  }
primes.forEach( (item)=> sum += item);
  return sum;
}


sumPrimes(10);
console.log(sumPrimes(10));

/*

    "Smallest Common Multiple"
    Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters.
    The range will be an array of two numbers that will not necessarily be in numerical order.
    For example, if given 1 and 3, find the smallest common multiple of both 1 and 3 that is also evenly divisible by all numbers between 1 and 3. The answer here would be 6.

*/

function smallestCommons(arr) {
  /// sorting the provided array to easily create an array of numbers within range
  let newArr = arr.sort( (x, y)=> x - y);
  console.log(newArr + ' sorted');
/// this var will help us stop the loop when we catch the needed SCM! :)
  let stop = 0;
// this var is going to be the array which contains the the number within range
  let rangeArr = [];
//create the range array by pushing the numbers that come between the two numbers provided
  rangeArr.push(newArr[0]);
/// this loop, creates the range array
  for(let j = newArr[newArr.length - 1] - newArr[0]; j > 1; j--){
    rangeArr.push(rangeArr[rangeArr.length - 1] + 1);
  }
  rangeArr.push(newArr[newArr.length - 1]);
//// this line check if the range array is completed
  console.log(rangeArr + ' rangeArr');
/// this monster loop looks for the needed number which will pass all the test /// the SCM! 
  for(var i = newArr[newArr.length - 1]; stop <= rangeArr.length; i++){

    for ( var n = 0; n < rangeArr.length; n++){
      if ( i % rangeArr[n] == 0)
       stop++;
    }
    if(stop == rangeArr.length)
    return i;
    else{
      stop = 0;
    }
  }
  return i;
}


// smallestCommons([1,5]);
console.log(smallestCommons([23,18]));

/*

    "Drop it"
    Given the array arr, iterate through and remove each element starting from the first element (the 0 index) until the function func returns true when the iterated element is passed through it.
    Then return the rest of the array once the condition is satisfied, otherwise, arr should be returned as an empty array.

*/

function dropElements(arr, func) {
  // Drop them elements.
  let result = [];
  let stop = false;
  arr.forEach( (item)=> {
    if (func(item) == true && stop == false){
    result = arr.slice(arr.indexOf(item));
    stop = true;
    }

   
  })
   return result;
}

dropElements([1, 2, 3], function(n) {return n < 3; });
console.log(dropElements([1, 2, 3, 9, 2], function(n) {return n > 2;}));

/*

    "Everything Be True"
    Check if the predicate (second argument) is truthy on all elements of a collection (first argument).
    In other words, you are given an array collection of objects. The predicate pre will be an object property and you need to return true if its value is truthy. Otherwise, return false.
    In JavaScript, truthy values are values that translate to true when evaluated in a Boolean context.

*/

function truthCheck(collection, pre) {
  // Is everyone being true?
  let arr = [...collection];
  if (arr.some( (item) => !!item[pre] == false )){
    return false;
  }
  else{
   return true;
  }
  
}

// truthCheck([{"user": "Tinky-Winky", "sex": "male"}, {"user": "Dipsy", "sex": "male"}, {"user": "Laa-Laa", "sex": "female"}, {"user": "Po", "sex": "female"}], "sex");
console.log(truthCheck([{"user": "Tinky-Winky", "sex": "male", "age": 0}, {"user": "Dipsy", "sex": "male", "age": 3}, {"user": "Laa-Laa", "sex": "female", "age": 5}, {"user": "Po", "sex": "female", "age": 4}], "age"))

/*

    "Arguments Optional"
    Create a function that sums two arguments together. If only one argument is provided, then return a function that expects one argument and returns the sum.
    For example, addTogether(2, 3) should return 5, and addTogether(2) should return a function.
    Calling this returned function with a single argument will then return the sum:
    var sumTwoAnd = addTogether(2);
    sumTwoAnd(3) returns 5.
    If either argument isn't a valid number, return undefined.

*/

function addTogether(x, y) {
  if(isNaN(x) == false && y == undefined){
    return function addSecond(y){
      if (typeof y == 'number'){
       return x + y;
      }
      return undefined;

    }
  }
  else if(typeof x == 'number' && typeof y == 'number'){
 return x + y ;
  }
  else {
     return undefined;
  }

}

addTogether(2,3);
console.log(addTogether(2)([3]));

/*

    "Make a Person"
    Fill in the object constructor with the following methods below:
    getFirstName() getLastName() getFullName() setFirstName(first) setLastName(last) setFullName(firstAndLast)
    Run the tests to see the expected output for each method.
    The methods that take an argument must accept only one argument and it has to be a string.
    These methods must be the only available means of interacting with the object.



*/

 /// building a function constructor that makes an object's properties private and accessable only through methods of the created object
var Person = function(firstAndLast) {
 
  let arr = firstAndLast.split(" ");
  let firstName = arr[0];
  let lastName = arr[1];
  this.getFullName = function() {
    return firstName + " " + lastName;
  };
  this.getFirstName = function(){
    return firstName;
  }
  this.getLastName = function(){
    return lastName;
  }
  this.setFirstName = function(first){
      firstName = first;
  }
  this.setLastName = function(last){
    lastName = last;
  }
  this.setFullName = function(firstAndLast){
   firstName = firstAndLast.split(" ")[0]
   lastName = firstAndLast.split(" ")[1];
  }

  return firstAndLast;
};

var bob = new Person('Bob Ross');
bob.getFullName();
console.log(bob.getFullName())

/*

    "Map the Debris"
    Return a new array that transforms the elements' average altitude into their orbital periods (in seconds).
    The array will contain objects in the format {name: 'name', avgAlt: avgAlt}.
    You can read about orbital periods on Wikipedia.
    The values should be rounded to the nearest whole number. The body being orbited is Earth.
    The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.

*/

function orbitalPeriod(arr) {
  var GM = 398600.4418;
  var earthRadius = 6367.4447;
  var newArr = [...arr];
  var avgAlt;
  newArr = arr.forEach( (item)=>{
  avgAlt = item["avgAlt"];
  console.log(avgAlt);
  let T = 2 * Math.PI * (Math.sqrt(Math.pow((earthRadius + avgAlt), 3)/GM));
  let newT = Math.round(T);
  console.log(newT);
  delete item["avgAlt"]
  console.log(item["avgAlt"] + " lol")
  item["orbitalPeriod"] = newT;
  })
  return arr;
}

orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}]);
console.log(JSON.stringify(orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}])));
