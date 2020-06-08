# DSA-Recursion
 1. Counting Sheep
Write a recursive function that counts how many sheep jump over the fence. Your program should take a number as input. That number should be the number of sheep you have. The function should display the number along with the message "Another sheep jumps over the fence" until no more sheep are left.

Input: 3
Output:
3: Another sheep jumps over the fence
2: Another sheep jumps over the fence
1: Another sheep jumps over the fence
All sheep jumped over the fence
-
function CountingSheep(sheep){
 if(sheep === 0){
 	return console.log('All sheep jumped over the fence');
 } else {
 	console.log(sheep, 'Another sheep jumps over the fence');
   return CountingSheep(sheep)
 }
}

CountingSheep(3);

2. Power Calculator
Write a function called powerCalculator() that takes two parameters, an integer as a base, and another integer as an exponent. The function returns the value of the base raised to the power of the exponent. Use only exponents greater than or equal to 0 (positive numbers)

powerCalculatorRec(10,2) should return 100
powerCalculatorRec(10,-2) should return exponent should be >= 0

-
function PowerCalculator(base, exp) {
    if(exp < 0){
		 console.log('exponent should be >= 0');
	return null;	
} else if (exp === 1){
		return base;
	} else {
		base = base * base;
		return PowerCalculator(base, exp - 1);
    }
}

3. Reverse String
Write a function that reverses a string. Take a string as input, reverse the string, and return the new string.
-
function reverseString(str){
  if (str === '') {
    return ''
  }  else {
    return reverseString(str.substr(1)) + str.charAt(0);
  }  
}

4. nth Triangular Number
Calculate the nth triangular number. A triangular number counts the objects that can form an equilateral triangle. The nth triangular number is the number of dots composing a triangle with n dots on a side, and is equal to the sum of the n natural numbers from 1 to n. This is the Triangular Number Sequence: 1, 3, 6, 10, 15, 21, 28, 36, 45.

function nthTriangle(n){
  return (n <= 1) ? n : n + nthTriangle(n - 1); 
}
5 - String Splitter

Split a string based upon a separator (similar to String.prototype.split).

What is the input to the program
What is the output of the program
What is the input to each recursive calls
What is the output of each recursive calls
Notes for later: have to use substring and splitter

6 - Binary Representation

Write a recursive function that prints out the binary representation of a given number. For example, the program should take 3 as an input and print 11 as output, or 25 as an input and print 11001 as an output. Note that the binary representation of 0 should be 0.

What is the input to the program
What is the output of the program
What is the input to each recursive calls
What is the output of each recursive calls

7 - Anagrams

An anagram is any word or phrase that exactly reproduces the letters in another order. Write a program that creates an anagram (listing all the rearrangements of a word) of a given word. For example, if the user types east, the program should list all 24 permutations, including eats, etas, teas, and non-words like tsae.

Hint: For your algorithm, you might want to think about a prefix and use that to create the new words. For example, given east, use e as a prefix and you would place e in front of all six permutations of ast — ast, ats, sat, sta, tas, and tsa. This will give you the words east, eats, esat, esta, etas, and etsa. Continue this way until you find all the anagrams for east. There should be 24 of them.

What is the input to the program
What is the output of the program
What is the input to each recursive calls

8 - Animal Hierarchy

Step through the code and find the input to the program, input to each recursive calls, output of each recursive calls and the output of the program. The purpose of this exercise is not for you to copy paste the code and find out the output but rather step through each line, analyze each step to understand how recursion works.

const AnimalHierarchy = [ {id: 'Animals','Parent': null}, {id: 'Mammals','Parent': 'Animals'}, {id: 'Dogs','Parent':'Mammals' }, {id: 'Cats','Parent':'Mammals' }, {id: 'Golden Retriever','Parent': 'Dogs'}, {id: 'Husky','Parent':'Dogs' }, {id: 'Bengal','Parent':'Cats' } ]

// ============================== function traverse(AnimalHierarchy, parent) { let node = {}; AnimalHierarchy.filter(item => item.Parent === parent) .forEach(item => node[item.id] = traverse(AnimalHierarchy, item.id)); return node;
} console.log(traverse(AnimalHierarchy, null));

What is the input to the program
What is the output of the program
What is the input to each recursive calls
What is the output of each recursive calls
9 - Factorial

Write a recursive program that finds the factorial of a given number. The factorial of a number can be found by multiplying that number by each number between itself and one. The factorial of 5 is equal to 5 * 4 * 3 * 2 * 1 = 120

What is the input to the program
What is the output of the program
What is the input to each recursive calls
What is the output of each recursive calls

 10 - Fibonacci

Write a recursive program that prints the fibonacci sequence of a given number. The fibonnaci sequence a series of numbers in which each number is the sum of the two preceding numbers. For example the 7th fibonacci number in a fibonaci sequence is 13. The sequence looks as follows: 1 1 2 3 5 8 13.

What is the input to the program
What is the output of the program
What is the input to each recursive calls
What is the output of each recursive calls

11 - Organization Chart

Write a recursive program that prints the following organization chart. Your output should show the output to be as shown below with proper indentation to show the hierarchy.

Zuckerberg Schroepfer Bosworth Steve Kyle Andra Zhao Richie Sofia Jen Schrage VanDyck Sabrina Michelle Josh Swain Blanch Tom Joe Sandberg Goler Eddie Julie Annie Hernandez Rowi Inga Morgan Moissinac Amy Chuck Vinni Kelley Eric Ana Wes
