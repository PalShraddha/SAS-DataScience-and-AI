# SAS-DataScience-and-AI
optimization Concepts for Data Science and Artificial Intelligence.
#  Learning Mathematical Optimization with SAS

> A personal learning journal documenting my study of **Optimization Concepts for Data Science and Artificial Intelligence** — an official SAS Institute course (2023).

---

##  What is this?

This repository documents my journey through mathematical optimization using SAS — covering how to move beyond descriptive and predictive analytics into **prescriptive analytics**: not just understanding data, but using it to make optimal decisions.

The course is built around **PROC OPTMODEL**, SAS's powerful optimization procedure, and spans linear programming, nonlinear programming, integer programming, and Python integration with SAS Viya.

---

##  Course Structure

| Lesson | Topic | Key Concepts |
|--------|-------|--------------|
| 1 | Introduction to Mathematical Optimization | Objective function, decision variables, constraints, problem classification |
| 2 | Linear Programming (LP) | Simplex method, dual values, reduced costs, PROC OPTMODEL |
| 3 | Nonlinear Programming (NLP) | KKT conditions, gradient descent, Newton's method, local vs global optima |
| 4 | Integer & Mixed Integer LP (MILP) | Binary variables, branch & bound, LP relaxation |
| 5 | Open Source Interactivity | SAS Viya + Python, swat API, Jupyter integration |

---

##  Core Concepts

### The Analytics Hierarchy

```
┌─────────────────────────────────┐
│     PRESCRIPTIVE  ← We are here │  What should you do?
│        (Optimization)            │
├─────────────────────────────────┤
│         PREDICTIVE               │  What will happen?
│     (ML, Forecasting)            │
├─────────────────────────────────┤
│         DESCRIPTIVE              │  What happened?
│    (Reports, Dashboards)         │
└─────────────────────────────────┘
```

### The Generic Optimization Problem

```
minimize / maximize   f(x)
subject to            cᵢ(x)  ≤ / = / ≥  bᵢ    for i = 1, 2, ..., m
                      lⱼ ≤ xⱼ ≤ uⱼ              for j = 1, 2, ..., n

Where:
  x       = decision variables  (the choices you control)
  f(x)    = objective function  (what you optimize)
  cᵢ(x)  = constraint functions (the limits on your decisions)
  x*      = optimal solution    (best feasible objective value)
```

### Problem Type Classification

```
LP   → linear objective + linear constraints + continuous variables  → Easiest ✓
NLP  → nonlinear objective or constraints   + continuous variables  → Harder (starting point matters)
ILP  → linear objective + linear constraints + ALL integer variables → Harder (combinatorial)
MILP → linear objective + linear constraints + SOME integer vars    → Harder (most realistic)
```


##  Key Terminology

| Term | Definition |
|------|-----------|
| **Decision variable** | A quantity you control (e.g., units to produce, routes to use) |
| **Objective function** | The expression you minimize or maximize (profit, cost, distance) |
| **Constraint** | A restriction on the decision variables (resource limits, demand requirements) |
| **Feasible solution** | Any set of variable values that satisfies all constraints |
| **Optimal solution** | The feasible solution with the best objective value |
| **Dual value** | Rate of change of the objective per unit relaxation of a constraint (shadow price) |
| **Reduced cost** | How much an objective coefficient must change before a zero variable enters the basis |
| **LP relaxation** | Dropping integer constraints to get a solvable LP — gives a bound on the true IP optimal |
| **Branch & bound** | Algorithm for IP: branches on non-integer variables, prunes using LP bounds |
| **KKT conditions** | First-order optimality conditions for constrained NLP (generalize Lagrange multipliers) |

---

##  Why Optimization?

Formalizing a business problem as an optimization model provides:

- **Structure** — Know exactly how and why decisions are made
- **Consistency** — All decisions driven toward the same goals
- **Repeatability** — Same logic applied every run, no gut-feel variation
- **Adaptability** — Modify constraints without rebuilding from scratch
- **Persistence** — Model survives staff changes; not locked in someone's head
- **Scalability** — Handle thousands of variables with the same formulation

---

##  Tools Used

- **SAS PROC OPTMODEL** — Primary modeling and solving environment
- **SAS Viya** — Cloud-native analytics platform
- **Python (swat)** — SAS Scripting Wrapper for Analytics Transfer; connects Python to SAS Viya CAS
- **Jupyter Notebook** — Open-source interface for running SAS Viya Python workflows

---

## 📈 Progress

- [x] Lesson 1 — Introduction to Mathematical Optimization
- [x] Lesson 2 — Linear Programming
- [ ] Lesson 3 — Nonlinear Programming
- [ ] Lesson 4 — Integer & Mixed Integer Linear Programming
- [ ] Lesson 5 — Open Source Interactivity

---

## 📖 Reference

**Book:** *Optimization Concepts for Data Science and Artificial Intelligence — Slides and Notes*  
**Authors:** Robert Blanchard, Mark Hartmann, Chip Wells, Ari Zitin et al.  
**Publisher:** SAS Institute Inc., Cary, NC — © 2023  


---

## 🙋 About

This repo is part of my self-directed study in data science and operations research. I'm using it to build a solid foundation in prescriptive analytics before applying optimization to real-world problems.

Feel free to open an issue or discussion if you're studying the same material!


