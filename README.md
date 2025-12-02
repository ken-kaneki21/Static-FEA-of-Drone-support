# Structural Support Arm FEA (Fusion 360)

This project contains a static structural analysis of a curved aluminum support arm subjected to a 40 N downward load at the top face. The goal is to verify structural safety, quantify stresses and deflections, and estimate safety factor against yielding.

---

## 1. Objective

- Evaluate whether the support arm safely carries a 40 N load.
- Quantify:
  - Maximum Von Mises stress
  - Maximum displacement
  - Safety factor relative to aluminum yield strength

---

## 2. Geometry and Material

- Component: Curved support / landing arm modeled in Autodesk Fusion 360  
- Material: **Aluminum 6061**  
- Yield strength: ~276 MPa (Fusion 360 material library)

---

## 3. Boundary Conditions and Loads

- **Constraint:** bottom face fixed (all DOF).  
- **Load Case:**  
  - 40 N force applied on the **top face**, vertical downward  
  - Gravity enabled in the model

This loading represents a conservative worst-case tip/landing load on the arm.

---

## 4. Meshing and Solver

- Software: Autodesk Fusion 360 – Static Stress Study  
- Element type: parabolic solid elements  
- Mesh: automatic with refinement around curvature and fillet regions  
- Approx. element count: ~2500 elements (order of magnitude)

---

## 5. Results Summary

- **Max Von Mises stress:** ≈ 16 MPa  
- **Max displacement:** ≈ 0.5 mm at the loaded end  
- **Minimum safety factor:** ≈ 16.5 (based on yield strength 276 MPa)

### Interpretation

- Stresses are far below yield → arm remains safely elastic.  
- Displacement is small (< 1 mm) → stiffness is adequate for typical support/landing use.  
- Safety factor > 16 → strong margin; design could be light-weighted if needed.

---

## 6. Files in This Folder

Suggested structure:

```text
Structural_SupportArm_FEA/
│
├── Structural_load_report.pdf          # Original Fusion 360 study report
├── SupportArm_FEA_Short_Report.pdf     # Clean short report (optional)
├── screenshots/
│   ├── stress_vonmises.png
│   ├── displacement.png
│   └── safetyfactor.png
└── README.md                           # This file
