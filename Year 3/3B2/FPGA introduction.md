Inside an FPGA we have CLBs, configurable logic blocks, and inside these are LUTs.
LUTs (look up tables) contain the outputs for any combination of inputs.

For n inputs, we have $2^n$ elements in our look up table. The inputs just act as the address.
We often build it as a small SRAM (fast, rewritable, maintained value while power on) memory and a multiplexer tree to choose the output.

Digital design steps: State diagram -> state table -> K-map -> circuit implementation

De Morgan's theorem:
$\overline{AB} = \overline{A} + \overline{B}$
$\overline{A + B} = \overline{A}\,\overline{B}$

If there are $n$ variables there are $2^n$ minterms (m) and maxterms (M)
The sum of products (SOP) is made of minterms $(\overline{a}b\overline{c})$
The POS is made of maxterms $(a+b+\overline{c})$

There are some laws of Boolean algebra:
Commutative. Associative. Distributive: $a(b+c)=ab+ac$
Absorption: $a+ab = a$

Canonical form: All the binary variables appear once and only once in each term or factor.

If $f = \sum (m_7 + m_6 + m_2)$ then by finding $\overline{f}$ and performing De Morgan we find also $f = \prod M_0, M_1, M_3, M_4, M_5$

To find the POS, map the zeros in the K-map to find $\overline{f}$

Actual or potential circuit malfunction due to signals encountering delays. 
Static 0 hazard is when it goes 1 for a bit, static 1 is the opposite
Hazards cured by adding overlapping logic on the k-map

Verilog design and test software material: ModelSim / EDA playground
Verilog design units (Modules)
```verilog
module ANDg (
	input wire x1, x2,
	output wire f
);
	assign f = x1 & x2;
endmodule
```
Hierarchical modelling - model the low level components and build larger

```verilog
module light (
	input wire x1, x2,
	output wire f
);
	wire s1, s2, s3, s4;
	
	NOTg c1 (.x(x1), .f(s2));
	...
endmodule

// NOTg (inverter)
module NOTg (
	input wire x,
	output wire f
); 
	assign f = ~x;
endmodule
```

Structural modelling - described by interconnecting lower-level components
Behaviour modelling - a module is described by its input/output response

Within an always block, statements execute sequentially, however multiple always blocks execute concurrently
Register Transfer Level (RTL) - A type of behavioural modelling for the purpose of synthesis, where hardware is implied or inferred

Verilog data types:
* wire (net type, used for connections)
* reg (variable type for procedural assignment)
* integer (signed 32-bit)
* vectors: wire $[3:0]$ a; (MSB:LSB)
4 state logic:
* 1 - high
* 0 - low
* x - unknown
* z - high impedance (tri-state)

In Verilog, signals are declared inside the module and used to connect "always @(\*)" blocks and continuous assignments
```Verilog
reg [3:0] temp;
temp[3:2] = 2'b01;
```
The ordering of statements inside an always block affects simulation behaviour. Typically use blocking (=) or non-blocking (<=) assignments depending on modelling style
$[0:a]$ means ascending importance of bits, $[a:0]$ is descending

Continuous assignments in Verilog
1) Simple: assign f1 = x1 | x2
2) Ternary: assign f = s1 ? x1 : x2
3) Combinational logic in Verilog
```Verilog
always @(\*) begin
	case (sel)
		2'b00: f = x1;
		2'b01: f = x2;
		2'b10: f = x3;
		default: f = x4;
	endcase
end
```

Procedural blocks also execute concurrently at the module level
They are triggered by events specified in a sensitivity list
Local variables can be declared inside procedural blocks
Use blocking and non-blocking assignments

Inside the procedural blocks we have sequential statements, e.g. 
```Verilog
	if (s1)
		f = x1;
```

case statements are typically synthesised as parallel selection logic, particularly suitable for muxes and FSM decoding

Sum-of-products implementation of the 4-to-1 mux:
$f=\overline{s_1}\overline{s_0}I_0+\overline{s_1}s_0 I_1 + s_1 \overline{s_0}I_2+s_1s_0 I_3$
Generally, mux implementations of logic functions require that a given function be decomposed in terms of the variables that are used as the select inputs
Shannon's Expansion Theorem:
Any Boolean function $f(x_1,x_2,...,x_n)$ can be written in the form $f(x_1,x_2,...,x_n) = \overline{x_1}\cdot f(0,x_2,...,x_n) + x_1 \cdot f(1,x_2,...,x_n)$

A decoder has n inputs and $2^n$ outputs, asserting one depending on the input combination
When using decoders to build logic, it is easiest to express functions as a truth table or in canonical SOP form

ROM programming technologies -
EPROM - erasable read only memory (requires uv light to erase)
EEPROM - electrically EPROM

Gray code - successive decimal digits differ in exactly one bit

ROM implementation - 
A 4-line to 16-line decoder in a matrix with other variables
The row is the word and the column is the bit in the word (assuming a 32-bit architecture)

What is logic function were fixed (like TTL) but combined into a single device, and wiring connections could be programmed somehow?
Programmable array logic (PAL)

We can link a large programmable AND array to a fixed OR array.
ROM has it the other way around.

A PAL has programmable AND array, fixed OR array
A PLA had both programmable

### Sequential circuits

The output of a sequential circuit is a function of both present and past inputs, and is also called a finite state machine.
Modelled as a combinational circuit with a feedback memory

Bistable (flip-flop) circuits can store a single bit, registers store multiple bits
S-R bistable - $Q^+$ (after clock) $= S+\overline{R}Q$. $S=R=1$ is a forbidden state

J-K bistable uses a master slave set up to avoid $S=R=1$ problem, now toggles. The slave follows as the clock falls

We can write a D bistable as:
```Verilog
	always @(posedge Clk) begin
		Q <= D;
	end
```
We can combine these into parallel access shift registers, with modes to either load in parallel or by shifting.

Models for sequential circuits:
* Mealy network:
Output depends on input and current state. $Z = f(x,Q)$. $Q^+ = f(x,Q)$
All flip flops change state at the same time
* Moore network:
Output depends on current state. $Z = f(Q)$. $Q^+ = f(x,Q)$
When a set of inputs is applied, the resulting outputs do not appear until after the clock pulse causes the flip flops to change state

A synchronous circuit is a sequential circuit that uses a clock to synchronise all of the bistables operation.

We can make an FSM in Verilog with
```Verilog
	always @(posedge Clock) begin
		state <= next_state;
	end
	always @(*) begin
		case (state)
			...
		endcase
	end 
```

Sequential PAL - SPAL
Logic gates and registers after the programmable AND array, all fixed

Programmable logic device (PLD) - arrange multiple PAL arrays in a single device
This is followed by programmable macrocells where we can select the type of system (sequential or combinational), the type of output (active LOW or active HIGH) and the I/O (could be tri-state)

Complex PLD - CPLD 
Combine multiple PLDs (logic blocks) in a single device with programmable interconnect and I/O. Often referred to as a Logic Array Blocks (LAB)

CPLD architecture features: 
Programmable interconnect array (PI or PIA)
- Global routing connects any signal to any destination in device
- Programmed with EPROM or EEPROM
I/O control blocks:
* Separated from logic by PI
* Tri-state buffer control

