[https://github.com/hetsakariya0111-gi/CGxSU_Semester_1/blob/main/Semester_3/Digital%20Logic%20and%20Design/06_Logic%20Gates_and_Universal_Gates.md]

# Logic Gates: Quick Notes

`0` = LOW/OFF, `1` = HIGH/ON

## Gates

| Gate | Expression | Output is 1 when |
|---|---|---|
| AND | Y = AB | both inputs are 1 |
| OR | Y = A + B | at least one input is 1 |
| NOT | Y = A' | flips the input |
| NAND | Y = (AB)' | opposite of AND (0 only for 1,1) |
| NOR | Y = (A+B)' | opposite of OR (1 only for 0,0) |
| XOR | Y = A⊕B | inputs are different |
| XNOR | Y = (A⊕B)' | inputs are same |

## Truth Table

| A | B | AND | OR | NAND | NOR | XOR | XNOR |
|---|---|-----|----|------|-----|-----|------|
| 0 | 0 | 0 | 0 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 |

## Universal Gates

NAND and NOR are universal because NOT, AND and OR can all be made using only one of them. So any circuit can be built from just NAND or just NOR.

AND, OR and XOR are not universal: they can't make NOT.

## De Morgan's Law

```
(AB)'  = A' + B'
(A+B)' = A'B'
```

## NAND Only

```
NOT = NAND(A,A)                       1 gate
AND = NAND(A,B) -> NAND(x,x)          2 gates
OR  = NAND(A,A), NAND(B,B)
      -> NAND of both                 3 gates
```

## NOR Only

```
NOT = NOR(A,A)                        1 gate
OR  = NOR(A,B) -> NOR(x,x)            2 gates
AND = NOR(A,A), NOR(B,B)
      -> NOR of both                  3 gates
```

`x` = output of the first gate.

## Trick

- NAND: AND is easy (2 gates), OR is harder (3)
- NOR: OR is easy (2 gates), AND is harder (3)

## Tips

- Show algebra: ((AB)')' = AB
- Draw the truth table to prove
- `'` means NOT