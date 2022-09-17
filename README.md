# dp_table
A new data structure that can avoid extra memory space in Dynamic Programming problems. (Still in implementation phase)

Tabulation visits every possible subproblem which may not be required to be computed and hence a tabulation table ends up using extra space (for unnecessary problems)

Memoization is perfect for single keys. For example [state] -> f(state), but if we need to solve problems of DP where there are multiple states/parameters, we will need someting like 

```[state1][state2][state3]....[stateN] -> f(state1,state2,state3,...stateN)```

![image](https://user-images.githubusercontent.com/39441413/190867414-38de5bc4-38dc-48da-9c7b-5d37897453b3.png)

It is a function mapping to another function mapping to another function and so on..

Lets say we want to represent the above mappings in C++, Then it would be somewhat like

```unordered_map<auto, unordered_map<unordered_map<auto, auto>> >```

Hence the lookup if just O(1) Constant time and so is adding and deleting without wasting extra space (in case of tabulation table).
