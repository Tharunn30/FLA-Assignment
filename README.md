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
No. of states: 3
No. of transitions: 2

State 1:
Path 0: q0 q1
Path 1: q0
Path 2: q1

State 2:
Path 0: q2
Path 1: q2

State 3:
Path 0: q1
Path 1: q0 q1

Final state of NFA: q2
```

**Output:**

*NFA Table:*
```
   q0    q1    q2
0  q1  q0 q1     
1  q1        q2  
2  q0  q1         
```

*DFA Table:*
```
    q0q1    q2
0  q1q0q1     
1  q1q2       
2  q0q1     
```

*Final States of DFA:*
```
Final states of the DFA are :  ['q1q2', 'q0q1q2']
```

### Note
- The script uses the pandas library to display the NFA and DFA tables. Make sure you have pandas installed (`pip install pandas`) before running the script.
