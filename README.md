# Smooth Izhikevich Model (SIZ)

The Izhikevich model is widely recognized for its ability to replicate the spiking behavior of biological neurons with computational efficiency. However, this new model introduces a smoothed approach to improve certain aspects of the original formulation, offering enhanced flexibility and applicability in specific scenarios.

To ensure reproducibility and provide a reference this repository includes two Colab notebooks:

- **IZ_Model**: A Python implementation of the Izhikevich model, based on the original  [MATLAB code](https://www.izhikevich.org/publications/figure1.m).
    
-  **SIZ_Model**: An implementation of the proposed "smooth" Izhikevich model.
    
Both notebooks are organized into three main sections:

1.  **Definitions**:  This section includes all necessary functions, parameters, and initial values required for the simulations.
    
2.  **Run**: Here, the models are solved, and the results are plotted for each neuron type using default parameter values.
    
3.  **Sheet**:  This section provides a comprehensive graphical summary (sheet) of all neuron types simulated in the model.
    
For consistency and comparability, the integration step size (`tau`) is set to  **0.1**  in both models. However, it’s worth noting that in the original Izhikevich MATLAB code, the step size varies depending on the neuron type being simulated.

To solve the system of equations for the new model, we used the **Dormand-Prince method**, an explicit 5th-order Runge-Kutta method, known as `'dopri5'` in the `ode` integrator of the [SciPy](https://docs.scipy.org/doc/scipy/reference/generated/scipy.integrate.ode.html#ode) library. 

If you wish to experiment with custom parameters in the  SIZ_Model, you can modify and rerun the **pipeline functions**, at the bottom definition section, to explore different configurations.
