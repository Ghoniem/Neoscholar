# Silicon-Based Solar Cell Technology

##  Project Statement

Silicon-based solar cell technology is a cornerstone of modern renewable
energy systems, providing an efficient and sustainable means to harness
solar energy. This project invites undergraduate students to explore the
key principles and applications of silicon photovoltaics. Students will
gain insights into the photoelectric effect, bandgap energy, and
spectral absorption properties that underlie the conversion of sunlight
into electricity.

The project will also explore the manufacturing processes of silicon
solar cells, examining techniques such as wafer production, doping, and
anti-reflective coatings. A focus will be placed on evaluating
efficiency improvements through advanced designs like passivated emitter
rear contact (PERC) cells.

Beyond theoretical knowledge, students will use Python to simulate the
Shockley-Queisser efficiency limit for silicon-based cells. The
simulator will allow them to calculate and visualize the efficiency as a
function of material properties and environmental conditions. The
results will include solar spectrum utilization and recommendations for
optimizing cell designs.

The project further explores the economic and environmental implications
of solar technology, including cost trends, government incentives, and
lifecycle emissions. By the end of the project, students will have a
comprehensive understanding of silicon-based solar cell technology and
its pivotal role in the transition to sustainable energy systems.

## Physics of Silicon-Based Solar Cells

Students will dive into the underlying physics that govern silicon solar
cell performance, including:

-   The **photoelectric effect** and its role in converting sunlight
    into electricity.

-   **Bandgap energy** of silicon and how it influences photon
    absorption.

-   **Spectral properties** of sunlight and how they impact the
    efficiency of solar cells.

-   Loss mechanisms, such as thermalization and reflection losses.

**Python Development Idea (Optional - with guidance):**\
Students can calculate the theoretical efficiency of a silicon solar
cell using the **Shockley-Queisser limit**. By inputting solar spectral
data and the silicon bandgap energy, they can:

-   Simulate the maximum efficiency of a single-junction silicon solar
    cell.

-   Create visualizations of solar spectrum utilization, including
    absorbed vs. unused energy.

## Manufacturing Process

Students will examine the manufacturing steps for silicon solar cells,
including:

-   Extraction and purification of silicon from raw materials.

-   Wafer production: single-crystal silicon (Czochralski process) vs.
    polycrystalline silicon.

-   Fabrication steps such as doping, anti-reflective coating, and
    contact grid application.

-   Efficiency vs. cost trade-offs in advanced technologies like PERC
    (Passivated Emitter and Rear Cell).

## Applications

Students will study the widespread applications of silicon-based solar
cells.

-   Residential and commercial rooftop installations.

-   Utility-scale solar farms.

-   Hybrid systems, such as solar battery storage.

-   Emerging areas, including solar integration into wearables and
    buildings (e.g., building-integrated photovoltaics, BIPV).

## Economics

Students will assess the economic aspects of silicon-based solar cell
technology.

-   The cost breakdown of solar cell manufacturing and installation.

-   Impact of economies of scale and government incentives.

-   Market trends in the adoption of solar energy globally.

-   Comparison of silicon-based solar cells to other technologies like
    thin-film or perovskite solar cells.

## Environmental Impact {#environmental-impact .unnumbered}

Students will analyze the environmental implications:

-   Carbon footprint of silicon solar cell manufacturing.

-   Comparison of lifecycle emissions with other energy sources.

-   End-of-life management: challenges in recycling and disposal of
    silicon solar cells.

-   Role of solar energy in reducing the reliance on fossil fuels.

## Suggested Python Project

**Title:** *Solar Cell Efficiency Simulator*\
**Objective:** Develop a Python program that calculates and visualizes
the theoretical efficiency of a silicon solar cell.\
**Features:**

1.  **Input Parameters:**

    -   Solar spectrum data (AM1.5 standard spectrum).

    -   Silicon band gap energy.

    -   Effects of temperature on efficiency.

2.  **Calculations:**

    -   Use the Shockley-Queisser model to calculate maximum efficiency.

    -   Analyze the impact of different spectral regions (visible,
        infrared, etc.) on energy conversion.

3.  **Visualizations:**

    -   Plot the solar spectrum with highlighted absorbed and unused
        regions.

    -   Efficiency as a function of band gap energy for various
        materials.

4.  **Output:**

    -   Report showing the efficiency limits under standard conditions.

    -   Recommendations for optimizing silicon solar cell designs.

## Equations of the Model

This document describes the equations used in a practical solar cell
efficiency model that incorporates key real-world loss mechanisms. The
model extends the Shockley-Queisser limit with adjustments for
reflection, recombination, resistive, and thermalization losses.

## Solar Spectrum

The spectral irradiance $I(E)$ of sunlight is modeled using Planck's
law:
$$I(E) = \frac{2 \pi c^2 E^3}{(hc)^3 \left(e^{E / kT_{\text{sun}}} - 1\right)}$$
where:

-   $E$: Photon energy (J),

-   $c$: Speed of light (m/s),

-   $h$: Planck's constant (J s),

-   $T_{\text{sun}}$: Sun's temperature (5778 K),

-   $k$: Boltzmann constant (J/K).

## Absorption of Photons

Photons with energy $E \geq E_g$ (bandgap energy of the material) are
absorbed. The absorbed spectrum is given by:
$$I_{\text{absorbed}}(E) = I(E) \quad \text{for} \quad E \geq E_g$$

## Thermalization Loss

Photons with an energy higher than the band gap ($E > E_g$) lose their
excess energy as heat. The effective photon energy contributing to
electricity is:
$$E_{\text{effective}} = \min(E, E_g) \cdot \eta_{\text{thermalization}}$$
where $\eta_{\text{thermalization}}$ is the thermalization efficiency
(e.g., 80%).

## Generated Power

The generated power $P_{\text{gen}}$ is obtained by integrating the
absorbed photon energy over the spectrum:
$$P_{\text{gen}} = (1 - \eta_{\text{reflection}})(1 - \eta_{\text{recombination}})(1 - \eta_{\text{resistance}}) \int_{E_g}^\infty E_{\text{effective}} I_{\text{absorbed}}(E) \, dE$$
where:

-   $\eta_{\text{reflection}}$: Fractional reflection loss (e.g., 10%),

-   $\eta_{\text{recombination}}$: Fractional recombination loss (e.g.,
    20%),

-   $\eta_{\text{resistance}}$: Fractional resistive loss (e.g., 5%).

## Total Incident Power

The total incident power $P_{\text{total}}$ is the integral of the
entire solar spectrum:
$$P_{\text{total}} = \int_0^\infty E \cdot I(E) \, dE$$

## Practical Efficiency

The practical efficiency $\eta$ is the ratio of generated power to total
incident power: $$\eta = \frac{P_{\text{gen}}}{P_{\text{total}}}$$

## References

1.  Shockley, W., & Queisser, H. J. (1961). \"Detailed Balance Limit of
    Efficiency of p-n Junction Solar Cells.\" *Journal of Applied
    Physics*, 32(3), 510--519. [DOI](https://doi.org/10.1063/1.1736034)

2.  Nelson, J. (2003). *The Physics of Solar Cells*. Imperial College
    Press.

3.  Green, M. A. (1982). \"Solar Cell Fill Factors: General Graph and
    Empirical Expressions.\" *Solid-State Electronics*, 25(11),
    1025--1028.

4.  Knier, G. (2002). \"How Do Solar Cells Work?\" *NASA Science*.
    [Online
    Article](https://science.nasa.gov/astrophysics/focus-areas/how-do-solar-cells-work)

# Project Phases {#project-phases .unnumbered}

## Phase 1: Literature Review {#phase-1-literature-review .unnumbered}

**Topics to cover:**

-   Fundamental principles of silicon photovoltaics, including the
    photoelectric effect and bandgap energy.

-   Spectral absorption properties of silicon and their impact on energy
    conversion.

-   Overview of advanced solar cell designs, including passivated
    emitter rear contact (PERC) cells.

-   Environmental and economic impacts of solar cell technologies.

**Deliverable:** A written summary (2--3 pages) highlighting the
principles of silicon photovoltaics and key advancements.

## Phase 2: Manufacturing Processes {#phase-2-manufacturing-processes .unnumbered}

**Activities:**

-   Study the processes involved in silicon solar cell manufacturing,
    including wafer production, doping, and anti-reflective coatings.

-   Evaluate manufacturing techniques for their impact on efficiency and
    cost.

**Deliverable:** A detailed report on manufacturing processes and their
role in enhancing solar cell performance.

## Phase 3: Simulation and Analysis {#phase-3-simulation-and-analysis .unnumbered}

**Activities:**

-   Use Python to simulate the Shockley-Queisser efficiency limit for
    silicon-based cells.

-   Calculate and visualize efficiency as a function of material
    properties and environmental conditions.

-   Analyze results for solar spectrum utilization and provide
    recommendations for optimizing cell designs.

**Deliverable:** A Python script and accompanying graphs illustrating
the efficiency simulation results.

## Phase 4: Economic and Environmental Analysis {#phase-4-economic-and-environmental-analysis .unnumbered}

**Activities:**

-   Investigate cost trends and government incentives for solar
    technologies.

-   Perform a lifecycle emissions analysis for silicon-based cells.

**Deliverable:** A comparative analysis report detailing economic
feasibility and environmental impacts.

## Phase 5: Report and Presentation {#phase-5-report-and-presentation .unnumbered}

**Final Report:**

-   Abstract and introduction.

-   Literature review summary.

-   Description of manufacturing processes.

-   Results of the Python-based simulation.

-   Economic and environmental analysis.

-   Conclusions and recommendations for improving solar cell designs.

**Presentation:** A 10-minute presentation summarizing the project.

# Key Learning Outcomes {#key-learning-outcomes .unnumbered}

-   Understanding the principles and applications of silicon
    photovoltaics.

-   Hands-on experience with Python for simulating solar cell
    efficiencies.

-   Insights into manufacturing processes and their impact on
    performance and cost.

-   Awareness of the economic and environmental trade-offs in solar
    technology.

# Tools and Resources {#tools-and-resources .unnumbered}

**Python Libraries:**

-   `matplotlib`, `numpy` for analysis and plotting.

-   `pandas` for data handling.

**References:**

-   Books: *Solar Cell Materials* by Tom Markvart.

-   Websites: National Renewable Energy Laboratory (NREL), International
    Renewable Energy Agency (IRENA).

# Potential Extensions {#potential-extensions .unnumbered}

-   Explore tandem or multi-junction solar cell designs.

-   Simulate the impact of temperature variations on solar cell
    efficiency.

-   Evaluate hybrid systems combining silicon cells with perovskite
    layers.

# Grading Rubric for Solar Project {#grading-rubric-for-solar-project .unnumbered}

**Total Points: 100**\
The grading is divided into **Project Report (70 points)** and **Final
Presentation (30 points)**.

## 1. Project Report (70 points) {#project-report-70-points .unnumbered}

The report will be assessed based on the following components:

### A. Literature Review (15 points) {#a.-literature-review-15-points .unnumbered}

-   **Comprehensiveness (10 points)**:

    -   Covers key topics: principles of photovoltaics, spectral
        absorption, and advanced designs.

    -   Properly cites credible references.

-   **Clarity and Structure (5 points)**:

    -   Written clearly and logically, with well-organized sections.

### B. Manufacturing Processes (15 points) {#b.-manufacturing-processes-15-points .unnumbered}

-   **Detail and Accuracy (10 points)**:

    -   Includes detailed descriptions of key manufacturing steps.

    -   Explains their impact on efficiency and cost.

-   **Presentation of Data (5 points)**:

    -   Data is well-organized using tables, graphs, or illustrations.

### C. Python Code and Simulation (20 points) {#c.-python-code-and-simulation-20-points .unnumbered}

-   **Correctness (10 points)**:

    -   Code executes without errors.

    -   Results align with theoretical predictions of the
        Shockley-Queisser limit.

-   **Visualization and Insights (5 points)**:

    -   Provides clear and meaningful graphs of simulation results.

-   **Documentation and Clarity (5 points)**:

    -   Code is well-documented with comments explaining logic.

### D. Economic and Environmental Analysis (10 points) {#d.-economic-and-environmental-analysis-10-points .unnumbered}

-   **Economic Feasibility (5 points)**:

    -   Provides detailed calculations for cost trends and incentives.

-   **Environmental Impact (5 points)**:

    -   Addresses lifecycle emissions and sustainability factors.

### E. Report Quality (5 points) {#e.-report-quality-5-points .unnumbered}

-   **Organization and Flow (3 points)**:

    -   Sections follow a logical order and are interconnected.

-   **Grammar, Style, and Formatting (2 points)**:

    -   Free of major grammatical errors, formatted consistently.

## 2. Final Presentation (30 points) {#final-presentation-30-points .unnumbered}

The presentation will be assessed based on the following components:

### A. Delivery and Communication (10 points) {#a.-delivery-and-communication-10-points .unnumbered}

-   **Clarity and Confidence (5 points)**:

    -   Speakers demonstrate a clear understanding of the project.

    -   Ideas are communicated confidently and concisely.

-   **Audience Engagement (5 points)**:

    -   Visual aids (slides) are effective and engaging.

    -   Team responds effectively to questions.

### B. Content Coverage (15 points) {#b.-content-coverage-15-points .unnumbered}

-   **Introduction and Objectives (5 points)**:

    -   Clearly outlines the project objectives and significance.

-   **Results and Analysis (5 points)**:

    -   Key findings, including efficiency simulation results and
        economic analysis, are presented with graphs or charts.

-   **Conclusion and Recommendations (5 points)**:

    -   Summarizes findings and provides actionable insights.

### C. Time Management (5 points) {#c.-time-management-5-points .unnumbered}

-   Presentation is delivered within the allotted time (e.g., 10
    minutes).

# Grading Summary {#grading-summary .unnumbered}

  **Category**                           **Points**
  ------------------------------------- ------------
  **Project Report**                       **70**
  Literature Review                          15
  Manufacturing Processes                    15
  Python Code and Simulation                 20
  Economic and Environmental Analysis        10
  Report Quality                             5
  **Final Presentation**                   **30**
  Delivery and Communication                 10
  Content Coverage                           15
  Time Management                            5
  **Total**                               **100**

  : Grading Rubric for Silicon-Based Solar Cell Project

# The Organic Rankine Cycle in Renewable Energy

## Project Statement

The Organic Rankine Cycle (ORC) is a crucial technology in the renewable
energy sector, offering a pathway to harness low-grade heat sources for
sustainable power generation. This undergraduate project focuses on
understanding and simulating the ORC, emphasizing its thermodynamic
principles, applications, and environmental benefits. Students will
explore the selection of organic working fluids, analyze real-world
applications such as geothermal and solar power plants, and evaluate the
economic feasibility of ORC systems.

A significant component of the project involves programming in Python to
calculate thermodynamic properties, visualize T-S and H-S diagrams, and
determine efficiency and power flows using tools like CoolProp. In
addition, students will examine the environmental impacts of ORCs,
discussing their role in reducing greenhouse gas emissions and using
waste heat effectively.

The project integrates theoretical knowledge with practical skills,
allowing students to analyze and model energy systems while considering
economic and environmental factors. By the end of this project,
participants will have a comprehensive understanding of ORC technology
and its pivotal role in the advancement of renewable energy solutions.

## Thermodynamics and Selection of Organic Fluids

This section explores the thermodynamic principles of the ORC and the
criteria for selecting working fluids. Key considerations include:

-   Critical temperature and pressure.

-   Thermal stability.

-   Environmental and safety properties.

-   Efficiency impact.

Diagrams of typical organic fluid T-S and P-H plots will be discussed.

## Applications of Organic Rankine Cycle

The ORC is utilized in various renewable energy applications:

-   Geothermal power plants.

-   Solar thermal systems.

-   Biomass power plants.

-   Industrial waste heat recovery.

Real-world examples and case studies will be provided.

## Thermodynamic Equations for Calculating Efficiency and Power Flows

The ORC efficiency and power flows are calculated using fundamental
thermodynamic equations: $$\begin{aligned}
    \eta &= \frac{W_{net}}{Q_{in}} \\
    W_{net} &= W_{turbine} - W_{pump} \\
    Q_{in} &= \dot{m}(h_3 - h_2)
\end{aligned}$$ The derivation of these equations will be detailed along
with assumptions and boundary conditions.

## Python Project for Efficiency and Power Flows in an ORC

This section outlines a Python-based project to model and simulate the
ORC. Students will:

1.  Input parameters: working fluid, heat source temperature, and
    pressure.

2.  Calculate thermodynamic properties using `CoolProp`.

3.  Plot T-S and H-S diagrams for the cycle.

4.  Compute the efficiency and net power output.

An example Python script will be included.

## Economics of Typical ORCs

The economic feasibility of ORCs is examined, considering:

-   Capital costs.

-   Operating and maintenance costs.

-   Payback period.

-   Economic incentives and subsidies.

Case studies from commercial ORC installations will be analyzed.

## Environmental Impact of ORC

The environmental benefits of ORCs include:

-   Reduction in greenhouse gas emissions.

-   Utilization of renewable and waste heat sources.

-   Minimal environmental footprint of organic fluids.

The potential environmental hazards of organic fluids will also be
discussed.

## Conclusions

This section summarizes the role of the ORC in renewable energy,
highlighting its advantages, challenges, and future prospects.

# Project Phases {#project-phases-1 .unnumbered}

## Phase 1: Literature Review {#phase-1-literature-review-1 .unnumbered}

**Topics to cover:**

-   Fundamental principles of the Organic Rankine Cycle, including
    thermodynamic properties and processes.

-   Selection criteria for organic working fluids (e.g., thermal
    stability, efficiency, environmental impact).

-   Real-world applications in geothermal, solar power, and waste heat
    recovery.

-   Environmental and economic impacts of ORC technology.

**Deliverable:** A written summary (2--3 pages) highlighting the
principles, applications, and benefits of ORC technology.

## Phase 2: Simulation and Thermodynamic Analysis {#phase-2-simulation-and-thermodynamic-analysis .unnumbered}

**Activities:**

-   Use Python and CoolProp to calculate thermodynamic properties of
    organic fluids.

-   Plot T-S and H-S diagrams to visualize the ORC cycle.

-   Determine efficiency and power flows based on input conditions and
    working fluid properties.

**Deliverable:** A Python script and accompanying graphs illustrating
the ORC cycle and efficiency calculations.

## Phase 3: Economic Feasibility Study {#phase-3-economic-feasibility-study .unnumbered}

**Activities:**

-   Perform a cost-benefit analysis of ORC systems, considering capital
    costs, maintenance, and operating expenses.

-   Evaluate economic feasibility based on payback periods and energy
    cost savings.

**Deliverable:** A report detailing the economic analysis of ORC
systems.

## Phase 4: Environmental Impact Analysis {#phase-4-environmental-impact-analysis .unnumbered}

**Activities:**

-   Assess greenhouse gas emission reductions through ORC
    implementation.

-   Evaluate the role of ORCs in effective waste heat utilization.

**Deliverable:** A comparative report on the environmental benefits and
challenges of ORC technology.

## Phase 5: Report and Presentation {#phase-5-report-and-presentation-1 .unnumbered}

**Final Report:**

-   Abstract and introduction.

-   Literature review summary.

-   Results of thermodynamic simulations and efficiency calculations.

-   Economic and environmental analysis.

-   Conclusions and recommendations for optimizing ORC systems.

**Presentation:** A 10-minute presentation summarizing the project.

# Key Learning Outcomes {#key-learning-outcomes-1 .unnumbered}

-   Understanding the principles and applications of ORC technology.

-   Hands-on experience with Python for thermodynamic modeling and
    visualization.

-   Insights into the economic and environmental trade-offs of ORC
    systems.

-   Development of skills in analyzing and designing renewable energy
    systems.

# Tools and Resources {#tools-and-resources-1 .unnumbered}

**Python Libraries:**

-   `matplotlib`, `numpy` for analysis and plotting.

-   `CoolProp` for thermodynamic property calculations.

-   `pandas` for data handling.

**References:**

-   Books: *Organic Rankine Cycle Technology for Energy Recovery* by
    Ennio Macchi.

-   Websites: National Renewable Energy Laboratory (NREL), International
    Renewable Energy Agency (IRENA).

# Potential Extensions {#potential-extensions-1 .unnumbered}

-   Simulate hybrid ORC systems combining geothermal and solar heat
    sources.

-   Explore the impact of superheating and regenerative cycles on ORC
    efficiency.

-   Assess the feasibility of novel working fluids with low global
    warming potential (GWP).

# Grading Rubric for ORC Project {#grading-rubric-for-orc-project .unnumbered}

**Total Points: 100**\
The grading is divided into **Project Report (70 points)** and **Final
Presentation (30 points)**.

## 1. Project Report (70 points) {#project-report-70-points-1 .unnumbered}

The report will be assessed based on the following components:

### A. Literature Review (15 points) {#a.-literature-review-15-points-1 .unnumbered}

-   **Comprehensiveness (10 points)**:

    -   Covers key topics: ORC principles, fluid selection, and
        real-world applications.

    -   Properly cites credible references.

-   **Clarity and Structure (5 points)**:

    -   Written clearly and logically, with well-organized sections.

### B. Thermodynamic Simulation (20 points) {#b.-thermodynamic-simulation-20-points .unnumbered}

-   **Correctness (10 points)**:

    -   Code executes without errors and produces accurate results.

    -   Results align with thermodynamic principles.

-   **Visualization and Insights (5 points)**:

    -   Provides clear and meaningful graphs of T-S and H-S diagrams.

-   **Documentation and Clarity (5 points)**:

    -   Code is well-documented with comments explaining logic.

### C. Economic Feasibility (15 points) {#c.-economic-feasibility-15-points .unnumbered}

-   **Detail and Accuracy (10 points)**:

    -   Includes detailed cost-benefit analysis.

    -   Explains economic feasibility based on payback period and energy
        cost savings.

-   **Clarity (5 points)**:

    -   Results are presented clearly, using tables or graphs where
        appropriate.

### D. Environmental Analysis (10 points) {#d.-environmental-analysis-10-points .unnumbered}

-   **Impact Assessment (5 points)**:

    -   Effectively evaluates greenhouse gas emission reductions.

-   **Sustainability Insights (5 points)**:

    -   Discusses the role of ORCs in sustainable energy systems.

### E. Report Quality (10 points) {#e.-report-quality-10-points .unnumbered}

-   **Organization and Flow (5 points)**:

    -   Sections follow a logical order and are interconnected.

-   **Grammar, Style, and Formatting (5 points)**:

    -   Free of major grammatical errors, formatted consistently.

## 2. Final Presentation (30 points) {#final-presentation-30-points-1 .unnumbered}

The presentation will be assessed based on the following components:

### A. Delivery and Communication (10 points) {#a.-delivery-and-communication-10-points-1 .unnumbered}

-   **Clarity and Confidence (5 points)**:

    -   Speakers demonstrate a clear understanding of the project.

    -   Ideas are communicated confidently and concisely.

-   **Audience Engagement (5 points)**:

    -   Visual aids (slides) are effective and engaging.

    -   Team responds effectively to questions.

### B. Content Coverage (15 points) {#b.-content-coverage-15-points-1 .unnumbered}

-   **Introduction and Objectives (5 points)**:

    -   Clearly outlines the project objectives and significance.

-   **Results and Analysis (5 points)**:

    -   Key findings, including thermodynamic simulations and economic
        analysis, are presented with graphs or charts.

-   **Conclusion and Recommendations (5 points)**:

    -   Summarizes findings and provides actionable insights.

### C. Time Management (5 points) {#c.-time-management-5-points-1 .unnumbered}

-   Presentation is delivered within the allotted time (e.g., 10
    minutes).

  **Category**                  **Points**
  ---------------------------- ------------
  **Project Report**              **70**
  Literature Review                 15
  Thermodynamic Simulation          20
  Economic Feasibility              15
  Environmental Analysis            10
  Report Quality                    10
  **Final Presentation**          **30**
  Delivery and Communication        10
  Content Coverage                  15
  Time Management                   5
  **Total**                      **100**

  : Grading Rubric for Organic Rankine Cycle (ORC) Project

# Design and Analysis of a Small-Scale Hydroelectric Power Plant Using Python

The goal of this project is to provide students with a comprehensive
understanding of hydroelectric power generation. The project will
involve:

-   Review of the literature on hydro power systems and their
    environmental and economic impacts.

-   Data collection and analysis of site-specific conditions for hydro
    plant design (e.g., head, flow rate, and turbine selection).

-   Development or use of Python code for plant design and performance
    analysis.

-   An evaluation of the feasibility and sustainability of the proposed
    design.

-   Preparation of a detailed project report documenting the findings,
    methodology, and conclusions.

## Project Phases

## Phase 1: Literature Review {#phase-1-literature-review-2 .unnumbered}

**Topics to cover:**

-   Types of hydro power plants (run-of-river, storage, pumped storage).

-   Key components: dams, turbines, generators, and penstocks.

-   Environmental and social impacts of hydro projects.

-   Current advancements in turbine technology and small-scale hydro
    systems.

**Deliverable:** A written summary (2--3 pages) highlighting the
importance of hydro power, key design considerations, and its role in
renewable energy.

## Phase 2: Site Analysis {#phase-2-site-analysis .unnumbered}

**Activities:**

-   Select or assume a hypothetical or real site for the hydro plant.

-   Research or assume site-specific parameters like river flow rates
    (Q), available head (H), and seasonal variations.

-   Evaluate potential turbine types based on head and flow rate ranges.

**Deliverable:** A dataset summarizing head, flow, and seasonal
variations, along with the rationale for selecting a particular turbine
type.

## Phase 3: Design and Simulation {#phase-3-design-and-simulation .unnumbered}

**Activities:**

-   Use Python code to:

    -   Calculate the power output for different flow rates and head
        values.

    -   Perform economic analysis, including capital cost, annual
        revenue, and payback period.

    -   Simulate seasonal variability in power output.

-   Extend the code to include:

    -   Additional parameters like penstock friction losses or turbine
        efficiency curves.

    -   Optimization of power output and cost.

**Deliverable:** A Python script that models the power plant and
generates useful visualizations (e.g., power vs. flow rate, seasonal
output, and cost breakdown).

## Phase 4: Comparative Analysis {#phase-4-comparative-analysis .unnumbered}

**Activities:**

-   Compare the design with a real-world small-scale hydro plant or a
    case study.

-   Evaluate how variations in assumptions (e.g., turbine efficiency or
    head) impact power generation and economic viability.

**Deliverable:** A 1--2 page comparison report with graphs and key
insights.

## Phase 5: Report and Presentation {#phase-5-report-and-presentation-2 .unnumbered}

**Final Report:**

-   Abstract and introduction.

-   Literature review summary.

-   Methodology for site selection and design.

-   Results of power and economic analysis, with visualizations.

-   Conclusions and recommendations for improving plant performance.

**Presentation:** A 10-minute presentation summarizing the project.

## Key Learning Outcomes

-   Understanding the fundamentals of hydroelectric power generation.

-   Hands-on experience with Python for engineering design and analysis.

-   Insights into the trade-offs between cost, efficiency, and
    environmental impacts in energy projects.

-   Development of technical reporting and communication skills.

## Tools and Resources

**Python Libraries:**

-   `matplotlib`, `numpy` for analysis and plotting.

-   Optional: `pandas` for data handling.

**Data Sources:**

-   Open datasets for river flow rates (e.g., USGS streamflow data).

-   Case studies from organizations like the International Hydropower
    Association (IHA).

**References:**

-   Books: *Hydropower Engineering Handbook* by C. S. Gupta.

-   Websites: International Renewable Energy Agency (IRENA), IHA.

## Potential Extensions

-   Incorporate environmental impact analysis using Python.

-   Simulate pumped storage systems with energy storage cycles.

-   Evaluate hybrid systems combining hydro with solar or wind.

# Grading Rubric for Hydropower Project {#grading-rubric-for-hydropower-project .unnumbered}

**Total Points: 100**\
The grading is divided into **Project Report (70 points)** and **Final
Presentation (30 points)**.

# 1. Project Report (70 points) {#project-report-70-points-2 .unnumbered}

The report will be assessed based on the following components:

## A. Literature Review (15 points) {#a.-literature-review-15-points-2 .unnumbered}

-   **Comprehensiveness (10 points)**:

    -   Covers key topics: types of hydro power plants, turbines,
        environmental/economic impacts.

    -   Properly cites credible references.

-   **Clarity and Structure (5 points)**:

    -   Written clearly and logically, with well-organized sections.

## B. Site Analysis (15 points) {#b.-site-analysis-15-points .unnumbered}

-   **Data Quality (10 points)**:

    -   Includes relevant site-specific parameters (head, flow rate,
        seasonal variations).

    -   Provides rationale for turbine selection with reference to
        technical specifications.

-   **Presentation of Data (5 points)**:

    -   Data is well-organized using tables, graphs, or charts.

## C. Python Code and Simulation (20 points) {#c.-python-code-and-simulation-20-points-1 .unnumbered}

-   **Correctness (10 points)**:

    -   Code executes without errors.

    -   Results align with input parameters and hydro power
        calculations.

-   **Extension and Innovation (5 points)**:

    -   Includes extensions like efficiency curves, friction losses, or
        other enhancements.

-   **Documentation and Clarity (5 points)**:

    -   Code is well-documented with comments explaining logic.

## D. Economic and Environmental Analysis (10 points) {#d.-economic-and-environmental-analysis-10-points-1 .unnumbered}

-   **Economic Viability (5 points)**:

    -   Provides detailed calculations for capital cost, revenue, and
        payback period.

-   **Environmental Impact (5 points)**:

    -   Addresses potential environmental trade-offs or sustainability
        factors.

## E. Comparative Analysis (5 points) {#e.-comparative-analysis-5-points .unnumbered}

-   **Depth of Comparison (3 points)**:

    -   Effectively compares the design with a real-world case study or
        benchmarks.

-   **Insights and Recommendations (2 points)**:

    -   Provides meaningful conclusions based on the comparison.

## F. Report Quality (5 points) {#f.-report-quality-5-points .unnumbered}

-   **Organization and Flow (3 points)**:

    -   Sections follow a logical order and are interconnected.

-   **Grammar, Style, and Formatting (2 points)**:

    -   Free of major grammatical errors, formatted consistently.

# 2. Final Presentation (30 points) {#final-presentation-30-points-2 .unnumbered}

The presentation will be assessed based on the following components:

## A. Delivery and Communication (10 points) {#a.-delivery-and-communication-10-points-2 .unnumbered}

-   **Clarity and Confidence (5 points)**:

    -   Speakers demonstrate a clear understanding of the project.

    -   Ideas are communicated confidently and concisely.

-   **Audience Engagement (5 points)**:

    -   Visual aids (slides) are effective and engaging.

    -   Team responds effectively to questions.

## B. Content Coverage (15 points) {#b.-content-coverage-15-points-2 .unnumbered}

-   **Introduction and Objectives (5 points)**:

    -   Clearly outlines the project objectives and significance.

-   **Results and Analysis (5 points)**:

    -   Key findings, including power output, economic analysis, and
        seasonal variability, are presented with graphs or charts.

-   **Conclusion and Recommendations (5 points)**:

    -   Summarizes findings and provides actionable insights.

## C. Time Management (5 points) {#c.-time-management-5-points-2 .unnumbered}

-   Presentation is delivered within the allotted time (e.g., 10
    minutes).

# Grading Summary {#grading-summary-1 .unnumbered}

  **Category**                           **Points**
  ------------------------------------- ------------
  **Project Report**                       **70**
  Literature Review                          15
  Site Analysis                              15
  Python Code and Simulation                 20
  Economic and Environmental Analysis        10
  Comparative Analysis                       5
  Report Quality                             5
  **Final Presentation**                   **30**
  Delivery and Communication                 10
  Content Coverage                           15
  Time Management                            5
  **Total**                               **100**

  : Grading Rubric for Hydropower Project

# Appendix: Python code for a single solar cell efficiency simulator

``` {style="custompython" caption="Python Code for Solar Cell Efficiency Simulator"}
import numpy as np
import matplotlib.pyplot as plt
from scipy.constants import h, c, k

# Constants
q = 1.602e-19  # Elementary charge (C)
hc = h * c  # Planck's constant times the speed of light (J*m)
T_sun = 5778  # Sun's temperature (K)
kT_sun = k * T_sun

# Reasonable Loss Parameters
reflection_loss = 0.1  # 10% of sunlight is reflected
recombination_loss = 0.2  # 20% of generated carriers are lost
resistive_loss = 0.05  # 5% of power is lost due to resistance
thermalization_efficiency = 0.8  # 80% efficiency for photons above bandgap

# Functions
def solar_spectrum(E_photon):
    spectrum = (2 * np.pi * c**2 * E_photon**3) / ((hc)**3 * (np.exp(E_photon / kT_sun) - 1))
    return spectrum

def calculate_efficiency(E_g, E_photon, spectrum):
    absorbed = E_photon >= E_g
    absorbed_spectrum = spectrum[absorbed]
    absorbed_energy = E_photon[absorbed]
    effective_energy = np.minimum(absorbed_energy, E_g) * thermalization_efficiency
    power_generated = np.trapz(effective_energy * absorbed_spectrum, x=E_photon[absorbed])
    power_generated *= (1 - reflection_loss) * (1 - recombination_loss) * (1 - resistive_loss)
    total_power = np.trapz(E_photon * spectrum, x=E_photon)
    efficiency = power_generated / total_power
    return efficiency

E_photon = np.linspace(0.1, 4, 1000) * q
spectrum = solar_spectrum(E_photon)
E_g = 1.1 * q
efficiency = calculate_efficiency(E_g, E_photon, spectrum)
print(f"Practical Efficiency with Losses: {efficiency * 100:.2f}%")

plt.figure(figsize=(10, 6))
plt.plot(E_photon / q, spectrum, label="Solar Spectrum (AM1.5)")
plt.axvline(E_g / q, color="r", linestyle="--", label=f"Bandgap Energy (E_g = {E_g / q:.2f} eV)")
plt.fill_between(E_photon / q, spectrum, where=(E_photon >= E_g), alpha=0.3, label="Absorbed Spectrum")
plt.title("Solar Spectrum and Absorption with Losses")
plt.xlabel("Photon Energy (eV)")
plt.ylabel("Spectral Intensity")
plt.legend()
plt.grid()
plt.show()
```

# Appendix: Python code for a multi-junction solar cell efficiency simulator

``` {style="custompython" caption="Python Code for Solar Cell Efficiency Simulator"}
import numpy as np
import matplotlib.pyplot as plt
from scipy.constants import h, c, k

# Constants
q = 1.602e-19  # Elementary charge (C)
hc = h * c  # Planck's constant times the speed of light (J*m)

# Solar spectrum (AM1.5)
def solar_spectrum(E_photon):
    T_sun = 5778  # Sun's temperature (K)
    kT_sun = k * T_sun
    spectrum = (2 * np.pi * c**2 * E_photon**3) / ((hc)**3 * (np.exp(E_photon / kT_sun) - 1))
    return spectrum

# Absorption calculation
def absorption(alpha, d, E_photon):
    return 1 - np.exp(-alpha * d)

# Layer-by-layer absorption and power contribution
def layer_efficiency(E_g, alpha, d, E_photon, transmitted_spectrum):
    absorbed = absorption(alpha, d, E_photon)
    usable_photons = (E_photon >= E_g)
    effective_energy = np.minimum(E_photon, E_g) * absorbed * usable_photons
    layer_power = np.trapz(effective_energy * transmitted_spectrum, x=E_photon)
    
    # Reduce transmitted spectrum for subsequent layers
    remaining_spectrum = transmitted_spectrum * (1 - absorbed)
    return layer_power, remaining_spectrum

# Total efficiency function
def total_efficiency(layers, E_photon, spectrum):
    transmitted_spectrum = spectrum  # Start with full spectrum
    total_power = 0
    incident_power = np.trapz(E_photon * spectrum, x=E_photon)  # Total incident power
    for layer in layers:
        E_g, alpha, d = layer
        layer_power, transmitted_spectrum = layer_efficiency(E_g, alpha, d, E_photon, transmitted_spectrum)
        total_power += layer_power
    return total_power / incident_power

# Efficiency with loss mechanisms
def practical_efficiency(layers, E_photon, spectrum, losses):
    transmitted_spectrum = spectrum  # Start with full spectrum
    total_power = 0
    incident_power = np.trapz(E_photon * spectrum, x=E_photon)  # Total incident power
    for layer in layers:
        E_g, alpha, d = layer
        layer_power, transmitted_spectrum = layer_efficiency(E_g, alpha, d, E_photon, transmitted_spectrum)
        
        # Apply loss mechanisms
        layer_power *= (1 - losses['reflection']) * (1 - losses['thermalization']) * (1 - losses['recombination'])
        total_power += layer_power
    return total_power / incident_power

# Material and layer properties
layers = [
    # Example: [Bandgap (J), Absorption coefficient (1/m), Thickness (m)]
    [1.85 * q, 1e7, 1e-6],  # Layer 1: GaInP2
    [1.424 * q, 1e7, 2e-6],  # Layer 2: GaAs
    [0.66 * q, 1e6, 3e-6],  # Layer 3: Ge
]

# Photon energy range (in Joules)
E_photon = np.linspace(0.1, 4, 1000) * q
spectrum = solar_spectrum(E_photon)

# Ideal efficiency
ideal_efficiency = total_efficiency(layers, E_photon, spectrum)
print(f"Ideal Efficiency: {ideal_efficiency * 100:.2f}%")

# Loss mechanisms
losses = {
    'reflection': 0.1,  # 10% reflection loss
    'thermalization': 0.2,  # 20% thermalization loss
    'recombination': 0.15,  # 15% recombination loss
}

# Practical efficiency
practical_efficiency_value = practical_efficiency(layers, E_photon, spectrum, losses)
print(f"Practical Efficiency: {practical_efficiency_value * 100:.2f}%")

# Plot individual graphs for each layer
for i, layer in enumerate(layers):
    E_g, alpha, d = layer
    absorption_curve = absorption(alpha, d, E_photon)
    absorbed_spectrum = absorption_curve * spectrum
    
    # Shade only the portion above the bandgap
    mask = E_photon >= E_g
    absorbed_spectrum_above_bandgap = absorbed_spectrum * mask

    plt.figure(figsize=(10, 6))
    plt.plot(E_photon / q, spectrum, label="Solar Spectrum (AM1.5)", color="black")
    plt.fill_between(E_photon / q, absorbed_spectrum_above_bandgap, color=f"C{i}", alpha=0.3, label=f"Layer {i+1} Absorbed")
    plt.axvline(E_g / q, color=f"C{i}", linestyle="--", label=f"Layer {i+1} Bandgap {E_g / q:.2f} eV")

    plt.title(f"Absorption for Layer {i+1}")
    plt.xlabel("Photon Energy (eV)")
    plt.ylabel("Spectral Intensity (arbitrary units)")
    plt.legend()
    plt.grid()
    plt.show()
```

# Python code for thermodynamic properties of R134a

``` {style="custompython" caption="Python code for thermodynamic properties of R134a"}
from CoolProp.CoolProp import PropsSI

def r134a_table_examples():
    """
    Examples for calculating R134a properties using CoolProp, covering:
    1. General R134a properties.
    2. Superheated state: Given temperature and pressure, find all properties.
    3. Saturation region: Given entropy and pressure, find the refrigerant quality (x).
    4. Saturation region: Given entropy and pressure, find properties.
    5. Liquid state: Given pressure and x=0, find all properties.
    6. Liquid state: Given pressure and entropy, find all properties.
    """

    # (1) General R134a Properties: Given P & T
    print("(1) General R134a Properties")
    pressure = 500000  # Pa (5 bar)
    temperature = 300  # K (27°C)
    print(f"Pressure: {pressure / 1000:.2f} kPa, Temperature: {temperature - 273.15:.2f} °C")
    print(f"Specific Enthalpy: {PropsSI('H', 'P', pressure, 'T', temperature, 'R134a') / 1000:.2f} kJ/kg")
    print(f"Specific Entropy: {PropsSI('S', 'P', pressure, 'T', temperature, 'R134a'):.4f} J/kg.K\n")

    # (2) Superheated State: Given T & P, find all properties
    print("(2) Superheated State")
    pressure = 600000  # Pa (6 bar)
    temperature = 40 + 273.15  # K (40°C)
    print(f"Pressure: {pressure / 1000:.2f} kPa, Temperature: {temperature - 273.15:.2f} °C")
    print(f"Specific Enthalpy: {PropsSI('H', 'P', pressure, 'T', temperature, 'R134a') / 1000:.2f} kJ/kg")
    print(f"Specific Entropy: {PropsSI('S', 'P', pressure, 'T', temperature, 'R134a'):.4f} J/kg.K\n")

    # (3) Saturation Region: Given S & P, find quality (x)
    print("(3) Saturation Region: Find Quality (x)")
    pressure = 200000  # Pa (2 bar)
    entropy_liquid = PropsSI('S', 'P', pressure, 'Q', 0, 'R134a')  # Saturated liquid entropy
    entropy_vapor = PropsSI('S', 'P', pressure, 'Q', 1, 'R134a')  # Saturated vapor entropy
    entropy = entropy_liquid + 0.5 * (entropy_vapor - entropy_liquid)  # Ensure quality < 1 (e.g., 0.5)
    quality = (entropy - entropy_liquid) / (entropy_vapor - entropy_liquid)  # Quality calculation
    print(f"Pressure: {pressure / 1000:.2f} kPa, Entropy: {entropy / 1000:.2f} kJ/kg.K")
    print(f"Quality (x): {quality:.4f}\n")

    # (4) Saturation Region: Given S & P, find properties
    print("(4) Saturation Region: Find Properties")
    enthalpy_liquid = PropsSI('H', 'P', pressure, 'Q', 0, 'R134a')  # Saturated liquid enthalpy
    enthalpy_vapor = PropsSI('H', 'P', pressure, 'Q', 1, 'R134a')  # Saturated vapor enthalpy
    enthalpy = enthalpy_liquid + quality * (enthalpy_vapor - enthalpy_liquid)  # Enthalpy for quality
    print(f"Pressure: {pressure / 1000:.2f} kPa")
    print(f"Entropy: {entropy / 1000:.2f} kJ/kg.K, Quality (x): {quality:.2f}")
    print(f"Enthalpy: {enthalpy / 1000:.2f} kJ/kg\n")

    # (5) Liquid State: Given P & x=0, find all properties
    print("(5) Liquid State: Find All Properties")
    pressure = 400000  # Pa (4 bar)
    print(f"Pressure: {pressure / 1000:.2f} kPa")
    print(f"Saturated Liquid Enthalpy: {PropsSI('H', 'P', pressure, 'Q', 0, 'R134a') / 1000:.2f} kJ/kg")
    print(f"Saturated Liquid Density: {PropsSI('D', 'P', pressure, 'Q', 0, 'R134a'):.2f} kg/m^3\n")

    # (6) Liquid State: Given P & S, find all properties
    print("(6) Liquid State: Find Properties")
    pressure = 300000  # Pa (3 bar)
    entropy = 1.0  # kJ/kg.K
    temperature = PropsSI('T', 'P', pressure, 'S', entropy * 1000, 'R134a')  # Temperature from S & P
    print(f"Pressure: {pressure / 1000:.2f} kPa, Entropy: {entropy:.2f} kJ/kg.K")
    print(f"Temperature: {temperature - 273.15:.2f} °C")
    print(f"Enthalpy: {PropsSI('H', 'P', pressure, 'S', entropy * 1000, 'R134a') / 1000:.2f} kJ/kg")
    print(f"Density: {PropsSI('D', 'P', pressure, 'S', entropy * 1000, 'R134a'):.2f} kg/m^3\n")

# Call the function to run all examples
r134a_table_examples()
```

# Appendix: Python code for the Ideal Rankine Cycle

``` {style="custompython" caption="Python code for the Ideal Rankine Cycle"}
from CoolProp.CoolProp import PropsSI
import matplotlib.pyplot as plt
import numpy as np

def rankine_cycle_analysis():
    """
    Perform calculations for the ideal Rankine cycle, including:
    1. Specific work of turbine and pump.
    2. Heat added (qin) and rejected (qout).
    3. Net work (wnet) and thermal efficiency (eta).
    Generate T-S and H-S diagrams with saturation dome and cycle curves.
    """

    # Define state points (pressures in Pa, temperatures in K)
    P1 = 100000  # Condenser pressure (Pa)
    P2 = 5000000  # Boiler pressure (Pa)
    T3 = 773.15  # Turbine inlet temperature (K)
    Pcrit = 22e6
    dome_p2 = Pcrit
    dome_p1 = 1e4
    # State 1: Saturated liquid at P1
    h1 = PropsSI('H', 'P', P1, 'Q', 0, 'Water')  # Enthalpy (J/kg)
    s1 = PropsSI('S', 'P', P1, 'Q', 0, 'Water')  # Entropy (J/kg.K)

    # State 2: Compressed liquid (isentropic process)
    s2 = s1  # Isentropic process
    h2 = PropsSI('H', 'P', P2, 'S', s2, 'Water')
    T2 = PropsSI('T', 'P', P2, 'S', s2, 'Water')

    # State 2_prime: Saturated liquid at P2
    h2_prime = PropsSI('H', 'P', P2, 'Q', 0, 'Water')
    s2_prime = PropsSI('S', 'P', P2, 'Q', 0, 'Water')

    # State 3: Superheated vapor
    h3 = PropsSI('H', 'P', P2, 'Q', 1,  'Water')  # Enthalpy (J/kg)
    s3 = PropsSI('S', 'P', P2, 'Q', 1, 'Water')

    # State 4: Saturated mixture (isentropic expansion)
    s4 = s3  # Isentropic process
    h4 = PropsSI('H', 'P', P1, 'S', s4, 'Water')

    # Work and heat calculations
    wturb = h3 - h4  # Work done by the turbine (J/kg)
    wpump = h2 - h1  # Work done by the pump (J/kg)
    qin = h3 - h2  # Heat added in the boiler (J/kg)
    qout = h1 - h4  # Heat rejected in the condenser (J/kg)

    # Net work and thermal efficiency
    wnet = wturb - wpump  # Net work (J/kg)
    eta = wnet / qin  # Thermal efficiency

    # Display results
    print("Rankine Cycle Analysis")
    print(f"State 1: h1 = {h1 / 1000:.2f} kJ/kg, s1 = {s1 / 1000:.4f} kJ/kg.K")
    print(f"State 2: h2 = {h2 / 1000:.2f} kJ/kg, s2 = {s2 / 1000:.4f} kJ/kg.K, T2 = {T2 - 273.15:.2f} °C")
    print(f"State 2_prime: h2_prime = {h2_prime / 1000:.2f} kJ/kg, s2_prime = {s2_prime / 1000:.4f} kJ/kg.K")
    print(f"State 3: h3 = {h3 / 1000:.2f} kJ/kg, s3 = {s3 / 1000:.4f} kJ/kg.K")
    print(f"State 4: h4 = {h4 / 1000:.2f} kJ/kg, s4 = {s4 / 1000:.4f} kJ/kg.K")
    print(f"Turbine Work (wturb): {wturb / 1000:.2f} kJ/kg")
    print(f"Pump Work (wpump): {wpump / 1000:.2f} kJ/kg")
    print(f"Heat Added (qin): {qin / 1000:.2f} kJ/kg")
    print(f"Heat Rejected (qout): {qout / 1000:.2f} kJ/kg")
    print(f"Net Work (wnet): {wnet / 1000:.2f} kJ/kg")
    print(f"Thermal Efficiency (eta): {eta * 100:.2f}%")

    # Generate T-S Diagram
    s_sat_liquid = []
    t_sat_liquid = []
    s_sat_vapor = []
    t_sat_vapor = []

    for p in np.logspace(np.log10(dome_p1), np.log10(dome_p2), 200):
        s_sat_liquid.append(PropsSI('S', 'P', p, 'Q', 0, 'Water'))
        t_sat_liquid.append(PropsSI('T', 'P', p, 'Q', 0, 'Water'))
        s_sat_vapor.append(PropsSI('S', 'P', p, 'Q', 1, 'Water'))
        t_sat_vapor.append(PropsSI('T', 'P', p, 'Q', 1, 'Water'))

    plt.figure()
    # Saturation dome
    plt.plot([s / 1000 for s in s_sat_liquid], [t - 273.15 for t in t_sat_liquid], label="Saturation Liquid", linestyle="-", linewidth=1)
    plt.plot([s / 1000 for s in s_sat_vapor], [t - 273.15 for t in t_sat_vapor], label="Saturation Vapor", linestyle="-", linewidth=1)

    # Cycle curve
    cycle_s = [s1, s2, s2_prime, s3, s4, s1]
    cycle_t = [PropsSI('T', 'P', P1, 'Q', 0, 'Water') - 273.15, T2 - 273.15, PropsSI('T', 'P', P2, 'Q', 0, 'Water') - 273.15,
               PropsSI('T', 'P', P2, 'Q', 1, 'Water') - 273.15, PropsSI('T', 'P', P1, 'Q', 0, 'Water') - 273.15, PropsSI('T', 'P', P1, 'Q', 0, 'Water') - 273.15]
    plt.plot([s / 1000 for s in cycle_s], cycle_t, label="Cycle", linewidth=2, color="red")

    # Label states
    for i, (s, t) in enumerate(zip(cycle_s, cycle_t), start=1):
        plt.text(s / 1000, t, f"State {i}", fontsize=8)

    plt.xlabel("Entropy (kJ/kg.K)")
    plt.ylabel("Temperature (°C)")
    plt.title("Rankine Cycle T-S Diagram")
    ylim = 500
    plt.legend()
    plt.grid()
    plt.show()

    # Generate H-S Diagram (Mollier Diagram)
    h_sat_liquid = []
    s_sat_liquid = []
    h_sat_vapor = []
    s_sat_vapor = []

    for p in np.logspace(np.log10(dome_p1), np.log10(dome_p2), 500):
        h_sat_liquid.append(PropsSI('H', 'P', p, 'Q', 0, 'Water'))
        s_sat_liquid.append(PropsSI('S', 'P', p, 'Q', 0, 'Water'))
        h_sat_vapor.append(PropsSI('H', 'P', p, 'Q', 1, 'Water'))
        s_sat_vapor.append(PropsSI('S', 'P', p, 'Q', 1, 'Water'))

    plt.figure()
    # Saturation dome
    plt.plot([s / 1000 for s in s_sat_liquid], [h / 1000 for h in h_sat_liquid], label="Saturation Liquid", linestyle="-", linewidth=1)
    plt.plot([s / 1000 for s in s_sat_vapor], [h / 1000 for h in h_sat_vapor], label="Saturation Vapor", linestyle="-", linewidth=1)

    # Cycle curve
    cycle_h = [h1, h2, h2_prime, h3, h4, h1]
    cycle_s = [s1, s2, s2_prime, s3, s4, s1]
    plt.plot([s / 1000 for s in cycle_s], [h / 1000 for h in cycle_h], label="Cycle", linewidth=2, color="red")

    # Label states
    for i, (s, h) in enumerate(zip(cycle_s, cycle_h), start=1):
        plt.text(s / 1000, h / 1000, f"State {i}", fontsize=8)

    plt.xlabel("Entropy (kJ/kg.K)")
    plt.ylabel("Enthalpy (kJ/kg)")
    plt.title("Rankine Cycle H-S Diagram (Mollier Diagram)")
    plt.legend()
    plt.grid()
    plt.show()

rankine_cycle_analysis()
```

# Appendix: Design of a Hydro Power Plant

``` {style="custompython" caption="Python Code for Design of a Hydro Power Plant"}
import numpy as np
import matplotlib.pyplot as plt

# Constants
g = 9.81  # Gravitational acceleration (m/s^2)
rho = 1000  # Water density (kg/m^3)

# User Inputs
head = 50  # Net head in meters
flow_rate = 20  # Flow rate in cubic meters per second (m^3/s)
efficiency = 0.9  # Efficiency of the turbine (fraction, e.g., 90%)

# Function to calculate power
def calculate_power(flow_rate, head, efficiency):
    """
    Calculate the power output of a hydroelectric power plant.
    :param flow_rate: Flow rate (m^3/s)
    :param head: Head (m)
    :param efficiency: Turbine efficiency (fraction)
    :return: Power (kW)
    """
    power = efficiency * rho * g * flow_rate * head
    return power / 1000  # Convert to kW

# Turbine Selection
turbine_types = {
    "Pelton": {"head_range": (50, 1000), "flow_range": (1, 10)},
    "Francis": {"head_range": (10, 300), "flow_range": (5, 50)},
    "Kaplan": {"head_range": (2, 20), "flow_range": (10, 100)},
}

def select_turbine(head, flow_rate):
    """
    Select a suitable turbine based on head and flow rate.
    """
    for turbine, specs in turbine_types.items():
        if specs["head_range"][0] <= head <= specs["head_range"][1] and specs["flow_range"][0] <= flow_rate <= specs["flow_range"][1]:
            return turbine
    return "No suitable turbine found"

# Economic Analysis
def economic_analysis(power_output, cost_per_kw=1500, electricity_price=0.1):
    """
    Calculate capital cost, annual revenue, and payback period.
    :param power_output: Power output (kW)
    :param cost_per_kw: Capital cost per kW ($)
    :param electricity_price: Price per kWh ($/kWh)
    :return: Capital cost, annual revenue, payback period (years)
    """
    capital_cost = power_output * cost_per_kw
    annual_revenue = power_output * 8760 * electricity_price  # 8760 hours/year
    payback_period = capital_cost / annual_revenue
    return capital_cost, annual_revenue, payback_period

# Seasonal Variability
def seasonal_variability(head, flow_rate, months):
    """
    Simulate power output over months with variable flow rates.
    :param head: Head (m)
    :param flow_rate: Average flow rate (m^3/s)
    :param months: List of monthly flow rate factors (e.g., [0.8, 1.2, ...])
    :return: List of monthly power outputs (kW)
    """
    monthly_powers = []
    for factor in months:
        monthly_flow = flow_rate * factor
        monthly_power = calculate_power(monthly_flow, head, efficiency)
        monthly_powers.append(monthly_power)
    return monthly_powers

# Main Execution
power_output = calculate_power(flow_rate, head, efficiency)
selected_turbine = select_turbine(head, flow_rate)

# Economic Analysis
capital_cost, annual_revenue, payback_period = economic_analysis(power_output)

# Seasonal Variability Simulation
monthly_factors = [0.7, 0.8, 1.0, 1.2, 1.1, 0.9, 0.8, 0.7, 0.9, 1.0, 1.1, 1.2]
monthly_powers = seasonal_variability(head, flow_rate, monthly_factors)

# Display Results
print(f"Power Output: {power_output:.2f} kW")
print(f"Selected Turbine: {selected_turbine}")
print(f"Capital Cost: ${capital_cost:,.2f}")
print(f"Annual Revenue: ${annual_revenue:,.2f}")
print(f"Payback Period: {payback_period:.2f} years")

# Plot Seasonal Power Output
plt.figure()
months = np.arange(1, 13)
plt.bar(months, monthly_powers, color="skyblue", label="Monthly Power Output")
plt.xlabel("Month")
plt.ylabel("Power Output (kW)")
plt.title("Seasonal Variability in Power Output")
plt.xticks(months)
plt.grid(axis="y")
plt.legend()
plt.show()

# Plot Efficiency Curve
def plot_efficiency_curve():
    flow_rates = np.linspace(5, 50, 100)  # Vary flow rate between 5 and 50 m^3/s
    power_outputs = [calculate_power(flow, head, efficiency) for flow in flow_rates]
    efficiency_curve = np.linspace(0.7, 0.95, len(flow_rates))  # Example efficiency curve
    adjusted_power = [calculate_power(flow, head, eff) for flow, eff in zip(flow_rates, efficiency_curve)]

    plt.figure()
    plt.plot(flow_rates, power_outputs, label="Ideal Power Output", linestyle="--")
    plt.plot(flow_rates, adjusted_power, label="Adjusted Power Output")
    plt.xlabel("Flow Rate (m^3/s)")
    plt.ylabel("Power Output (kW)")
    plt.title("Efficiency Impact on Power Output")
    plt.legend()
    plt.grid()
    plt.show()

plot_efficiency_curve()
```
