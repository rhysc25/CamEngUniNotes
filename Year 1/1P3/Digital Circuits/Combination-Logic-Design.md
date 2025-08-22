# Combination Logic Design

Combinational logic circuits do not have an internal stored state, the output is a function of the current inputs.
$L=\bar{T}.\bar{W}.\bar{P}=\overline{(T+W+P)}$

We want to simplify logic expressions, to use fewer gates.
Can either use Boolean algebra or Karnaugh maps.

For Boolean algebra: Commutation is the same. Association is the same.
![Boolean Algebra Rules](Bool.png)

Things to remember:
$A+0=A$
$A+A=A$
$A.A=A$
$A.\overline{A}=0$

AND takes precedence over OR: $A.B+C.D=(A.B)+(C.D).$

Every Boolean law has a dual: Any statement is also valid with:
. replaced by +, + replaced by ., 0 replaced by 1, 1 replaced by 0. These must all be done at once.

A useful technique to simplify Boolean expressions is to expand each term until it includes one instance of each variable, or its compliment.
$A=A.(B+\overline{B})=AB+A\overline{B}$.

De Morgan's theorem (in data book):
$\overline{A+B+C}=\overline{A}.\overline{B}.\overline{C}$
$A.B.C=\overline{\overline{A}+\overline{B}+\overline{C}}$

We can prove these by subbing in different values of A and B for the two variable case, and the rest is proved by induction, if we for example consider B+C to be one variable.

De Morgan's theorem is used extensively to convert a circuit purely into NAND gates, remembering that a NAND gate with a tied input is essentially an inverter. This will give the sum of products (SOP) representation.

If we want to build a circuit using only NOR gates, we must first rewrite the expression for the opposite case, only at the end adding a bar on top. This will give the product of sums (POS) representation. Remember that a NOR gate with the inputs tied is essentially an inverter as well.

## VHDL
VHDL (Very high speed integrated circuits hardware description language). It is used to describe complex circuits.

First we have an interface, where we describe the inputs and outputs of out component.
Them we have the architectural specification where we describe how the output is related to the input, e.g. Y <= not (A and B); for a NAND gate.

Once these entities are made, we can create an entity that is our circuit, stating the ports in the interface, the whole circuit input and outputs.
For the architecture, state the signals, the intermediate signals between chips.
Then provide port maps for each entity in the architecture.

## Karnaugh Maps
Karnaugh maps are good for a maximum of 5 variables.
The first variable is high for the last 2 columns. The next variable is high for the middle 2 columns. The next variable is high for the bottom 2 rows. The last variable is high for the middle two rows.

It is very easy to fill in the table, for which cells are 1 and which aren't. If all cells are 1 then the output is 1.

A 4 variable expression creates a 1X1 cell of 1s.
A 3 variable expression creates a 1X2 block of 1s.
A 2 variable expression creates a 2X2 block or a 1X4 block of 1s.
A 1 variable expression creates a 2X4 block of 1s.

Important: Karnaugh maps, and the blocks within them, wrap round top-bottom and side-to-side, like the snake game.

For making NAND circuits, use the Karnaugh map normally.
For making NOR circuits, do what is easiest. A lot of the time is it easier to find $\bar{Y}$ by finding expressions for the zeroes, the inverting it.

## Don't Care States
Don't care state: A don't care state is an output for a combination of inputs that do not matter, or can never happen.
We represent this as an X on are Karnaugh map, and can be either a 1 or 0, whichever makes determining the blocks of 1s easier.

## Hazards
Hazards: When a signal undergoes a momentary transition when it is supposed to remain unchanged.
![Hazards](Hazards.png)

Removing hazards:
To fix a static 1-hazard, ensure all the sum-of-products terms overlap. This may involve introducing a new component.
To fix a static 0-hazard, draw the Karnaugh map of the inverse of the output concerned, and ensure all the sum-of-products terms are overlapping.

## Shaft Encoder
A shaft encoder is a wheel that rotates, with black sections representing 1s and white sections representing 0s. There may be a problem if there is a large change between sections, and there is overlap between the outputs.
To minimise this, we need to ensure that there is only a change of 1 bit between each section.
This is called unit distance code.

## Binary Basics
A binary digit is a bit, 8 bits is a byte.
The 8th bit is the most significant bit, and the 1st is the least significant bit.
8 bits can store $(2^8-1)=255$ different values.

To convert decimal into binary, divide by 2 over and over again, writing down the remainder each time. The binary number is these remainders read upwards.

Octal is base 8 and hexadecimal is base 16.
In hex, 11 is A, 12 is B, ..., 15 is F.
Hex can be labelled by $2E_H$,$2E_{16}$, $\$59$ or $0X59$ for PIC processors.
If we split a binary number into two sets of four then evaluate each set, we get the hexadecimal equivalent.

## Two's Complement
2s complement: 00000000 to 0111111 is 0 to 127, then 1000000 to 11111111 is -128 to -1.
To convert from positive to negative or negative to positive, we flip the signs of all bits, and add 1.
This is very handy as is means that any number with a MSB of 0 is positive, and any number with a MSB of 1 is negative.

## Binary Addition
Binary addition:
0 + 0 = 0, 0 + 1 = 1, 1 + 1 = 0, carrying the 1.

For unsigned numbers, there is an overflow when a bit is carried outside of the byte.
For signed numbers it is more complex, as we are ignoring the carried bit to define our numbers.
For an unsigned bit:
There is an overflow error when the carry into the MSB is not the same as the carry out.
For example, a 1 may be carried out of the MSB, but nothing is carried in, indicating an overflow error.

We could represent signed numbers by having a bit for the sign and the other 7 represent the magnitude, but this leads to there being 2 zeroes, and we would need separate circuits for addition and subtraction.

## Binary Coded Decimal
Binary coded decimal is where each group of 4-bits encodes a number.

## Alphanumeric Character Codes
Alphanumeric character codes use bits to represent characters, and is largely standardised, apart from what the 8th bit encodes, which varies for machine and purpose.
