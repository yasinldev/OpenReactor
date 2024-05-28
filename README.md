# OpenReactor

OpenReactor is a comprehensive nuclear reactor simulation tool designed to model the behavior and dynamics of nuclear reactors. This project aims to provide an educational and research platform for understanding the complexities of nuclear reactor operations, safety protocols, and performance optimization.

## Planned Features

* Actor Reactor Modeling (ARM): A novel approach to reactor simulation that combines the best features of deterministic and stochastic methods.
* Multi-Physics Simulation: Integration of thermal-hydraulics, neutronics, and fuel performance models to provide a comprehensive reactor simulation environment.
* Graphical User Interface (GUI): An intuitive and user-friendly interface for setting up simulations, visualizing results, and analyzing data.
* Data Analysis Tools: Built-in tools for post-processing simulation data, generating reports, and conducting sensitivity analyses.
* Educational Resources: Tutorials, documentation, and example problems to help users learn how to use the software and understand nuclear reactor concepts.

## Theory and Background

OpenReactor is built on a foundation of advanced nuclear engineering principles and computational methods. The software leverages state-of-the-art algorithms and models to simulate the behavior of nuclear reactors under various operating conditions and scenarios. By combining the latest research in reactor physics, thermal-hydraulics, and materials science, OpenReactor provides a powerful tool for studying reactor dynamics and performance. 

### Theory Foundations
At the core of OpenReactor is the application of neutron transport theory and reactor kinetics. Neutron transport equations, particularly the Boltzmann transport equation[1,1], form the basis for simulating the distribution and behavior of neutrons within the reactor core. The software employs both deterministic and Monte Carlo methods to solve these equations, allowing for accurate predictions of neutron flux distributions, reactivity, and power generation. Reactor kinetics models, including point kinetics and spatial kinetics, are integrated to simulate transient behaviors and control rod movements.

 ```math
\left( \frac{1}{v} \frac{\partial}{\partial t} + \mathbf{\Omega} \cdot \nabla + \Sigma_t(\mathbf{r}, E) \right) \psi(\mathbf{r}, \mathbf{\Omega}, E, t) = \int_{4\pi} \int_0^\infty \Sigma_s(\mathbf{r}, E' \rightarrow E, \mathbf{\Omega}' \cdot \mathbf{\Omega}) \psi(\mathbf{r}, \mathbf{\Omega}', E', t) \, dE' \, d\mathbf{\Omega}' + S(\mathbf{r}, \mathbf{\Omega}, E, t)
```
<p align="center">
  <sup>1.1</sup>
</p>

Thermal-hydraulic modeling is crucial for understanding the heat transfer and fluid flow within the reactor. OpenReactor utilizes the Navier-Stokes equations for fluid dynamics and heat conduction equations for thermal analysis. Coupled with detailed coolant flow and heat exchange models, the software simulates the thermal performance of the reactor core, including temperature distributions, pressure drops, and boiling phenomena in both single-phase and two-phase flows.

## Computing
The OpenReactor project will be implemented in Rust, a systems programming language known for its performance and safety features. Rust's memory safety guarantees and concurrency model make it an ideal choice for developing high-performance scientific software like a nuclear reactor simulator.

Rust is chosen for several reasons. Firstly, Rust ensures memory safety through its ownership system, which prevents common bugs such as null pointer dereferencing and buffer overflows without needing a garbage collector. This memory safety is crucial for developing reliable software, especially in complex applications like reactor simulations. Secondly, Rust’s concurrency model enables safe and efficient parallel computations, which are essential for handling the complex simulations that involve multiple physical processes running concurrently. Finally, Rust's performance is comparable to C and C++, making it suitable for compute-intensive applications such as neutron transport simulations.

In the field of computer science, several advanced computational methods and techniques will be utilized to develop and optimize the OpenReactor simulation software. Parallel computing is crucial for efficiently solving the complex, large-scale problems encountered in nuclear reactor simulations. By dividing tasks into smaller sub-tasks that can be processed simultaneously, parallel computing significantly reduces computation time. Rust’s concurrency features, including threads and asynchronous programming, facilitate the implementation of parallel algorithms, thereby enhancing the performance and efficiency of the simulations.

Numerical methods are mathematical techniques used to approximate solutions to complex equations, and they are central to the functioning of OpenReactor. Finite Element Analysis (FEA) is one such method, used for solving partial differential equations that describe neutron transport and thermal-hydraulic behavior. FEA discretizes the reactor geometry into smaller elements, allowing for accurate and efficient computation of physical phenomena. Another crucial method is Monte Carlo Simulations, which are used for neutron transport calculations. These stochastic methods simulate the random paths of neutrons and are particularly useful for modeling complex geometries and material compositions within the reactor. Additionally, iterative solvers are employed for solving large systems of linear equations that arise from discretization methods. Iterative solvers like Conjugate Gradient or GMRES are efficient and can handle the large matrices typical in reactor simulations.

## References and Further Reading
To ensure comprehensive documentation and proper attribution of academic and technical sources, each directory in the OpenReactor codebase will contain a `README.md` file. These files will provide detailed information about the code within the directory, including explanations, documentation, and references to academic sources. This approach will facilitate understanding, maintainability, and transparency of the codebase.

## License
OpenReactor is licensed under the MIT License. This license allows for open source distribution and modification of the software, making it freely available for both personal and commercial use. Users are permitted to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software, provided that the original copyright notice and this permission notice are included in all copies or substantial portions of the software.

