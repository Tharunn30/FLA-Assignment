# NFA to DFA Conversion

This Python script converts a Non-Deterministic Finite Automaton (NFA) into a Deterministic Finite Automaton (DFA). It takes user input for the number of states and transitions, collects transition details, and then generates the corresponding DFA.

### Prerequisites

- Python 3.x
- pandas library (Install using `pip install pandas`)

### Usage

1. Run the script.
2. Enter the number of states `n` and the number of transitions `t`.
3. For each state, provide the state name and its transitions using various input paths.
4. Enter the final state of the NFA.

### Input

- Number of states (`n`)
- Number of transitions (`t`)
- For each state `i` from `1` to `n`:
    - State name
    - `t` transitions with paths and the states reachable from the current state through each path
- Final state of NFA

### Output

1. **NFA Table:** 
   - Displays the input NFA in tabular format.
   
2. **DFA Table:** 
   - Displays the converted DFA in tabular format.

3. **Final States of DFA:** 
   - Lists the final states of the generated DFA.

### How it Works

1. **Input NFA Processing:**
   - Accepts user input for NFA states and transitions.
   - Constructs the NFA table.

2. **DFA Conversion:**
   - Converts the NFA transitions into equivalent DFA transitions.
   - Computes the DFA table and final states.

### Example

**Input:**
```
No. of states : 4
No. of transitions : 2
state name : A
path : a
Enter end state from state A travelling through path a : A B
path : b
Enter end state from state A travelling through path b : A
state name : B
path : a
Enter end state from state B travelling through path a : C
path : b
Enter end state from state B travelling through path b : C
state name : C
path : a
Enter end state from state C travelling through path a : D
path : b
Enter end state from state C travelling through path b : D
state name : D
path : a
Enter end state from state D travelling through path a : 
path : b
Enter end state from state D travelling through path b : 

```

**Output:**

*NFA Table:*
```
        a    b
A  [A, B]  [A]
B     [C]  [C]
C     [D]  [D]
D      []   []
      
```

*DFA Table:*
```
         a    b
A       AB    A
AB     ABC   AC
ABC   ABCD  ACD
AC     ABD   AD
ABCD  ABCD  ACD
ACD    ABD   AD
ABD    ABC   AC
AD      AB    A
   
```

*Final States of DFA:*
```
Final states of the DFA are :  ['ABCD', 'ACD', 'ABD', 'AD']
```

### Note
- The script uses the pandas library to display the NFA and DFA tables. Make sure you have pandas installed (`pip install pandas`) before running the script.
