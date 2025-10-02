# PowerAmplifier_2.4GHz
The design of a 2.4GHz amplifier for RF use, optimized for efficiency.

##Biasing
The CG2H40010 transistor used for the amplifier is biased with a drain voltage of 28V as required by the specification. Since we are looking to optimize for efficiency, the gate voltage  is set as low as possible. We set the gate voltage to -2.85V, which results in a simulated drain-source current of 73.35mA. Gate voltage could probably be set even lower, but specification doesn't allow drain-source current of less than 50mA, so we wanted to maintain a margin.
