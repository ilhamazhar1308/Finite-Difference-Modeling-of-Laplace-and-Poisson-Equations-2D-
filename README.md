# Finite-Difference-Modeling-of-Laplace-and-Poisson-Equations-2D-

# 2D Laplace and Poisson Equation Solver for Geophysical Applications
This repository contains Python implementations of the **2D Laplace and Poisson equations**
solved using the **finite difference method**.  
The codes are developed for **educational purposes** to help students understand numerical
modeling of potential fields and heat transfer, with direct relevance to **geophysical
applications**.

---

## 📌 Purpose of This Project

This project is created to:

- Introduce **numerical solutions of partial differential equations (PDEs)**  
- Demonstrate the difference between **Laplace** and **Poisson** equations  
- Show how **boundary conditions and internal sources** affect physical fields  
- Provide a foundation for **geophysical modeling**, such as:
  - geothermal heat flow
  - gravity and magnetic potential fields
  - subsurface physical interpretation

The codes are intentionally kept **simple and transparent** so they can be used as
a **learning tool** in geophysics, physics, or engineering courses.

---

## 📘 Educational Objectives

By using this repository, users will learn:

- How to discretize 2D domains using a finite difference grid
- How iterative numerical schemes work (Jacobi-type iteration)
- The physical meaning of boundary-controlled vs source-controlled systems
- The role of Laplace and Poisson equations in real geophysical problems

---

## 🔢 Numerical Method

Both programs use the **Finite Difference Method (FDM)** with a regular 2D grid.

Each interior grid point is updated iteratively using neighboring values until a
steady-state solution is reached.

---

## 🔹 Laplace Equation

### Mathematical Form
\[
\nabla^2 T = 0
\]

### Physical Meaning
- No internal source or sink exists inside the domain
- The field is controlled **only by boundary conditions**
- Represents a **steady-state equilibrium system**

### Numerical Scheme
\[
T_{i,j} =
\frac{1}{4}
\left(
T_{i+1,j} + T_{i-1,j} + T_{i,j+1} + T_{i,j-1}
\right)
\]

### Interpretation
The temperature (or potential) at a point is the **average of its four neighboring points**.

---

## 🔹 Poisson Equation

### Mathematical Form
\[
\nabla^2 T = -S
\]

where:
- \( S \) is an **internal source term**

### Physical Meaning
- The system contains **internal heat generation or physical sources**
- Both boundary conditions and internal properties control the solution
- Produces **localized anomalies**

### Numerical Scheme
\[
T_{i,j} =
\frac{1}{4}
\left(
T_{i+1,j} + T_{i-1,j} + T_{i,j+1} + T_{i,j-1}
\right)
- \frac{h^2}{4} S
\]

---

## 🌍 Applications in Geophysics

### 1️⃣ Geothermal and Heat Flow Studies
- **Laplace**: steady heat conduction without internal heat sources  
- **Poisson**: geothermal reservoirs, magma chambers, or radioactive heat production  

Used to model:
- subsurface temperature distribution
- geothermal gradients
- heat transport in the Earth's crust

---

### 2️⃣ Gravity and Magnetic Modeling
The governing equation for gravitational potential is:

\[
\nabla^2 \Phi = -4\pi G \rho
\]

- **Laplace**: regions without mass anomalies (\( \rho = 0 \))
- **Poisson**: regions containing density contrasts (\( \rho \neq 0 \))

Applications:
- forward modeling of gravity anomalies
- interpretation of subsurface density structures
- foundation of gravity inversion methods

---

### 3️⃣ Electrical and Electromagnetic Methods
- **Laplace**: potential field without current sources
- **Poisson**: current injection in resistivity surveys

---

## 🧭 Why Laplace and Poisson Are Important in Geophysics

| Aspect | Laplace | Poisson |
|------|--------|--------|
| Internal source | No | Yes |
| Complexity | Simple | More realistic |
| Physical meaning | Boundary-controlled | Source-controlled |
| Use case | Baseline modeling | Anomaly modeling |

In practice:
- **Laplace equations represent idealized systems**
- **Poisson equations represent real Earth conditions**

---

## 📂 Repository Contents

- `Laplace_2D.py` — 2D Laplace heat transfer model
- `Poisson_2D.py` — 2D Poisson heat transfer model with internal source
- `Laplace.txt` — Output temperature field (Laplace)
- `Poisson.txt` — Output temperature field (Poisson)

---

## 🎓 Target Users

This repository is suitable for:
- Geophysics students
- Physics and engineering students
- Anyone learning numerical modeling of PDEs
- Beginners preparing for gravity, geothermal, or potential field modeling

---

## 🚀 Future Extensions

Possible future developments include:
- 3D modeling
- Gauss–Seidel or SOR schemes
- Error-based convergence criteria
- Application to gravity and magnetic inversion problems

---

## 👤 Author

**M. Ilham Azhar**  
Geophysics Student  
Numerical Modeling & Potential Field Methods

---

## 📜 License

This project is intended for **educational and academic use**.
