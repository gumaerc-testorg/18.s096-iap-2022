---
content_type: page
description: This page includes lecture notes and readings for each lecture.
draft: false
title: Lecture Notes and Readings
uid: d37b3aa2-ff0c-4286-b7ce-b7e4f3fbb2ea
---
## Lecture 1

### Lecture Notes

- Part 1: {{% resource_link "563ca6c0-9f9e-4974-8994-6ad8ce50438d" "Introduction (PDF)" %}}
- Part 2: Derivatives as Linear Operators \[notes not available\]

### Further Readings:

- {{% resource_link "7fb09805-6dae-4885-9ae5-a15a137eeeac" "matrixcalculus.org" %}} is a fun site to play with derivatives of matrix and vector functions. 
- {{% resource_link "74f87569-1e0d-48a8-aa40-76b813d43208" "*The Matrix Cookbook* (PDF)" %}} has a lot of formulas for these derivatives, but no derivations.
- Notes on {{% resource_link "521ba65d-d48f-44cc-9e5e-04b07df19b36" "Vector and Matrix Differentiation (PDF)" %}} are helpful.
- **Fancier math**: The perspective of derivatives as linear operators is sometimes called a {{% resource_link "cf2d8ed6-fba9-4bdc-a7f4-0c9b0d37eefb" "Fréchet derivative" %}} and you can find lots of very abstract (what I'm calling "fancy") presentations of this online, chock full of weird terminology whose purpose is basically to generalize the concept to weird types of vector spaces. The "little-o notation" o(δx) we're using here for "infinitesimal asymptotics" is closely related to the {{% resource_link "1aeee1d0-76c1-415d-b6f5-74bd951fb510" "Big *O* notation" %}} used in computer science, but in computer science people are typically taking the limit as the argument (often called "n") becomes very *large* instead of very small. A fancy name for a row vector is a "covector" or {{% resource_link "73e184c8-2d5c-4c28-8fb7-f75dc644164f" "linear form" %}}, and the fancy version of the relationship between row and column vectors is the {{% resource_link "aaae0ea3-f992-42fe-9137-27d102553d3f" "Riesz representation theorem" %}}, but until you get to non-Euclidean geometry you may be happier thinking of a row vector as the transpose of a column vector.

## Lecture 2

### Lecture Notes

- Part 1: Derivatives as Linear Operators (cont.) \[notes not available\]
- Part 2: {{% resource_link "fae7bc16-3dc6-42c3-9e16-8babd952dd58" "Two by Two Matrix Jacobians (html)" %}} ({{% resource_link "5f00501e-fb3c-48f9-a50d-d0c93bb377dc" "download the zip file" %}}) ({{% resource_link "f8969b88-aa7d-4225-9642-3bb4dcdfa89b" "pluto notebook source code" %}}) ({{% resource_link "0c0bb241-5d3f-4acb-a96d-6630947a841d" "download the source code zip file" %}})

### Further Readings:

- The terms "forward-mode" and "reverse-mode" differentiation are most prevalent in {{% resource_link "a74974a1-5cfa-4dd4-9b91-703c5a7b0536" "automatic differentiation" %}} (AD), which we will cover later in this course. 
- You can find many, many articles online about {{% resource_link "f6c9e676-7d4b-4d6a-a7e9-3f92226ee5eb" "backpropagation" %}} in neural networks. 
- There are many other versions of this, e.g. in differential geometry the derivative linear operator (multiplying Jacobians and perturbations dx right-to-left) is called a {{% resource_link "4e6d279b-9ec1-4cf2-931b-e2872fa322e1" "pushforward" %}}, whereas multiplying a gradient row vector (covector) by a Jacobian left-to-right is called a {{% resource_link "98e9217a-c498-4a70-8ccc-a486e1c5c8f4" "pullback" %}}. 
- This video on "{{% resource_link "2cf50840-a7af-4824-923d-5123c7219357" "Understanding Automatic Differentiation" %}}" by {{% resource_link "97f7bfbc-3160-4956-84fd-a699fdeb6e23" "Dr. Mohamed Tarek" %}} also starts with a similar left-to-right (reverse) vs right-to-left (forward) viewpoint and goes into how it translates to Julia code, and how you define custom chain-rule steps for Julia AD.

## Lecture 3

### Lecture Notes

- Part 1: {{% resource_link "e8eecb54-8a16-42ef-a24d-745cbf9451e3" "The Gradient of a Scalar Function of a Vector: Column Vector or Row Vector? (PDF)" %}}
- Part 2: {{% resource_link "d16e60c5-8982-4584-a1a5-cc9c290f7a3a" "Finite Difference (Jupyter notebook)" %}} ({{% resource_link "d9e83bd3-6b99-44b8-98c4-7ad59ffb2f4c" "download \"Finite Difference\" zip file" %}})

### Further Readings:

- Wikipedia has a useful list of {{% resource_link "862b8914-6694-4b70-956c-f37049e03c65" "properties of the matrix trace" %}}. 
- The "matrix dot product" introduced today is also called the {{% resource_link "30bce087-df61-4aeb-808a-af4058e26f7e" "Frobenius inner product" %}}, and the corresponding norm ("length" of the matrix viewed as a vector) is the {{% resource_link "922079db-519f-401f-889a-1b76a2dbe3e8" "Frobenius norm" %}}. 
- When you "flatten" a matrix A by stacking its columns into a single vector, the result is called {{% resource_link "0cdbebaf-9a5f-4c59-9775-c4adab68d807" "vec(A)" %}}, and many important linear operations on matrices can be expressed as {{% resource_link "1d099a8a-e43f-4e00-a6a9-756a5a9c81fc" "Kronecker products" %}}. 
- {{% resource_link "74f87569-1e0d-48a8-aa40-76b813d43208" "*The Matrix Cookbook* (PDF)" %}} has lots of formulas for derivatives of matrix functions. 
- There is a lot of information online on {{% resource_link "c072e56e-fe74-4a62-951a-551e6107403d" "finite difference" %}}, {{% resource_link "7327bd61-af6c-4ebd-8722-7fb6a714937e" "18.303 Notes on Finite Differences (PDF)" %}}, or {{% resource_link "44c437a4-c905-4e9a-8315-aa2d2b69f438" "Section 5.7 of Numerical Derivatives (PDF)" %}}. 
- The Julia {{% resource_link "242aa3e1-6b84-4afe-a21f-215f25def7c2" "FiniteDifferences.jl" %}} package provides lots of algorithms to compute finite-difference approximations; a particularly robust and powerful way to obtain high accuracy is to employ {{% resource_link "5401239e-084e-479b-9195-947d0385425d" "Richardson extrapolation" %}} to smaller and smaller δx. If you make δx too small, the finite precision (#digits) of {{% resource_link "4db5a206-9f8f-4f86-942a-4862e89d26af" "floating-point arithmetic" %}} leads to {{% resource_link "9ac68c88-9884-4e59-877b-fb1898f82a9b" "catastrophic cancellation" %}} errors.

## Lecture 4

### Lecture Notes

- Part 1: {{% resource_link "2b540304-7a27-4b57-80c3-6b694e9d3b7a" "The Gradient of the Determinant (html)" %}} ({{% resource_link "5153711d-d113-46cb-8df6-e7e20a7f78a2" "download the zip file" %}}) ({{% resource_link "ba7ce65c-f767-4459-8ebd-3dd65afb085a" "Julia source" %}}) ({{% resource_link "6cd714af-b338-40c7-a3a0-7d570503a662" "download Julia source zip file" %}})
- Part 2: {{% resource_link "ed4afe03-6d76-495e-872b-cf5c194f3d03" "Nonlinear Root-Finding, Optimization, and Adjoint-Method Differentiation (PDF)" %}}

### Further Readings (Part 1):

- There are lots of discussions of the {{% resource_link "fe648f42-dc91-4e58-b435-0e442d06b89b" "derivative of a determinant" %}} online, involving the {{% resource_link "87b023c0-0b4b-4060-831b-7454b833327f" "\"adjugate\" matrix" %}} det(A)A⁻¹. Not as well documented is that the gradient of the determinant is the cofactor matrix widely used for the {{% resource_link "67526795-abb1-48c6-a211-1f6c2697d7ab" "Laplace expansion" %}} of a determinant. 
- The formula for the {{% resource_link "3cd5d9bb-113f-4b5d-a005-73fda6d2c7f4" "derivative of log(det X)" %}} is also nice, and logs of determinants appear in surprisingly many applications (from statistics to quantum field theory). 
- {{% resource_link "74f87569-1e0d-48a8-aa40-76b813d43208" "*The Matrix Cookbook* (PDF)" %}} contains many of these formulas, but no derivations. 
- A nice application of d(det(A)) is solving for eigenvalues λ by applying Newton's method to det(A-λI)=0, and more generally one can solve det(M(λ))=0 for any function Μ(λ) — the resulting roots λ are called {{% resource_link "be14063d-0e57-4363-8ed7-3a0ef3ac3b24" "nonlinear eigenvalues" %}} (if M is nonlinear in λ), and one can apply Newton's method in {{% resource_link "6f1d3152-e76b-43ec-9cd2-2679d1052f0e" "\"The Nonlinear Eigenvalue Problem: Part II (PDF - 1.2 MB)\"" %}} using the determinant-derivative formula here.

### Further Readings (Part 2):

- There are many textbooks on {{% resource_link "5bafa66c-97e3-42c8-8684-e22458b373e2" "*Nonlinear Programming*" %}} (by Bertsekas), including specialized books on {{% resource_link "3b61d00f-90bf-475f-8af8-5fe402e59eb7" "*Convex Optimization*" %}} (by Boyd and Vandenberghe), {{% resource_link "3305c86a-f585-4840-81b8-f16b23b62b02" "*Introduction to Derivative-Free Optimization*" %}} (by Conn, Scheinberg, and Vicente), etcetera. 
- A useful review of topology-optimization methods can be found in Sigmund and Maute's "{{% resource_link "e5067873-f7d7-41bf-8c19-167851aa01bc" "Topology Optimization Approaches" %}}." 
- See the {{% resource_link "d4e9e361-3cbb-44a4-9168-fd6b5b6decf4" "Notes on Adjoint Methods (PDF)" %}} and {{% resource_link "808a0f46-a16b-4ae2-80b7-362094afbe14" "The Adjoint Method for Differentiating Complex Computations (PDF)" %}} from *18.335 Introduction to Numerical Methods*.

## Lecture 5

### Lecture Notes

- {{% resource_link "3fb574b6-9d05-49d6-b9f8-59012ce1ecb3" "Forward and Reverse Automatic Differentiation in a Nutshell" %}} (guest lecture by {{% resource_link "4e0c3bb6-a86c-4532-b0fe-68d22d125a35" "Dr. Chris Rackauckas" %}}) ({{% resource_link "16c346e3-c441-411e-b9a5-a3bbb8bf71d1" "download the zip file" %}})

### Further Readings:

- Googling "automatic differentiation" will turn up many, many resources—this is a huge practical field these days. {{% resource_link "3adca6cb-6e48-4069-8a88-d5c4d25c145e" "ForwardDiff.jl" %}} (described in detail by "{{% resource_link "bf30d717-9db4-4708-8219-2ce19838fcb7" "Forward-Mode Automatic Differentiation in Julia" %}}") uses {{% resource_link "8dcab5af-a846-45fd-ad46-d8688728c4db" "dual number" %}} arithmetic similar to lecture to compute derivatives.
- See also the article "{{% resource_link "8e050873-a2dc-46a8-a78c-4773e0b0be08" "How to Differentiate with a Computer" %}}," or google "dual number automatic differentiation" for many other reviews. 
- Implementing automatic reverse-mode AD is much more complicated than defining a new number type, unfortunately, and involves a lot more intricacies of compiler technology. See also Chris's blog post on {{% resource_link "7877a5d8-e9c3-4c63-aae8-531a01a917a5" "Engineering Trade-Offs in Automatic Differentiation" %}}, and Chris Rackauckas's discussion post on {{% resource_link "57fbb754-01f6-48e2-b86d-37e686515c97" "AD limitations" %}}.

## Lecture 6

### Lecture Notes

- Part 1: {{% resource_link "1aee9d00-51f0-4b24-ab9f-ed0de1f7aabe" "Derivatives of Eigenproblems (html)" %}} ({{% resource_link "4c0529a7-9649-4d68-9617-399fce0743dc" "download the zip file" %}}) ({{% resource_link "ba7ce65c-f767-4459-8ebd-3dd65afb085a" "Julia source" %}}) ({{% resource_link "4b3b3a58-f350-4ec8-a621-49d634341796" "download Julia source zip file" %}})
- Part 2: Second Derivatives, Bilinear Forms, and Hessian Matrices \[notes not available\]

### Further Readings (Part 1):

- Computing derivatives on curved surfaces ("manifolds") is closely related to {{% resource_link "0995fb1f-d9e1-4edf-9f84-d843bd0c2bc7" "tangent spaces" %}} in differential geometry. The effect of constraints can also be expressed in terms of {{% resource_link "ad0d5682-b617-40c0-86f9-e56e0e093791" "Lagrange multipliers" %}}, which are useful in expressing optimization problems with constraints (see also Chapter 5 of {{% resource_link "9b40b0d4-ea2c-4e32-a47a-f43c6a0c2ad0" "*Convex Optimization*" %}} by Boyd and Vandenberghe). 
- In physics, first and second derivatives of eigenvalues and first derivatives of eigenvectors are often presented as part of {{% resource_link "9896700a-54fd-469f-9549-060a517d223d" "\"time-independent\" perturbation theory" %}} in quantum mechanics, or as the {{% resource_link "685f6ac6-42a3-439e-900e-25092edad212" "Hellmann-Feynmann theorem" %}} for the case of dλ. 
- The derivative of an eigenvector involves *all* of the other eigenvectors, but a much simpler "vector-Jacobian product" (involving only a single eigenvector and eigenvalue) can be obtained from left-to-right differentiation of a *scalar function* of an eigenvector, as reviewed in the {{% resource_link "d4e9e361-3cbb-44a4-9168-fd6b5b6decf4" "18.335 Notes on Adjoint Methods (PDF)" %}}.

### Further Readings (Part 2):

- {{% resource_link "f06d15c0-03da-42ef-b19a-543028df9e0d" "Bilinear forms" %}} are an important generalization of quadratic operations to arbitrary vector spaces, and we saw that the second derivative can be viewed as a {{% resource_link "e3e0d87a-7506-43b6-b359-dd176d3839ac" "symmetric bilinear form" %}}. This is closely related to a {{% resource_link "c7ab4ea1-0400-4354-ae5b-c55239ba29cb" "quadratic form" %}}, which is just what we get by plugging in the same vector twice, e.g. the f''(x)\[δx,δx\]/2 that appears in quadratic approximations for f(x+δx) is a quadratic form. 
- The most familar multivariate version of f''(x) is the {{% resource_link "d2925290-5429-4128-bd43-d5de59949ae3" "Hessian matrix" %}}. 
- Khan Academy has an introduction to {{% resource_link "61f1f63d-bdc2-4db6-bdb1-1542edb7b50f" "quadratic approximation" %}}.

## Lecture 7

### Lecture Notes

- Part 1: Hessian Matrices (cont.) \[notes not available\]
- Part 2: {{% resource_link "2949c5a4-cf6e-4d05-a3d8-6827519cd759" "Backpropagation through Back Substitution with a Backslash (PDF)" %}}

### Further Readings (Part 1):

- {{% resource_link "bcb1db69-3480-4bb4-ba78-39afe2c5b282" "Positive-definite" %}} Hessian matrices, or more generally {{% resource_link "d8439f22-9fdb-4b0c-bfb8-7aeaf65147e7" "definite quadratic forms" %}} f″, appear at extrema (f′=0) of scalar-valued functions f(x) that are local minima; there are a lot more formal treatments of the same idea—{{% resource_link "c3a9636d-3cb6-49d3-9486-ee4238c295b0" "Unconstrained Optimization (PDF)" %}}, and conversely Khan academy has the {{% resource_link "33b7f288-cbb6-4b2b-8912-e0b610a534c8" "simple 2-variable version" %}} where you can check the sign of the 2×2 eigenvalues just by looking at the determinant and a single entry (or the trace). 
- There's a nice {{% resource_link "515779de-ee48-4fcd-bcee-6097702ba2af" "stackexchange discussion" %}} on why an {{% resource_link "77241122-0f3e-4f27-8bf8-0b665e254db7" "ill-conditioned" %}} Hessian tends to make steepest descent converge slowly.
- University of Toronto's {{% resource_link "1f465303-100e-4410-a986-a2075a4d026e" "Course Notes on Optimization (PDF - 3.3 MB)" %}} may also be helpful.

### Further Readings (Part 2):

- See this blog post on {{% resource_link "f52af74e-3012-4c63-b363-7fa675160724" "Calculus on Computational Graphs" %}} for a gentle review.
- See Columbia University's {{% resource_link "c3cec2fa-45aa-4a68-8e20-d53829334c03" "Course Notes on Computational Graphs, and Backpropagation (PDF)" %}} for a more formal approach.

## Lecture 8

### Lecture Notes

- Part 1: Hessian Matrices (cont.) \[notes not available\]
- Part 2: {{% resource_link "dfa38649-0a94-4d2f-90f9-50fee82de874" "Differentiable Programming and Neural Differential Equations" %}} (guest lecture by {{% resource_link "4e0c3bb6-a86c-4532-b0fe-68d22d125a35" "Dr. Chris Rackauckas" %}})

### Further Readings (Part 1):

- See e.g. these Stanford University's notes on {{% resource_link "07aa4df7-da2d-43ac-8e16-c9dc6570556b" "Sequential Convex Programming (PDF)" %}} using trust regions (sec. 2.2). 
- See 18.335 notes on {{% resource_link "d9ab2edb-fa9f-4e5f-bfed-04e9030a5e8a" "Quasi-Newton Optimization: Origin of the BFGS Update (PDF)" %}}. 
- The fact that a quadratic optimization problem in a sphere has {{% resource_link "0b9e1b07-d282-4c0b-b9e9-004c9edd3459" "strong duality" %}} and hence is efficiently solvable as discussed in section 5.2.4 of the {{% resource_link "9b40b0d4-ea2c-4e32-a47a-f43c6a0c2ad0" "*Convex Optimization*" %}} by Boyd and Vandenberghe. 
- There has been a lot of work on {{% resource_link "d93d2b96-726a-4cd8-8a33-3e74ad8b8cfd" "Hessian automatic computation" %}}, but for large-scale problems you can ultimately only compute Hessian-vector products efficiently in general, which are equivalent to a directional derivative of the gradient, and can be used e.g. for {{% resource_link "f7cc7ef6-1f76-4981-91b5-9acd0a02afc3" "Newton-Krylov methods" %}}.

### Further Readings (Part 2):

- A very general reference on adjoint-method (reverse-mode/backpropagation) differentiation of ODEs (and generalizations thereof), using notation similar to that of Chris R. today, is "{{% resource_link "fc05b8d4-b46f-4e0b-a334-234274209d49" "Adjoint Sensitivity Analysis for Differential-Algebraic Equations: The Adjoint DAE System and Its Numerical Solution" %}}".
- See also the {{% resource_link "8755868c-a119-4fe7-b391-7219fc2cf6da" "adjoint sensitivity analysis" %}} section of Chris's amazing {{% resource_link "27dcbabb-ee0c-4cf7-97c5-8f2d3cea918f" "DifferentialEquations.jl software suite" %}} for numerical solution of ODEs in Julia. 
- There is a nice YouTube lecture on {{% resource_link "28ef89a9-5f67-40ce-aa15-5d1e78cd39b2" "Adjoint State Method for an ODE" %}}, again using a similar notation.