Bayesian Signal Characterization (MCMC)
Team: shanmukhakumar
Members: BURUSU SHANMUKHA KUMAR, MOHAMMED SHAIK, SHARLI NELATURI
RUN INSTRUCTIONS
pip install numpy matplotlib
python mcmc_signal.py
OUTPUTS
Console: Prints MAP (Maximum A Posteriori) values for A, tau, and omega. Files: Generates 3 analysis images (trace_plots.png, posterior_histograms.png, fit_and_residuals.png).
PARAMETERS ESTIMATED

Parameter
Symbol
Physical Meaning
Amplitude
A
Signal growth scale
Turn-off Time
tau
Time where signal decay begins
Frequency
omega
Angular frequency of oscillation




THE MODEL
The code fits raw noisy data to this non-linear physical equation:
$$y(t) = A \cdot e^t \cdot [1 - \tanh(2(t - \tau))] \cdot \sin(\omega t)$$
WHAT YOU SEE
Trace Plots: 3 "fuzzy" lines showing the algorithm exploring the parameter space (convergence).
Histograms: Bell curves showing the probability/uncertainty for each parameter.
Fit & Residuals: Red line (Model) passing through black dots (Data). Blue dots (Residuals) scattered around zero.
SPECS
Algorithm: Metropolis-Hastings MCMC
Iterations: 20,000 steps
Likelihood: Gaussian with heteroscedastic noise (20% relative error)
Priors: Uniform (non-informative)
TESTED
Python: 3.11.9 (Windows)
Status: No additional setup needed


