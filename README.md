# CS3SY26_ProjectProposal by Aline Teresa Mendoza from CS Unit of PSHS


## Project Proposal Template:
cvbbbc
### Project Title or Name of the Application	:
### Section			   	      :
### Group Members			    :
### Date (Proposal Date)  : Nov 5, 2026
fdfhdfhfshsdhfhhtrthdfh
### Project Description:

**Project Overview:**
Patient Zero is an interactive epidemiological simulator designed to model the spread of infectious diseases and the impact of vaccination across a population over time. Understanding disease transmission and intervention strategies like herd immunity can be difficult through static charts alone. This application addresses that need by providing a visual, real-time sandbox where users can manipulate key outbreak parameters and observe how viruses propagate, mutate, and respond to public health measures.

**Target Demographics**
The primary target users for this application are high school and introductory college students, educators, and science enthusiasts.

Students can use the simulator as an interactive study tool to visualize biological and mathematical concepts such as infection rates, recovery timelines, and vaccine efficacy.

Educators can utilize the application during lectures or lab sessions to demonstrate real-world epidemiological scenarios without requiring complex statistical software.

**System Components, Features & Expected Outputs:**
The system is built around an object-oriented architecture where six core classes interact to run the simulation, manage immunization, and generate data:

Simulation (Core Engine): Controls the overall execution flow and timeline of the outbreak. It tracks dayCount, transmissionRate, and populationSize, utilizing methods like startSimulation(), pauseSimulation(), and stepTick() to advance the model day by day. It directly manages the spatial Environment and triggers updates to the StatisticsTracker.

Environment (Spatial Grid): Represents the physical space where interactions occur, defined by its width, height, and a list of active agents. Through updateGrid() and checkCollisions(), it tracks agent positions and detects when infected and susceptible individuals come into contact.

Agent (Population Entity): Represents an individual within the population, holding attributes for agentID, healthStatus (e.g., susceptible, infected, recovered, deceased), isVaccinated, and spatial coordinates (xCoord, yCoord). Agents interact with the environment and pathogens via move(), infect(), recover(), vaccinate(), and die().

Virus (Pathogen Model): Defines the biological characteristics of the disease, including virusName, infectionProbability, recoveryDuration, and mortalityRate, along with a mutate() method to simulate evolving strains. When an Agent encounters a Virus, these attributes determine the likelihood of transmission and the severity of the outcome.

Vaccine (Intervention Module): Models immunization efforts using vaccineName, efficacyRate, and distributionRate. Through the administer() method, vaccines are distributed to agents, updating their isVaccinated status and lowering their susceptibility to contracting the Virus.

StatisticsTracker (Data & Output Module): Monitors population metrics throughout the simulation, recording totalInfected, totalRecovered, totalVaccinated, and totalDead. Using recordData() and exportCSV(), it generates the primary expected outputs: real-time population trend graphs and downloadable CSV datasets for further spreadsheet analysis.
The primary target users for this application are high school and introductory college students, educators, and science enthusiasts.

Students can use the simulator as an interactive study tool to visualize biological and mathematical concepts such as infection rates, recovery timelines, and vaccine efficacy.

Educators can utilize the application during lectures or lab sessions to demonstrate real-world epidemiological scenarios without requiring complex statistical software.

System Components, Features & Expected Outputs
The system is built around an object-oriented architecture where six core classes interact to run the simulation, manage immunization, and generate data:

Simulation (Core Engine): Controls the overall execution flow and timeline of the outbreak. It tracks dayCount, transmissionRate, and populationSize, utilizing methods like startSimulation(), pauseSimulation(), and stepTick() to advance the model day by day. It directly manages the spatial Environment and triggers updates to the StatisticsTracker.

Environment (Spatial Grid): Represents the physical space where interactions occur, defined by its width, height, and a list of active agents. Through updateGrid() and checkCollisions(), it tracks agent positions and detects when infected and susceptible individuals come into contact.

Agent (Population Entity): Represents an individual within the population, holding attributes for agentID, healthStatus (e.g., susceptible, infected, recovered, deceased), isVaccinated, and spatial coordinates (xCoord, yCoord). Agents interact with the environment and pathogens via move(), infect(), recover(), vaccinate(), and die().

Virus (Pathogen Model): Defines the biological characteristics of the disease, including virusName, infectionProbability, recoveryDuration, and mortalityRate, along with a mutate() method to simulate evolving strains. When an Agent encounters a Virus, these attributes determine the likelihood of transmission and the severity of the outcome.

Vaccine (Intervention Module): Models immunization efforts using vaccineName, efficacyRate, and distributionRate. Through the administer() method, vaccines are distributed to agents, updating their isVaccinated status and lowering their susceptibility to contracting the Virus.

StatisticsTracker (Data & Output Module): Monitors population metrics throughout the simulation, recording totalInfected, totalRecovered, totalVaccinated, and totalDead. Using recordData() and exportCSV(), it generates the primary expected outputs: real-time population trend graphs and downloadable CSV datasets for further spreadsheet analysis.

# Class Diagram:
!([CS3SY26_ProjectProposal/photos/Untitled Diagram-2026-11-20T10-06-51.png)](https://github.com/getschooledon/CS3SY26_ProjectProposal/blob/main/photos/Untitled%20Diagram-2026-11-20T10-06-51.png))

### Goals:

- Objective 1: Implement a core Simulation engine and spatial Environment grid that manages individual Agent entities and tracks their movement and health state transitions.
- Objective 2: Integrate a configurable Virus model with adjustable parameters such as transmission probability, recovery duration, and mortality rates.
- Objective 3: Implement a Vaccine module and distribution mechanism to simulate immunization efficacy and its protective impact on agent susceptibility.
- Objective 4: Build a StatisticsTracker component to record real-time data on infected, recovered, vaccinated, and deceased populations for analysis and export.
