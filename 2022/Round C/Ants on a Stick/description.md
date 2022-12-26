### Problem

Ada has NN ants labelled from 11 to NN. She decides to test John's concentration skills. She takes a stick LL cm long, and drops the ants on it.

The positions on the stick at which the ants are dropped are represented by an integer array PP, where ant ii is dropped at the position PiPi (that is, PiPi cm away from the left end) on the stick. Each ant travels either to the left or right with a constant speed of 11 cm per second. The initial directions of the ants is represented by an array DD, where the direction of ant ii is DiDi: 00 if left, and 11 if right. When two ants meet, they bounce off each other and reverse their directions. The ants fall off the stick when they reach either end of it.

Ada challenges John to find the exact order in which the ants fall off the stick. John needs your help!

### Input

The first line of the input gives the number of test cases, TT. TT test cases follow.
The first line of each test case contains two integers, NN and LL: the number of ants, and the length of the stick, respectively.
The next NN lines describe the positions and directions of the ants. The ii-th line contains two integers, PiPi and DiDi: the position and direction of ant ii, respectively.

### Output

For each test case, output one line containing `Case #xx: A1A2…ANA1A2…AN`, where xx is the test case number (starting from 1), and AiAi is the label of the ii-th ant that falls off the stick. In other words, the first ant to fall off the stick is the ant labelled A1A1, the second is the ant labelled A2A2, and so on. If multiple ants fall off at the same time, output their labels in the *increasing* order.

### Limits

Memory limit: 1 GB.
1≤T≤100
N<LN<L.
Di∈{0,1}Di∈{0,1}, for all i.
0<P_i_<L, for all i.
All Pi are distinct.

#### Test Set 1

Time limit: 20 seconds.
1≤N≤10
1≤L≤100

#### Test Set 2

Time limit: 40 seconds.
1≤N≤1031≤N≤103.
1≤L≤1091≤L≤109.

#### Test Set 3

Time limit: 40 seconds.
1≤L≤10^9^
For at most 15 cases:
1≤N≤10^5^
For the remaining cases:
1≤N≤10^3^

### Sample

Sample Input

```
3
1 5
1 1
2 7
4 1
5 0
4 10
8 0
2 1
6 1
4 0
```

Sample Output

```
Case #1: 1
Case #2: 2 1
Case #3: 1 2 3 4
```

In Sample Case #1, as there is only a single ant (labelled 11), it is the only one to fall off. The time at which it falls off is 44 seconds.

In Sample Case #2, the two ants move towards each other, meet at 0.50.5 seconds and reverse their directions. Ant 22 then reaches the right end of the stick at 33 seconds, whereas ant 11 reaches the left end at 55 seconds. Thus, ant 22 falls off the stick, followed by ant 11.

In Sample Case #3, ants 22 and 44 move towards each other and meet at 11 second. Similarly, ants 11 and 33 also move towards each other and meet at 11 second. All 44 ants then change directions.

- Ants 11 and 22 move towards either ends of the stick and fall off at 44 seconds.
- Ants 33 and 44 move towards each other and meet at 33 seconds. They change directions and move towards either ends of the stick, and fall off at 88 seconds.