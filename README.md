# PowerAmplifier_2.4GHz
The design of a 2.4GHz amplifier for RF use, optimized for efficiency.

## Biasing
The CG2H40010 transistor used for the amplifier is biased with a drain voltage of 28V as required by the specification. Since we are looking to optimize for efficiency, the gate voltage  is set as low as possible. We set the gate voltage to -2.85V, which results in a simulated drain-source current of 73.35mA. Gate voltage could probably be set even lower, but specification doesn't allow drain-source current of less than 50mA, so we wanted to maintain a margin.

| **Category**                     | **Specification**                                           | **Simulated**       | **Measured**        |
|----------------------------------|-------------------------------------------------------------|---------------------|---------------------|
| **General operating conditions** |                                                             |                     |                     |
| Frequency of operation           | 2.4 GHz                                                     | 2.4 GHz             | 2.28 GHz            |
| Drain voltage \( V_D \)          | 28 V                                                        | 28 V                | 28 V                |
| Drain current \( I_D \)          | ≥ 50 mA                                                     | 73.35 mA            | 66 mA               |
| **Small-signal specifications at operating frequency** |                                         |                     |                     |
| Unconditional stability          | mu > 1  for all frequencies of interest               | True                | Conditionally stable|
| Small-signal bandwidth           | ≥ 100 MHz within 1 dB                                       | 248.021 MHz         | 253.655 MHz         |
| Gain \( S_{21} \)                | ≥ 14 dB within bandwidth                                    | 15.7 dB             | 16.38 dB            |
| **Large-signal specifications**  |                                                             |                     |                     |
| Output power \( P_{out} \)       | ≥ 39 dBm for \( P_{in} = 27 dBm \)                         | 39.68 dBm           | 40.12 dBm           |
| Two-tone test                    | \( P_{out,peak} = 38 dBm \), IMD minimized, tone spacing 5 MHz | True             | True                |
| Power added efficiency            | Maximize for single-tone input                              | 50.44 %             | 58.67 %             |

