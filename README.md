# Finite-Difference-Modeling-of-Laplace-and-Poisson-Equations-2D-

# 2D Laplace and Poisson Equation Modeling for Geophysical Applications

This repository contains Python programs for solving the **2D Laplace and Poisson equations**
using the **finite difference method**.  
The codes are designed for **educational purposes**, especially for students learning
numerical modeling and its applications in **geophysics**.

---

## Purpose of This Repository

This project was created to:

- Help students understand **numerical solutions of partial differential equations (PDEs)**
- Demonstrate the difference between **Laplace** and **Poisson** equations
- Show how **boundary conditions** and **internal sources** affect physical fields
- Provide a basic foundation for **geophysical modeling**, such as:
  - geothermal heat transfer
  - gravity and magnetic potential fields
  - subsurface physical interpretation

The programs are intentionally written in a **simple and clear form** to support learning
and experimentation.

---

## Educational Goals

By studying and running these codes, users will learn:

- How a 2D physical domain is discretized into a numerical grid
- How iterative finite difference schemes work
- The physical meaning of equilibrium systems
- Why internal sources create anomalies in geophysical fields

---

## Numerical Method Used

Both models use the **Finite Difference Method (FDM)** with an iterative approach.

Each interior grid point is updated using the values of its four neighboring points
until the solution reaches a steady state.

---

## Laplace Equation

### Governing Equation

Laplace equation (2D):

    ∇²T = 0

### Physical Meaning

- There is **no internal source or sink** inside the domain
- The field is controlled **only by boundary conditions**
- Represents a **steady-state equilibrium system**

### Numerical Interpretation

At each grid point, the temperature (or potential) is computed as the **average of its
four neighboring points**.

Laplace equation is commonly used as a **baseline or reference model**.

---

## Poisson Equation

### Governing Equation

Poisson equation (2D):

    ∇²T = −S

where:

- S is an **internal source term**

### Physical Meaning

- The domain contains **internal heat generation or physical sources**
- The solution is influenced by **both boundary conditions and internal properties**
- Produces **localized anomalies** in the field

Poisson equation represents **more realistic Earth conditions**.

---

## Applications in Geophysics

### 1️ Geothermal and Heat Transfer Modeling

- **Laplace equation**
  - Steady-state heat conduction
  - No internal heat production
  - Useful for background thermal modeling

- **Poisson equation**
  - Geothermal reservoirs
  - Magma bodies
  - Radiogenic heat sources

Used to model:
- subsurface temperature distribution
- geothermal gradients
- heat flow in the Earth's crust

---

### 2️⃣ Gravity and Magnetic Methods

In gravity modeling, the governing equation is:

    ∇²Φ = −4πGρ

- Laplace equation applies when density contrast is zero
- Poisson equation applies when density contrast exists

Applications include:
- forward modeling of gravity anomalies
- interpretation of subsurface density structures
- foundation of gravity inversion techniques

---

### 3️⃣ Electrical and Electromagnetic Methods

- Laplace equation: potential field without current sources
- Poisson equation: current injection in resistivity surveys

---

## Role of Laplace and Poisson in Geophysics

| Aspect | Laplace | Poisson |
|------|--------|--------|
| Internal source | No | Yes |
| Physical realism | Idealized | Realistic |
| Field behavior | Smooth | Anomalous |
| Typical use | Baseline modeling | Target interpretation |

In real geophysical studies:
- **Laplace equation represents ideal conditions**
- **Poisson equation represents real subsurface conditions**

---

## Repository Contents

- `Laplace_2D.py`  
  2D heat transfer modeling using Laplace equation

- `Poisson_2D.py`  
  2D heat transfer modeling using Poisson equation with internal source

- `Laplace.txt`  
  Output temperature field from Laplace model

- `Poisson.txt`  
  Output temperature field from Poisson model

---

## Intended Users

This repository is suitable for:

- Geophysics students
- Physics and engineering students
- Beginners in numerical modeling
- Anyone learning potential field methods

---

## Possible Future Development

- Extension to 3D modeling
- Gauss–Seidel or SOR iteration schemes
- Error-based convergence criteria
- Application to gravity and magnetic inversion problems

---

## Author

**Ilham Azhar**  
Geophysics Engineering Student  | Sumatera Institute of Technology (ITERA) 

Numerical Modeling and Potential Field Methods

---

## 📜 License

This project is intended for **educational and academic use**.

