# FLA-Assignment
NFA to DFA Conversion 

This code is for NFA to DFA conversion.
It takes input from the user.

This is the sample input for the code:

No. of states : 4

No. of transitions : 2

state name : A
path : a
Enter end state from state traveling through path a:
A B
path : b
Enter end state from state A traveling through path b:
A
state name : B
path : a
Enter end state from state B travelling through path a:
C
path : b
Enter end state from state B travelling through path b:
C
state name : C
path : a
Enter end state from state C while traveling through path a:
D
path : b
Enter end state from state C travelling through path b : 
D
state name : D
path : a
Enter end state from state D travelling through path a : 

path : b
Enter end state from state D travelling through path b : 

Sample output : 
NFA :- 

{'A': {'a': ['A', 'B'], 'b': ['A']}, 'B': {'a': ['C'], 'b': ['C']}, 'C': {'a': ['D'], 'b': ['D']}, 'D': {'a': [], 'b': []}}

Printing NFA table :- 
        a    b
A  [A, B]  [A]
B     [C]  [C]
C     [D]  [D]
D      []   []
Enter final state of NFA : 
D

DFA :- 

{'A': {'a': 'AB', 'b': 'A'}, 'AB': {'a': 'ABC', 'b': 'AC'}, 'ABC': {'a': 'ABCD', 'b': 'ACD'}, 'AC': {'a': 'ABD', 'b': 'AD'}, 'ABCD': {'a': 'ABCD', 'b': 'ACD'}, 'ACD': {'a': 'ABD', 'b': 'AD'}, 'ABD': {'a': 'ABC', 'b': 'AC'}, 'AD': {'a': 'AB', 'b': 'A'}}

Printing DFA table :- 
         a    b
A       AB    A
AB     ABC   AC
ABC   ABCD  ACD
AC     ABD   AD
ABCD  ABCD  ACD
ACD    ABD   AD
ABD    ABC   AC
AD      AB    A

Final states of the DFA are :  ['ABCD', 'ACD', 'ABD', 'AD']
