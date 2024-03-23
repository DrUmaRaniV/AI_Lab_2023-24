# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 23/03/2024                                                                           
### REGISTER NUMBER : 212221040093
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:

```
and(0,0,0).
and(0,1,0).
and(1,1,1).
and(1,0,0).
or(0,0,0).
or(0,1,1).
or(1,0,1).
or(1,1,1).
xor(0,0,0).
xor(0,1,1).
xor(1,0,1).
xor(1,1,0).
not(0,1).
not(1,0).
halfadder(A,B,S,C):-
    xor(A,B,S),
    and(A,B,C).
halfsubtractor(A,B,Diff,Bo):-
    xor(A,B,Diff),
    not(A,X),
    and(B,X,Bo).
fulladder(A, B, Cin, Sum, Cout) :-
    halfadder(A, B, S1, C1),          
    halfadder(S1, Cin, Sum, C2),      
    or(C1, C2, Cout).
```

### Output:

![WhatsApp Image 2024-03-23 at 15 35 06_557eebba](https://github.com/snoopydj911/AI_Lab_2023-24/assets/122033587/4f1340d1-212b-45cb-9128-a1aaf3bf1d36)


### Result:
Thus the truth table of circuit verified sucessfully.

