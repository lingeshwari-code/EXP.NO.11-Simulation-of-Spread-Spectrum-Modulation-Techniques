# EXP.NO.11-Simulation-of-Spread-Spectrum-Modulation-Techniques

11.Simulation of Spread Spectrum Modulation Techniques

# AIM
```
To simulate and analyze spread spectrum modulation techniques using Python by generating original data, performing modulation/demodulation, and spreading the signal.
```

# SOFTWARE REQUIRED
```
->Python 3.x

->Libraries: NumPy, Matplotlib
```

# ALGORITHMS
```
1.Generate Original Data

Generate a random sequence of binary data (0s and 1s).

2.Demodulation

Perform simple cumulative sum to simulate basic demodulation behavior.

3.Spread Spectrum Technique

Map 0 to -1 and 1 to +1.

Multiply each symbol with a random sequence of {-1, +1} to spread the signal.

4.Plot the Signals

Plot the Original Data.

Plot the Demodulated Signal.

Plot the Spread Signal.
```

# PROGRAM
```
import numpy as np
import matplotlib.pyplot as plt

# Use a different random seed and signal length
np.random.seed(42)
signal_length = 800

# Generate random binary data
binary_data = np.random.randint(0, 2, signal_length)

# Simulate demodulation using cumulative sum
demod_output = np.cumsum(binary_data)

# Perform spreading: 0 → -1, 1 → 1, with random polarity
modulated_data = 2 * binary_data - 1
spreaded_output = modulated_data * np.random.choice([-1, 1], size=signal_length)

# Plotting
fig, axs = plt.subplots(3, 1, figsize=(12, 6))

axs[0].plot(binary_data, color='green')
axs[0].set_title('Input Binary Data')

axs[1].plot(demod_output, color='red')
axs[1].set_title('Simulated Demodulated Output')

axs[2].plot(spreaded_output, color='purple')
axs[2].set_title('Randomly Spread Signal')

plt.tight_layout()
plt.show()
```

# OUTPUT
![image](https://github.com/user-attachments/assets/e51fd5f7-15d7-4c33-ac72-f4908d4c1c38)
# RESULT / CONCLUSIONS
```
Successfully simulated a simple spread spectrum modulation technique.

Observed the randomization effect on the original data through the spread signal.

Learned how spreading a signal increases its bandwidth and provides robustness against interference.
```
