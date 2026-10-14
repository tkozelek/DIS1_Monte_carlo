# Monte Carlo simulation of a car parts warehouse

Semester project for Discrete Simulation (FRI UNIZA, 2025), the first of three:
this Monte Carlo one,
[event-driven](https://github.com/tkozelek/DIS2_Event_driven_simulation) and
[agent-based](https://github.com/tkozelek/DIS3_Agent_Simulation).

A warehouse sells shock absorbers, brakes and lights. Every week it orders goods from one of two
suppliers, who do not always deliver, and a customer comes with a random demand. Storing parts costs
money and every missing part costs a penalty. The simulation compares ordering strategies by their
total cost over 30 weeks.

## How it works

- My own simulation core with replications, and my own random generators (uniform and empirical,
  discrete and continuous) on top of `Random`, with a separate seed for each generator.
- Strategies A to D from the assignment and a custom strategy E, loaded from a CSV file with the
  supplier and the quantities for every week. Example files are in the repository root.
- Charts with JFreeChart: how the average cost settles as the replications grow, and the cost day by
  day in a single run. The simulation can be stopped at any time.

## Run it

Open the project in IntelliJ IDEA and run `kozelek.Main` (the GUI uses IntelliJ GUI Designer forms).
Java 23, Maven.
