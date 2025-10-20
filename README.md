# Solving The Rocket Equation: Optimal Fuel Expulsion for Maximum Altitude
### Author: Kareem Al Dahshan  
**Date:** October 20, 2025  

---

## 🧠 Overview
This project presents a **numerical and analytical study** of the one-dimensional rocket equation, including **gravity** and **quadratic aerodynamic drag**.  
It explores how the **fuel burn profile**, modeled by a shape parameter `n`, affects the rocket’s **maximum altitude**.

The analysis combines:
- Physical derivations from **momentum conservation**.
- **Nondimensionalization** of the governing equations.
- A full **numerical integration** using Python and SciPy.
- Plots and explanations illustrating how thrust timing changes performance.

---

## ⚙️ Model Summary

**Governing equation:**
\[
\frac{dv}{dt} = -g - \frac{b}{m}v|v| - v_g\frac{\dot m}{m}
\]

**Dimensionless form:**
\[
\frac{du}{d\tau} = -\gamma - \frac{u|u|}{m(\tau)} - \frac{1}{m(\tau)}\frac{dm}{d\tau}, 
\quad \gamma = \frac{gT_0}{v_g}
\]

**Fuel-burn model:**
\[
z(\tau) = 1 - 0.9\,\tau^n
\]
where:
- `n` controls the *shape* of the burn (timing of thrust),
- `n < 1` → front-loaded burn,
- `n > 1` → back-loaded burn.

---

## 📊 Key Results
- **Optimal burn-shape:** `n ≈ 0.5` (front-loaded)
- **Maximum altitude:** ≈ **23.7 km**
- For higher `n` values (back-loaded burns), performance drops due to increased drag losses.
- Gravity loss during a fixed burn is constant; optimization depends on minimizing drag.

---

## 🧩 Repository Contents
| File | Description |
|------|--------------|
| `Rocket_Equation_Final.ipynb` | Full executable Jupyter notebook with derivations, code, and plots. |
| `README.md` | Project summary, usage instructions, and results overview. |

---

## 🖥️ How to Run
1. **Install requirements:**
   ```bash
   pip install numpy scipy matplotlib
   ```
2. **Open the notebook:**
   - In **Jupyter Notebook**:  
     ```bash
     jupyter notebook Rocket_Equation_Final.ipynb
     ```
   - Or in **Google Colab**:  
     Upload the notebook file directly.

3. **Run all cells** to generate the plots and results.

---

## 📈 Interpretation
- Front-loaded burns (small `n`) produce higher altitudes by limiting time spent at high speeds in dense atmosphere.
- Back-loaded burns (large `n`) result in lower performance due to delayed thrust and higher integrated drag losses.

---

## 🧮 Future Extensions
- Include **altitude-dependent air density** for realistic drag.
- Explore **multi-stage rockets** or **variable exhaust velocity**.
- Compare with **experimental or open-source flight data**.

---

## 📚 Citation
If you refer to or build upon this work, please credit:  
**Kareem Al Dahshan, “Solving The Rocket Equation: Optimal Fuel Expulsion for Maximum Altitude,” 2025.**

---

## 🧾 License
This project is released for educational and research purposes under the **MIT License**.

---
