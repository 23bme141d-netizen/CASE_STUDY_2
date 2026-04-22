Numerical Simulation of Vehicle Suspension System using Mass–Spring–Damper Model and FDM
->Project Overview
This project focuses on analysing the dynamic response of a vehicle suspension system using a mass–spring–damper model and solving the governing equation numerically using the Finite Difference Method (FDM) in MATLAB.
The displacement response is obtained when:
• Newton’s Second Law is satisfied
• Spring and damping forces are correctly modeled
• Time-dependent behaviour is computed numerically
This project demonstrates how numerical methods and time-stepping techniques can be used to analyse unsteady second-order systems efficiently using MATLAB.
-Objective
The main objectives of this project are:
• To understand the concept of vibration in mechanical systems
• To model a vehicle suspension system (quarter car model)
• To apply Newton’s Second Law
• To convert differential equations into finite difference form
• To simulate system response using MATLAB
• To study underdamped, critically damped, and overdamped cases
->Problem Description
A vehicle suspension system is modelled as:
• A single degree of freedom system (SDOF)
• Consisting of mass, spring, and damper
The system parameters used are realistic:
• Vehicle mass = 1300 kg → Quarter car mass = 325 kg
• Spring stiffness = 20000 N/m
• Initial displacement = 0.05 m (road bump)
• Initial velocity = 0 m/s
The system is analysed under free vibration conditions to determine displacement variation with time.
->Mathematical Formulation
$$
m \frac{d^2 x}{dt^2} + c \frac{dx}{dt} + kx = 0
$$

Equation of Motion
Where:
• m = mass
• cc = damping coefficient
• k = stiffness
• x(t) = displacement
Finite Difference Approximation
Second derivative:
$$
\frac{d^2 x}{dt^2} = \frac{x^{n+1} - 2x^n + x^{n-1}}{\Delta t^2}
$$
First derivative:
$$
\frac{dx}{dt} = \frac{x^n - x^{n-1}}{\Delta t}
$$
Final Discretized Equation
$$
x^{n+1} =
\frac{
(2m - c \Delta t)x^n - (m - c \Delta t)x^{n-1} - k \Delta t^2 x^n
}{m}
$$
Critical Damping
cc=2mkc_c = 2\sqrt{mk}



 
Damping Cases
• Underdamped → c=0.5Cc 
• Critical damping → c=Cc 
• Overdamped → c=2Cc
->Methodology
The displacement is computed using numerical simulation:
1.	Define system parameters 
2.	Convert full vehicle into quarter car model 
3.	Calculate critical damping 
4.	Apply finite difference equation 
5.	Solve displacement iteratively 
6.	Plot displacement vs time 
->MATLAB Implementation
The MATLAB program performs:
• Definition of system parameters
• Calculation of damping values
• Implementation of FDM equation
• Time-stepping numerical solution
• Plotting displacement response
->Results
The simulation shows:
• Underdamped system → oscillatory decay
• Critical damping → fastest return to equilibrium
• Overdamped system → slow decay
The system eventually reaches steady-state equilibrium.
->Key Concepts Demonstrated
This project illustrates:
• Newton’s Second Law
• Mechanical vibration analysis
• Finite Difference Method (FDM)
• Time-domain simulation
• Damping effects
• Numerical solution of ODE
->Engineering Significance
This model is widely used in:
• Vehicle suspension design
• Shock absorber systems
• Ride comfort analysis
• Structural vibration control
• Mechanical system modelling
This project highlights the importance of numerical simulation in modern mechanical engineering analysis.
->How to Run the Project
1.	Open MATLAB 
2.	Copy the provided code 
3.	Run the script 
4.	Observe:
• Displacement vs time graph
• Effect of damping 
->Author
Dhruv Patel
3rd Year Mechanical Engineering Student
Computational Engineering Laboratory Project
->Project Summary
This project successfully demonstrates how a vehicle suspension system can be modelled as a mass–spring–damper system and solved using the Finite Difference Method.
It reinforces the role of numerical methods and MATLAB in analysing unsteady dynamic systems in engineering.
