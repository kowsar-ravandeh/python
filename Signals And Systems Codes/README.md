t1: This code snippet demonstrates the convolution of a discrete-time input signal with a unit impulse response in Python using NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- Parameters: `z` is a decay factor, and `n` defines the range of discrete time indices from 0 to 19.
- Input Signal (`x[n]`): The input signal is defined as \( x[n] = z^n \cdot u[n] \), where \( u[n] \) is the unit step function, resulting in an exponentially decaying sequence.
- Impulse Response (`h[n]`): The impulse response is \( h[n] = u[n] \), represented as an array of ones, indicating a simple system.
- Convolution: The output response \( y[n] \) is computed by convolving the input signal \( x[n] \) with the impulse response \( h[n] \) using `np.convolve`.
- Plotting: Finally, the output response is visualized using a stem plot, showing how the output evolves over discrete time indices.
This effectively demonstrates how a discrete system responds to a given input signal.


t2: This code snippet illustrates the convolution of a rectangular input signal with an exponentially decaying impulse response in Python using NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- **Parameters**: 
  - `z` is a decay factor set to 0.5.
  - `n_x` and `n_h` define the ranges for the input signal \( x[n] \) and impulse response \( h[n] \) respectively.
- **Input Signal (`x[n]`)**: 
  - An array `x` of size 10 is initialized to zeros. The first 5 elements are set to 1, representing \( x[n] = 1 \) for \( 0 \leq n \leq 4 \).
- **Impulse Response (`h[n]`)**: 
  - An array `h` of size 10 is also initialized to zeros. The first 7 elements are populated with values of the form \( h[n] = z^n \), creating an exponentially decaying response for \( 0 \leq n \leq 6 \).
- **Convolution**: 
  - The output response \( y[n] \) is calculated by convolving the input signal \( x[n] \) with the impulse response \( h[n] \) using `np.convolve`.
- **Plotting**: 
  - The output response is visualized using a stem plot, with the x-axis representing the discrete time indices and the y-axis showing the output values.
This code effectively demonstrates how a rectangular input signal interacts with an exponentially decaying system response.


t3: This code snippet demonstrates the calculation of the output response of a continuous-time system in Python using NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- **Parameters**: 
  - `z` is set to 0.5, representing the decay factor.
  - `t` is a time array ranging from 0 to 10, with 1000 points for smooth plotting.
- **Input Signal (`x(t)`)**: 
  - The input signal is defined as \( x(t) = e^{-zt} \cdot u(t) \), where \( u(t) \) is the unit step function. This results in an exponentially decaying signal for \( t \geq 0 \).
- **Impulse Response (`h(t)`)**: 
  - The impulse response is defined as \( h(t) = u(t) \), which is a constant value of 1 for \( t \geq 0 \).
- **Output Response (`y(t)`)**: 
  - The output response is calculated as \( y(t) = \frac{1 - e^{-zt}}{z} \) for \( t \geq 0 \), which represents the system's response to the input signal.
- **Plotting**: 
  - The output response is visualized using a line plot, with the x-axis representing time and the y-axis showing the output values. The y-axis limits are set to enhance visibility.
This effectively demonstrates how a continuous-time system responds to a given input signal.


t4: This code snippet demonstrates the calculation of the output response of a continuous-time system with a rectangular input signal and a triangular impulse response in Python using NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- **Parameters**: 
  - `T` is set to 1, representing a time constant.
  - `t` is a time array ranging from 0 to \( 2T \) (0 to 2), with 1000 points for smooth plotting.
- **Input Signal (`x(t)`)**: 
  - The input signal is defined as \( x(t) = 1 \) for \( 0 < t < T \) and 0 otherwise, creating a rectangular pulse.
- **Impulse Response (`h(t)`)**: 
  - The impulse response is defined as \( h(t) = t \) for \( 0 < t < 2T \) and 0 otherwise, resulting in a triangular shape.
- **Output Response (`y(t)`)**: 
  - The output response is calculated using a loop:
    - For \( 0 < t < T \): \( y(t) = \frac{t^2}{2} \), representing the area under the input signal.
    - For \( T < t < 2T \): \( y(t) = t \cdot T - \frac{T^2}{2} \), which accounts for the effect of the input signal on the impulse response.
- **Plotting**: 
  - The output response is visualized using a line plot, with the x-axis representing time and the y-axis showing the output values. The y-axis limits are set for better visibility.
This effectively demonstrates how a continuous-time system responds to a rectangular input signal with a triangular impulse response.


t5: This code snippet illustrates the generation of a normalized weighted sum of sinusoidal functions in Python using NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- **Parameters**:
  - `t`: A time array ranging from 0 to 1, with 1000 points for smooth plotting.
  - `frequencies`: A list of frequencies for the sinusoidal functions (5 Hz, 10 Hz, and 15 Hz).
  - `weights`: A list of weights corresponding to each frequency, influencing their amplitude in the final pulse.
  - `phases`: A list of phase shifts for each sinusoidal function (0, \( \frac{\pi}{4} \), and \( \frac{\pi}{2} \)).
- **Pulse Generation**:
  - The pulse is generated as a weighted sum of sinusoidal functions using a generator expression. Each sinusoidal function is calculated using the formula:
    \[
    \text{pulse} = \sum (\text{weight} \cdot \sin(2 \pi \cdot \text{freq} \cdot t + \text{phase}))
    \]
- **Normalization**:
  - The generated pulse is normalized to fit within the range of 0 to 1. This is done by subtracting the minimum value and dividing by the range (max - min).
- **Plotting**:
  - The normalized pulse is visualized using a line plot. The x-axis represents time, and the y-axis shows the amplitude normalized between 0 and 1. The plot includes grid lines and a dashed line at y=0 for reference.
This effectively demonstrates how to create and visualize the combined effect of multiple sinusoidal functions with different weights and phases.


t6:This code snippet demonstrates the calculation of the output response of a continuous-time system with a rectangular input signal and a unit step response in Python using NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- **Parameters**: 
  - `T` is set to 1, representing a time constant.
  - `t` is a time array ranging from 0 to \( 3T \) (0 to 3), with 1000 points for smooth plotting.
- **Input Signal (`x(t)`)**: 
  - The input signal is defined as \( x(t) = 1 \) for \( 0 < t < T \) and 0 otherwise, creating a rectangular pulse.
- **Impulse Response (`h(t)`)**: 
  - The impulse response is defined as \( h(t) = 1 \) for \( 0 < t < 2T \) and 0 otherwise, representing a unit step function.
- **Output Response (`y(t)`)**: 
  - The output response is computed using a loop:
    - For \( 0 < t < T \): \( y(t) = t \), indicating a linear increase.
    - For \( T < t < 2T \): \( y(t) = T \), where the output remains constant.
- **Plotting**: 
  - The output response is visualized using a line plot, with the x-axis representing time and the y-axis showing the output values. The y-axis limits are set to enhance visibility and the x-axis limits are adjusted to cover the entire range of interest.
This effectively demonstrates how a continuous-time system responds to a rectangular input signal with a unit step response.


t7: This code snippet illustrates the simulation of a capacitor charging response in an RC (resistor-capacitor) circuit using Python with NumPy and Matplotlib. Here’s a brief explanation:
### Explanation:
- **Parameters**: 
  - `R` is the resistance, set to 1.0 ohm.
  - `C` is the capacitance, set to 1.0 farad.
  - `RC` is the time constant, calculated as the product of resistance and capacitance.
  - `T` is the duration of the pulse, set to 1.0 second.
  - `t` is a time array ranging from 0 to 5 seconds, with 1000 points for smooth plotting.
- **Input Signal (`x(t)`)**: 
  - The input signal is defined as \( x(t) = 1 \) for \( 0 < t < T \) (a rectangular pulse) and 0 otherwise.
- **Impulse Response (`h(t)`)**: 
  - The impulse response of the RC circuit is given by:
    \[
    h(t) = \frac{1}{RC} e^{-\frac{t}{RC}} \quad \text{for } t \geq 0
    \]
  - This represents the charging behavior of the capacitor.
- **Output Response (`y(t)`)**: 
  - The output response is calculated using convolution between the input signal and the impulse response:
    \[
    y(t) = x(t) * h(t)
    \]
  - The result is normalized by multiplying by the time step \( (t[1] - t[0]) \).
- **Time for Output Response**: 
  - A new time array `t_y` is created to match the length of the output response.
- **Plotting**: 
  - The output response \( y(t) \) is visualized using a line plot, with the x-axis representing time and the y-axis showing the output voltage across the capacitor. The limits of the axes are set for better visibility.
This effectively demonstrates how a capacitor charges over time in response to an input pulse in an RC circuit.


t8: This code snippet generates and visualizes a rectangular pulse function \( x(t) \) using Python with NumPy and Matplotlib. Here’s a brief explanation of the code:
### Explanation:
- **Parameter Definition**: 
  - `T1` is set to 1, representing the width of the rectangular pulse. You can modify this value to change the width of the pulse.
- **Time Array**: 
  - `t` is created as a linearly spaced array ranging from \(-2T1\) to \(2T1\) (from -2 to 2), consisting of 1000 points for smooth plotting.
- **Function Definition (`x(t)`)**: 
  - The function \( x(t) \) is defined as:
    \[
    x(t) = \begin{cases} 
    1 & \text{if } |t| < T1 \\ 
    0 & \text{otherwise} 
    \end{cases}
    \]
  - This results in a rectangular pulse with a height of 1, centered at zero, and a width of \(2T1\).
- **Plotting**: 
  - The pulse is plotted with the x-axis representing time \( t \) and the y-axis representing \( x(t) \).
  - The plot includes horizontal and vertical dashed lines at zero for reference, grid lines for better readability, and a shaded area under the curve to indicate the pulse.
- **Display**: 
  - The plot is displayed with appropriate labels, a title, and a legend.
This effectively demonstrates how to create and visualize a rectangular pulse function in Python.
