### Problem

You are given a positive integer AA. Find the number of factors of AA which are palindromes. A number is called a [palindrome](https://en.wikipedia.org/wiki/Palindromic_number) if it remains the same when the digits in decimal representation are reversed. For instance, 121 is a palindrome, while 123 is not.

### Input

The first line of the input gives the number of test cases, T. T lines follow.

Each line represents a test case and contains a single integer A.

### Output

For each test case, output one line containing `Case #x: y`, where xx is the test case number (starting from 1) and y is the number of factors of AA which are palindromes.

### Limits

Time limit: 2 seconds.
Memory limit: 1 GB.
1≤T≤100

#### Test Set 1

1≤A≤10^3^

#### Test Set 2

1≤A≤10^10^

### Sample

Sample Input

```
4
6
10
144
242
```

Sample Output

```
Case #1: 4
Case #2: 3
Case #3: 7
Case #4: 6
```

In the first test case, AA has 44 factors which are palindromes: 1,2,3,1,2,3, and 66.
In the second test case, AA has 33 factors which are palindromes: 1,2,1,2, and 55.
In the third test case, AA has 77 factors which are palindromes: 1,2,3,4,6,8,1,2,3,4,6,8, and 99.
In the fourth test case, AA has 66 factors which are palindromes: 1,2,11,22,121,1,2,11,22,121, and 242242.