## Whiteboarding Practice Problems

### Intro

Here are a list of questions that can be used to practice Whiteboarding. Some are easier and some are harder. Some might even be too easy, and some might even be too hard. Adjust and adapt as necessary. Perhaps add or remove a constraint if you need to change the difficulty on the fly.

Maybe a problem gets way harder in JavaScript if you're not allowed to use an object as the backing store, or maybe doing a problem with a constant time complexity is tremendously challenging and might not fit well inside the bounds of an technical interview. It's not the interviewer's goal to completely stump the interviewee, but to guide them to places of challenge and see them succeed. Practice finding the perfect amount of challenge to make it a great and successful interview.

These are intentionally pretty sparse. Be creative! Let the interviewer ask questions and work towards a more definitely specification.

### Problems

#### Reverse Words

Write a function that reverses the words in a sentence.

```
Sample Input:

Hello World

Sample Output:

World Hello
```

#### Swap Elements

Write a function that takes a list of numbers which is supplemented with positions that have to be swapped. Swap the numbers and return the list.

```
Sample Input:

1 2 3 4 5 6 7 8 9 : 0-8
1 2 3 4 5 6 7 8 9 10 : 0-1, 1-3

Sample Output:

9 2 3 4 5 6 7 8 1
2 4 3 1 5 6 7 8 9 10
```

#### JSON Menu IDs

Write a function that takes a JSON string which describes a menu. Calculate the SUM of IDs of all "items" in the case a "label" exists for an item. Return the sum.

```
Sample Input:

{"menu": {"header": "menu", "items": [{"id": 27}, {"id": 0, "label": "Label 0"}, null, {"id": 93}, {"id": 85}, {"id": 54}, null, {"id": 46, "label": "Label 46"}]}}

{"menu": {"header": "menu", "items": [{"id": 81}]}}

{"menu": {"header": "menu", "items": [{"id": 70, "label": "Label 70"}, {"id": 85, "label": "Label 85"}, {"id": 93, "label": "Label 93"}, {"id": 2}]}}

Sample Output:

46
0
248
```

#### Prime Palindrome

Write a function which determines the largest prime palindrome less than 1000.

```
Sample Input:

There is no input for this program.

Sample Output:

Print to stdout the largest prime palindrome less than 1000.
```

#### Set Intersection

Write a function that takes a string representation of two sorted list of numbers (ascending order). The lists themselves are comma delimited and the two lists are semicolon delimited. Print out the intersection of these two sets.

```
Sample Input:

1,2,3,4;4,5,6
20,21,22;45,46,47
7,8,9;8,9,10,11,12

Sample Output:

4

8,9
```

#### String Permutations

Write a function that takes a string and then prints all the permutations of that string in alphabetical order. We consider that digits < upper case letters < lower case letters. The sorting should be performed in ascending order.

```
Sample Input:

hat
abc
Zu6

Sample Output:

aht,ath,hat,hta,tah,tha
abc,acb,bac,bca,cab,cba
6Zu,6uZ,Z6u,Zu6,u6Z,uZ6
```

#### Reverse Array in Place

Write a function that takes an array and reverses it in place. That is, return the same array with the elements reverse. Don't create a new array.

```
Sample Input:

[1, 2, 3, 4, 5]

Sample Output:

[5, 4, 3, 2, 1]

```

#### Unique Elements

Write a function that takes a sorted list of numbers with duplicates. Print out the sorted list with duplicates removed.

```
Sample Input:

1,1,1,2,2,3,3,4,4
2,3,4,5,5

Sample Output:

1,2,3,4
2,3,4,5
```

### Additional Resources

If you've seen all of the above problem once already.. go through them again! :) Seeing problems repeatedly can be very helpful. If you've seen them all a ton already check out some of the following resources for more practice.

#### Toy Problems

Pick some of the most challenging Toy Problems, even if you've already completed them, and complete them in a whiteboarding session. It adds quite a bit of challenge to have to solve a problem on a board with someone watching. Even if you've solved it before.

#### CodeEval

[CodeEval](http://www.codeeval.com) is a great resource for short problems and they will even test your solution code for you.

#### Project Euler

[Project Euler](http://www.projecteuler.net) is another huge list of problems that are great for solving with computers. They are super mathy so get ready for that.

#### Cracking the Coding Interview

[Cracking the Coding Interview](http://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X) is a super good resource for technical job interviews. There are tons of great practice questions included. Worth every penny.
