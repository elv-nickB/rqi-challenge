# Rayleigh Quotient Iteration – Interview Exercise

## Overview
This exercise evaluates numerical intuition, the ability to learn and explain a mathematical method, and practical software skills. You will study the Rayleigh Quotient Iteration (RQI) method for computing an eigenpair, explain it clearly, and then implement a small web service that exposes the solver over HTTP.

## Instructions
You are free to consult online resources or use LLMs to help understand concepts and to reference documentation. You cannot use LLMs to implement entire functions or scaffold your code. Please ask if you are not sure.

You may tackle the following parts in any order. The goal is to go as wide as possible in these three areas rather than fixate on one of them - if you are stuck it's better to move on and come back. 

---

## Part 1 — Conceptual Understanding
Learn the **Rayleigh Quotient Iteration** method and then explain it in plain english, focusing firstly on intuition for why the method works and secondly on achieving a rigorous understanding.

Please write-up a summary of your learnings wherever is convenient

---

## Part 2 — Implement the Algorithm
Implement RQI for **real symmetric matrices**:

- **Input:** matrix \( A \in \mathbb{R}^{n \times n} \)
- **Output:** an approximate eigenvalue and a normalized eigenvector
- Use double precision.
- Use a reasonable convergence criterion (e.g., residual norm or eigenvalue change).
- You may use standard linear algebra routines (e.g., LU/Cholesky) but should implement the iteration logic yourself.

---

## Part 3 — Build the Web Service

Expose a single endpoint:

### `POST /eigenpair`

**Response**
```json
{
  "eigenvalue": <float>,
  "eigenvector": [ ... normalized vector ... ]
}
