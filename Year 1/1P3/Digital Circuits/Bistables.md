A bistable is a circuit with 2 states, which can be set and reset. 

Set Reset Bistable
![[Pasted image 20250501135632.png]]

When S is made HIGH, Q1 is HIGH, even if we turn S to LOW again. 
It can only be reset if R is made HIGH. Ensure both S and R are not HIGH at the same time, as this is a forbidden state.

$Q1 = S + \overline{Q2}$
$Q2 = R + \overline{Q1}$

We can use this for things like debouncing, when we don't want the variation in one variable to effect the output.

Gated SR Bistable
![[Pasted image 20250501140139.png]]

The gate is connected to a clock, CLK, which switches between HIGH and LOW at regular intervals, allowing the outputs to occur at specific times.

A change only occurs, e.g. to SET (Q1 = 1), when the gate is HIGH. It is only set when both S and G are HIGH.

Master Slave Bistable
![[Pasted image 20250501140429.png]]

2 SR bistables connected. The slave bistable is controlled by the master bistable. 

When $G_{master}$ is HIGH, then the master bistable is sensitive to input signals and the slave isn't. The opposite is true when it is LOW.

The inputs to the slave are the outputs from the master.

![[Pasted image 20250501140807.png]]

This is the symbol for the master slave arrangement.

Asynchronous inputs are ones which are not dependant on the CLK signal.

![[Pasted image 20250501140923.png]]

A D-type (delay/data) Latch

![[Pasted image 20250501141105.png]]

SET if D is HIGH once the clock arrives. RESET if it is LOW.

JK Bistable

![[Pasted image 20250501141315.png]]

The AND gates at the inputs prevent the problem of S = R = 1. J = K = 1 is actually a very useful input, toggling the state of the output.

![[Pasted image 20250501141530.png]]
![[Pasted image 20250501141544.png]]

This is the characteristic table of outputs of a JK bistable (in the databook).

![[Pasted image 20250502164627.png]]

Both J and K are constantly connected to 1, so toggle every time the clock goes HIGH (positively edge triggered). This halves the frequency of the clock.

![[Pasted image 20250502164814.png]]

The most significant bit is QA and the least is QD. When read in that order it counts the number of cycles of QD.

However, due to the propagation delay (the small amount of time taken for the bistable to change its state based on the inputs when the clock goes to HIGH), there are momentary glitches/ anomalous readings.

To fix this, we need to give them all a common clock, creating a synchronous counter.

A shift register uses a string of D-type latches. Data is only onto the next latch when the clock arrives. Therefore you can retrieve data from a stream of bits.

A parallel loading bistable is the opposite, where given 4 streams of bits, they are combined into one using D-type latches.
A parallel loading shift register is used to send one data bit at a time across the serial link, so less wires needed.

![[Pasted image 20250502170811.png]]

This is a Johnson counter, which uses a shift register of length N to produce a sequence of length 2N.

![[Pasted image 20250502170909.png]]

If we want to divide by 5 we use this. If the MSB and LSB are 1, therefore 101, then the counting resets. we can make this synchronous by adding additional circuits and using a common clock.

