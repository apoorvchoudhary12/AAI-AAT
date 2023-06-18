# AAI-AAT
1. Introduction of the Problem
The given problem revolves around simulating a fortune wheel in a stochastic gaming scenario. A fortune wheel typically consists of multiple sectors, each associated with a specific probability of being selected. The objective is to simulate the fortune wheel and determine the outcome based on the probabilities assigned to each sector.
To solve this problem, we can use optimization techniques provided by the OR-Tools library. By formulating the problem as a linear programming model, we can use the GLOP solver to find the optimal solution. The decision variables represent the selection of sectors, and the objective function is defined to maximize the expected outcome based on the assigned probabilities.
Initially, the sectors and their probabilities are defined. The solver is created, decision variables are instantiated, and the objective function is set to maximize the expected outcome. A constraint is added to ensure that only one sector is chosen. Additional constraints can be included based on specific requirements.
The simulation is then executed by solving the linear programming model. The selected sector is determined randomly based on the solution of the decision variables. The simulation is repeated for a specified number of times, and the count of each sector is recorded to analyze the results.
The simulation results are printed, displaying the probability of each sector being selected. Additionally, a visualization is provided using a bar chart to represent the counts of each sector. The expected value and entropy of the fortune wheel distribution are also calculated and displayed as measures of average outcome and randomness, respectively. Finally, the code identifies the winner by finding the sector with the highest count in the simulation results and prints the outcome as "Winner: Sector X".
2. Problem Formulation – Mathematically
To mathematically formulate the given problem of simulating a fortune wheel in a stochastic gaming scenario, we define the following:
1.Decision Variables:
Binary decision variables x[i] for each sector i, indicating whether sector i is selected or not. x[i] = 1 if sector i is selected, and x[i] = 0 otherwise.
2.Objective Function:
Maximize the expected outcome based on the selected sectors: Maximize: sum(p[i] * x[i]) for all sectors i
where p[i] represents the probability associated with sector i.
 3. Constraints:
• Only one sector can be selected:
Constraint: sum(x[i]) = 1
This ensures that exactly one sector is chosen.
• Binary constraints on decision variables: Constraint: x[i] in {0, 1} for all sectors i
This ensures that the decision variables are binary.
These constraints ensure that only one sector is selected and that the decision variables are binary.Additional constraints can be added depending on specific requirements, such as limitations on the sum of selected probabilities or restrictions on the number of sectors that can be chosen.By formulating the problem in this way, we can apply optimization techniques, such as linear programming, to find the optimal solution that maximizes the expected outcome while adhering to the given constraints.
3. Tool Used:
OR-Tools: OR-Tools is an open-source software library developed by Google that provides a collection of optimization tools, including linear programming solvers. It offers powerful optimization algorithms and modeling capabilities that can be utilized to formulate and solve the fortune wheel simulation problem.
Linear Programming: The problem of simulating the fortune wheel can be formulated as a linear programming model. Linear programming is a mathematical optimization technique used to maximize or minimize a linear objective function subject to linear constraints. By formulating the problem as a linear programming model, we can leverage the OR-Tools library to find the optimal solution.
Programming Language: A programming language such as Python is be used to implement the code that utilizes OR-Tools and formulates the linear programming model. Python, with its rich scientific computing libraries and easy-to-use syntax, is often a popular choice for such problems.
4.Algorithm:
The algorithm used for simulating a fortune wheel in a stochastic gaming scenario can be explained as follows:

Initialization:
• Initialize variables and data structures to store information about the sectors and their
outcomes. This includes the counts of each sector, the maximum count, and the winner
sector. Simulation Loop:
• Perform a loop to simulate the fortune wheel for a specified number of iterations. In each iteration:
• Generate a random number between 0 and 1 to represent the spin of the wheel.
• Iterate through each sector and calculate the cumulative probability by summing up the
probabilities of the previous sectors.
• Check if the generated random number is less than or equal to the cumulative
probability of the current sector.
• If it is, update the count of the current sector and check if it becomes the new winner
by having the maximum count. Probability Calculation:
• After completing the simulation loop, calculate the probabilities of each sector by dividing their respective counts by the total number of iterations. This provides an estimate of the likelihood of each sector being selected.
Winner Determination:
• Iterate through the counts of each sector and find the sector(s) with the highest count.
This indicates the winner(s) of the fortune wheel simulation. Outcome Presentation:
• Display the winner sector and its corresponding outcome. This can be done by printing the winner sector or providing any additional details associated with the winning sector.
The algorithm aims to simulate the fortune wheel by randomly selecting sectors based on their assigned probabilities. It keeps track of the counts of each sector during the simulation and determines the winner based on the highest count. The probability calculation step provides insights into the likelihood of each sector being selected. Finally, the algorithm presents the outcome by identifying the winner sector and displaying the corresponding result.
Conclusions:
In conclusion, simulating a fortune wheel in a stochastic gaming scenario allows us to understand the probabilities and outcomes associated with each sector of the wheel. By using optimization techniques provided by libraries such as OR-Tools, we can formulate the problem as a linear programming model and find the optimal solution to maximize the expected outcome.
By simulating the fortune wheel and running multiple iterations, we can gather statistical information about the occurrences of each sector and determine the winner based on the highest count. This provides insights into the distribution of outcomes and allows us to analyze the probabilities of each sector being selected.Additionally, visualization techniques such as bar charts can be used to visually represent the counts of each sector, providing a clearer understanding of the distribution. Measures such as the expected value and entropy can be calculated to quantify the average outcome and randomness of the fortune wheel distribution. By incorporating constraints and regularization techniques, we can control the complexity of the model and encourage additional properties such as sparsity, derivative smallness, or robustness to noise or missing inputs.
Simulating a fortune wheel in a stochastic gaming scenario is not only an interesting problem to solve, but it also has practical applications in various fields such as gambling, decision- making processes, and probabilistic analysis.
Overall, the simulation provides valuable insights into the behavior of the fortune wheel, allows for analysis and optimization, and facilitates decision-making based on the probabilities and outcomes associated with each sector.
