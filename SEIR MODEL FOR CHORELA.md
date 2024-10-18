
```python
import numpy as np
from scipy.integrate import odeint
import matplotlib.pyplot as plt

# Parameters
# given the basic reproduction rate of cholera lies between 2 to 4 (CDC, 2022), (Montero et al., 2023) (Kigen et al., 2020).
# on average R0 = 3
# Therefore, Beta = R0*gamma
beta = 3*1/7 # Transmission rate
sigma = 1/5  # Rate of exposed to infectious (1/incubation period)
gamma = 1/7  # Recovery rate

# Initial conditions
S0 = 207972  # Susceptible
E0 = 78      # Exposed
I0 = 25      # Infected
R0 = 24      # Recovered
N = S0 + E0 + I0 + R0  # Total population

# Time points (days)
t = np.linspace(0, 160, 160)  # 0 to 160 days

# SEIR model differential equations
def deriv(y, t, N, beta, sigma, gamma):
    S, E, I, R = y
    dSdt = -beta * S * I / N
    dEdt = beta * S * I / N - sigma * E
    dIdt = sigma * E - gamma * I
    dRdt = gamma * I
    return dSdt, dEdt, dIdt, dRdt

# Initial conditions vector
y0 = S0, E0, I0, R0

# Integrate the SEIR equations over the time grid
ret = odeint(deriv, y0, t, args=(N, beta, sigma, gamma))
S, E, I, R = ret.T

# Plot results
plt.figure(figsize=(10, 6))
plt.plot(t, S, 'b', label='Susceptible')
plt.plot(t, E, 'orange', label='Exposed')
plt.plot(t, I, 'r', label='Infected')
plt.plot(t, R, 'g', label='Recovered')
plt.xlabel('Time (days)')
plt.ylabel('Population')
plt.title('SEIR Model Simulation')
plt.legend()
plt.grid()
plt.show()

```


    
![png](output_2_0.png)
    



```python

```
