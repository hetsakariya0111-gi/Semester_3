[https://github.com/hetsakariya0111-gi/CGxSU_Semester_1/blob/main/Semester_3/Digital%20Logic%20and%20Design/06_Logic%20Gates_and_Universal_Gates.md]

LOGIC GATES: QUICK NOTES >
************************

0 = LOW/OFF, 1 = HIGH/ON

GATES >
*****

AND   Y = AB        1 only if both inputs are 1
OR    Y = A + B     1 if at least one input is 1
NOT   Y = A'        flips the input
NAND  Y = (AB)'     opposite of AND (0 only for 1,1)
NOR   Y = (A+B)'    opposite of OR (1 only for 0,0)
XOR   Y = A⊕B       1 if inputs are different
XNOR  Y = (A⊕B)'    1 if inputs are same

TRUTH TABLE (A B) >
*****************

A B | AND OR NAND NOR XOR XNOR
0 0 |  0   0   1    1   0   1
0 1 |  0   1   1    0   1   0
1 0 |  0   1   1    0   1   0
1 1 |  1   1   0    0   0   1

UNIVERSAL GATES >
***************

NAND and NOR are universal because NOT, AND and OR
can all be made using only one of them.
So any circuit can be built from just NAND or just NOR.
(AND, OR, XOR are not universal: no way to make NOT.)

DE MORGAN'S LAW (used in conversions) >
*************************************

(AB)' = A' + B'
(A+B)' = A'B'

NAND ONLY >
*********

NOT = NAND(A,A)                    1 gate
AND = NAND(A,B) → NAND(x,x)        2 gates
OR  = NAND(A,A), NAND(B,B)
      → NAND of both               3 gates

NOR ONLY >
********
NOT = NOR(A,A)                     1 gate
OR  = NOR(A,B) → NOR(x,x)          2 gates
AND = NOR(A,A), NOR(B,B)
      → NOR of both                3 gates

TRICK >
*****

NAND: AND is easy (2), OR is harder (3)
NOR:  OR is easy (2), AND is harder (3)

TIPS >
****

- Show algebra: ((AB)')' = AB
- Draw truth table to prove
- ' means NOT