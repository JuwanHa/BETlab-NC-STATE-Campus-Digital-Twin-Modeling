# BETlab NC State Campus Digital Twin Modeling

This repository documents the Building Energy Technology Laboratory (BETlab) digital twin modeling work for North Carolina State University's Centennial Campus. Centennial Campus operates as a microgrid campus with district heating and cooling, combined heat and power (CHP), thermal energy storage, solar photovoltaic generation, battery energy storage systems, advanced metering infrastructure, and building automation systems.

The project develops and organizes digital twin models of campus buildings and district heating and cooling systems to support simulation, control, semantic validation, demand flexibility, energy efficiency, and resilience studies.

## Campus Digital Twin Scope

NC State Centennial Campus provides a real-world testbed for grid-interactive and energy-flexible building research. The digital twin effort connects building energy models, HVAC system representations, semantic models, measured BAS data, utility data, and advanced control workflows.

Requests for information related to the campus digital twin building models should be directed to Dr. Soolyeon Cho, Director of the Building Energy Technology Laboratory (BETlab), at scho3@ncsu.edu.

## Building Models

### Fitts-Woolard Hall

Fitts-Woolard Hall is a four-story academic building on Centennial Campus completed in 2020. The building is served by the campus district heating and cooling system and includes VAV systems with terminal reheat coils, Dedicated Outdoor Air Systems (DOAS), and AHU economizers.

The EnergyPlus model represents the full building, including all floors and occupied spaces. It aggregates 465 rooms into 226 thermal zones and models the district heating and cooling connection using EnergyPlus `DistrictHeating` and `DistrictCooling` components. The air-side HVAC system includes four AHUs, with AHU-1 serving laboratory spaces and AHU-2 through AHU-4 serving general spaces with DOAS support.

A semantic modeling and validation workflow is also developed for Fitts-Woolard Hall using BAS data, Brick schema, ASHRAE Standard 223P concepts, and SHACL constraints. This workflow supports validation of HVAC data consistency and operational rules based on ASHRAE Guideline 36.

### Wolf Ridge Apartments and Industrial Building

Digital twin models are used to evaluate a Building Thermal System (BTS) across multiple real case-study buildings, including a mid-sized institutional office building, a six-story suite-style student housing building, and a lightweight steel-structure warehouse.

The BTS includes rooftop solar thermal collectors, Thermal Mass Energy Storage (TMES), Thermally Activated Building Systems (TABS), and DOAS ventilation. High-fidelity dynamic simulations using actual weather and utility meter data were conducted at one-minute resolution for the peak heating period from December 13 to 22, 2023.

### Hunt Library

The James B. Hunt Jr. Library model represents a flagship academic facility with flexible interior layouts, extensive glazing, technology-rich spaces, VAV air handling units, demand-controlled ventilation, hydronic heating and cooling distribution, and district energy integration. The Hunt Library building energy model is currently under development.

### Textile Complex

The Textile Complex model represents the Wilson College of Textiles facilities, including classrooms, research laboratories, pilot-scale manufacturing spaces, and industry-engaged extension areas. The model accounts for laboratory-intensive HVAC needs, including high-capacity ventilation, humidity-controlled environments, and dedicated exhaust systems. The Textile Complex building energy model is currently under development.

### Solar House

The NCSU Solar House model represents a demonstration residence focused on passive and active solar design, renewable energy integration, solar thermal domestic hot water, photovoltaic generation, high-efficiency heat pump operation, natural ventilation, and building-scale energy monitoring. The Solar House building energy model is under validation.

## Advanced Modeling and Control

The broader research effort includes Physics-Informed Neural Network (PINN) models that combine data-driven learning with thermodynamics and heat-transfer principles. By integrating calibrated EnergyPlus simulation data with RC thermal network models, PINNs can support physically consistent prediction of building thermal dynamics. When coupled with Model Predictive Control (MPC), these models enable optimized HVAC setpoint control and improved cooling energy efficiency.

## Repository Contents

- `docs/DT Modeling.docx`: source document describing the current digital twin modeling work and supporting references.
- `README.md`: repository overview and project description for GitHub.

## References

- Yujin Kim, Juwan Ha, Seungmin Lee, Soolyeon Cho. (2026). Ontology-Based Semantic Modeling of HVAC Systems in the Office Building: A Foundation for Scalable Control and Digital Twin Integration. 2026 ASHRAE Winter Conference, Las Vegas.
- Hawks, M. and S. Cho. (2024). Review and analysis of current solutions and trends for zero energy building (ZEB) thermal systems. Renewable and Sustainable Energy Reviews, 189, 114028.
- Hawks, M. and S. Cho. (2026). Thermal Mass Energy Storage (TMES) Engineering Framework that Enables the Use of Passive and Renewable Energy for Radiant Heating and Cooling Systems. ASHRAE Transactions, 132, LV-26-137.
- Hawks, M. and S. Cho. (2026). Control Architecture for an Energy Flexible Building Dual Mechanical System with Novel Storage. ASHRAE Transactions, 132, LV-26-094.
- Juwan Ha, Seungmin Lee, Yujin Kim, and Soolyeon Cho. (2025). Improving energy and data efficiency in factory building: A physics-informed neural networks-based model predictive control (PINNs-based MPC) approach. ASHRAE Transactions, 131, 670-678.
- Seo, B., Yoon, Y. B., Yu, B. H., Cho, S., and Lee, K. H. (2020). Comparative analysis of cooling energy performance between water-cooled VRF and conventional AHU systems in a commercial building. Applied Thermal Engineering, 170, 114992.
- Seo, B., Yoon, Y., Lee, K. H., and Cho, S. (2023). Comparative analysis of ANN and LSTM prediction accuracy and cooling energy savings through AHU-DAT control in an office building. Buildings, 13(6), 1434.
- Yoon, Y., Seo, B., Mun, J., and Cho, S. (2023). Energy savings and life cycle cost analysis of advanced double skin facade system applied to old apartments in South Korea. Journal of Building Engineering, 71, 106535.
