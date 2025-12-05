# 🔄 Python Fixed-Point Iteration Solver

A custom **Numerical Root Finder** implemented in Python. This program solves for roots of an equation by rearranging it into the form $x = g(x)$ and applying the **Fixed-Point Iteration** method. It repeatedly applies the function to an initial guess until the value converges to a stable point.

## 🚀 Features

* **Transformation Function:** Currently configured to solve using $g(x) = \frac{2 - e^x + x^2}{3}$.
* **Step-by-Step Logging:** Prints a table showing the iteration number (**`n`**) and the calculated value (**`pn`**) at every step.
* **Convergence Check:** Stops when the difference between consecutive values is less than the tolerance (**`1e-2`**).
* **Safety Mechanism:** Includes a maximum iteration counter (**`N=10`**) to prevent infinite loops if the function diverges.

## 🛠️ Algorithm Specifications

The solver relies on the following parameters defined in the script:

| Category | Logic / Value |
| :--- | :--- |
| **Formula** | $p_{n+1} = g(p_n)$ |
| **Function `g(x)`** | `(2 - np.e**x + x**2) / 3` |
| **Tolerance (`TOL`)** | `1e-2` (0.01) |
| **Max Iterations (`N`)** | `10` |
| **Stop Condition** | When `abs(p - p0) <= TOL` |

## 📂 Project Structure

The project consists of a single Python script:

1.  **`Fixed-Point-Iteration.py`**: Contains the `g(x)` function definition and the iteration loop.

## 💻 How to Run

### 1. Install Dependencies
This project requires **NumPy**. If you don't have it, install it via pip:

```bash
pip install numpy
```
### 2. Run
Execute the python file in your terminal:
```text
Fixed-Point-Iteration.py
```

### 3. Input
The program will ask for a single initial guess (**`p0`**) to start the iteration process.
```text
Enter p0: 1
```

## 📝 Example Usage
### **Scenario 1** 
Finding the Fixed Point starting at 1.

#### Console Input:
```text
Enter p0: 1
```

#### Generated Output:
```text
n           pn
1     0.093906233529323 
2     0.369632840939599 
3     0.297014601131652 
4     0.318809224858852 
5     0.312604470929267 
Fixed-Point has converged
final p = 0.312604470929267
```

### Scenario 2 (No Convergence)
If the function does not stabilize within 10 steps:

```text
n        pn
 ...
10     1.543...
zero not found to the desired tolerance

```

* **Note:** The no. of steps can be changed.
  
## ⚠️ Requirements
* **Python 3.x**
* **NumPy Library** (import numpy)
