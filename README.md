# quantum_numerov_method
solving Schrödinger equation with Numerov algorithm
The Numerov algorithm is a numerical method used to solve second-order ordinary differential equations, particularly those encountered in quantum mechanics. It approximates the wavefunction by iteratively calculating values at discrete positions.

Here's a step-by-step explanation of the code:

1-The code begins by importing the necessary libraries: numpy for numerical computations and array operations, matplotlib for plotting, and scipy.interpolate for spline interpolation.
The variables a, b, n, and h are defined to set up the range of positions (x) and the step size (h) for the calculation.

2-The numerov function is defined to perform the Numerov algorithm. It takes initial values y0 and y1, arrays of positions x, a function f(x) representing the potential energy, and the step size h as inputs. Inside the function, an initial array psiinitial is created and initialized with the initial values. Then, a loop iterates over the positions, applying the Numerov algorithm to calculate the wavefunction values at each position.

3-The normalize function is defined to normalize the wavefunction array. It takes the wavefunction array x as input, computes the normalization constant, and returns the normalized wavefunction.

4-The sawtoothpotential function is defined to calculate the sawtooth potential energy. It takes the amplitude a and the position array x as inputs and returns an array of potential energy values based on the sawtooth potential formula.

5-the main part of the code begins by initializing the parameters for the infinite square well case. The array psi is created to store the resulting wavefunction values. The initial values for the first two positions are set.

6-The energy eigenvalue E is initialized, and the squared wave vector k2 is defined based on the energy. The Numerov algorithm is then applied by calling the numerov function, passing the initial values, position array, wave vector, and step size. The resulting wavefunction is then normalized using the normalize function.

7-The endpoint value of the wavefunction psiend, step size of energy iteration dE, and tolerance for the wavefunction difference tol are set.

8-Two arrays, wavefunction1 and Earray, are created to store the wavefunctions and energy levels of the five lowest states.

9-The shooting method is implemented in a loop that runs five times. Within the loop, the energy E is iteratively adjusted, and the Numerov algorithm is applied to calculate the wavefunction psi1 for the current energy value. If the wavefunction at the endpoint changes sign, indicating the presence of an eigenstate, a refinement process is performed to improve the energy estimate. This refinement involves iteratively adjusting the energy values and recalculating the wavefunction until the wavefunction endpoint reaches a desired tolerance. The resulting wavefunction and energy level are stored in wavefunction1 and Earray, respectively.

10-The code then proceeds to plot the results using matplotlib. Subplots are created to display the energy levels and wavefunctions. The energy levels are plotted as horizontal lines, and the wavefunctions are plotted on separate subplots. The plot of all wavefunctions is also generated.

11-Finally, the plots are displayed using plt.show().

In summary, the code utilizes the Numerov algorithm to solve the Schrödinger equation for the infinite square well potential. It iteratively adjusts the energy values using the shooting method to find the eigenstates and corresponding energy levels. The resulting wavefunctions and energy levels are visualized through plots.
