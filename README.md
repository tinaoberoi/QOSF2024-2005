This repo contains the solution Cohort 10 QOSF tasks

## Task 1:
<hr>
Solution: ![Taks1.ipynb](./QOSF%20Task1.ipynb)

```

Task 1 State VectorStatevector simulation of quantum circuits

For this task, you will implement a state vectorstatevector simulator for quantum circuits from scratch. The goal is to demystify how to simulate a quantum computer and to demonstrate your familiarity with quantum circuits.

1) Naive simulation using matrix multiplication

Remember that  [1, 0] = |0> is the most common representation of the single-qubit zero state, and analogously [0, 1] = |1>. 

Most matrix representations of quantum gates you can find online follow this convention. For example, the X gate can be written as

X = [[1  0], [0   1]]  

Using the Kronecker product and the np.kron function in numpy (we are using it as an example, but you can use any library you want to), you can create a vector of length 2^n representing an n-qubit quantum state, and matrix representation of X, H, and CNOT gates. 

Hint: The single-qubit Identity matrix is

I = [[0  1], [1   0]]  

Define a quantum circuit consisting of these gates and apply the gates sequentially to the state vectorstatevector via matrix multiplication. 

Plot the runtime of your code as a function of the number of qubits. How many qubits can you simulate this way? 


2) Advanced simulation using tensor multiplication

Tensors are generalizations of vectors and matrices to any number of dimensions. Instead of representing an n-qubit state as a vector of length 2^n, it may be more natural to write it as an n-dimensional tensor of shape (2, 2, …., 2). The transformations between these two representations are naturally possible via np.reshape and np.flatten.

Using tensor multiplication and the np.tensordot (or np.einsum) function, you can apply a gate to the quantum state by multiplying the 1- or 2-qubit matrices with the state tensor along the corresponding qubit axes.

Define a quantum circuit consisting of the 1- and 2-qubit matrix representations of X, H, CNOT (same as above) and apply them sequentially to the quantum state tensor via tensor multiplication.

Plot the runtime of your code as a function of the number of qubits. How many qubits can you simulate this way? Compare your results to subtask 1).

```

## Task3:

<hr>

Solution: ![Taks3.ipynb](./QOSF%20Task3.ipynb)


```
Task 3 Optimization 

In the Bin Packing Problem (BPP), given a collection of items, the goal is to efficiently pack the items into the minimum number of bins, where each item has an associated weight, and the bins have a maximum weight. The problem can be found in different industries. For example, the supply chain management industry requires loading multiple packages onto a truck, plane, or vessel. In this task, you will solve the BPP using quantum computing.

From Integer Linear Programming (ILP) to Quadratic Unconstrained Binary Optimization (QUBO)

Define the ILP formulation of the BPP. You can use Docplex or similar frameworks to do it. 
Create a function to transform the ILP model into a QUBO 
Test your function with specific instances (size small, medium, and big) 

Create a Brute Force solver for the QUBO problem and solve the specific instances. 

To solve the QUBO, use quantum annealing simulators. You can use the Dwave Ocean Framework. Here is an example.

Use a Quantum Variational approach to solve the QUBO. 

Create multiple Ansantz for tests. 
Build a function with input being the QUBO and Ansantz. Using a hybrid approach solved the QUBO. 

Use QAOA to solve the QUBO. 

Create from scratch a QAOA function. 

Compare and analyze the results. 

What is the difference between QAOA, Quantum Annealing, and Quantum Variational approaches with different Ansatz? 
How do the results compare with the brute force approach? 

```