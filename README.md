# Rayleigh Quotient Iteration – Interview Exercise

## Overview
This exercise evaluates numerical intuition, the ability to learn and explain a mathematical method, and practical software skills. You will study the Rayleigh Quotient Iteration (RQI) method for computing an eigenpair, explain it clearly in a short writeup, and then implement a small web service that exposes the solver over HTTP.

## Instructions
You are free to consult online resources or use LLMs to help understand concepts or to reference library documentation. Do not query for full implementations of an RQI solver (psuedocode ok).

You may tackle the following parts in any order. The goal is to go as wide as possible in these three areas rather than fixate on one of them - if you are stuck it's better to move on and come back. 

---

## Part 1 — Conceptual Understanding
Learn the **Rayleigh Quotient Iteration** method and then explain it in plain english, focusing primarily on intuition not full rigor. 

Please write a high level summary of the method in the provided `writeup.md` file. You can also use a latex editor if you are more comfortable with that

You're encouraged to learn this topic using whatever method you are most comfortable with, but the provided document is a useful reference, especially the three algorithm sections 27.1, 27.2, and 27.3 and surrounding discussion: [reference here](https://www.cs.cmu.edu/afs/cs/academic/class/15859n-f16/Handouts/TrefethenBau/RayleighQuotient-27.pdf)

---

## Part 2 — Implement the Algorithm
Implement RQI for **real symmetric matrices**:

- **Input:** matrix A
- **Output:** an approximate eigenvalue and a normalized eigenvector
- Use a reasonable convergence criterion
- You may use standard linear algebra routines from common libraries (i.e matvec/matmul/linear-system-solvers), but you must implement the core logic

---

## Part 3 — Build the Web Service

Expose a single endpoint:

### `POST /eigenpair`

**Request**
Should contain the input matrix. The exact structure is left for you to consider.

**Response**
```json
{
  "eigenvalue": <float>,
  "eigenvector": [ ... normalized vector ... ]
}
```