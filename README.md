# Prospective LCA of PLA Production in Denmark

**Prospective Life Cycle Assessment and Input-Output Modeling of Polylactic Acid Production: A 2050 Sustainability Roadmap for Denmark**

Course project for **12773 Advanced Life-Cycle Assessment Methods** at the Technical University of Denmark (DTU), Spring 2026.

> Group project combining environmentally extended input-output analysis, prospective life-cycle assessment, scenario modelling, and environmental learning to investigate the future environmental performance of polylactic acid (PLA) production toward 2050.

---

## Project Overview

Polylactic acid (PLA) is a bio-based and biodegradable alternative to conventional fossil-based plastics. However, its future environmental performance depends not only on improvements in PLA production itself, but also on changes in electricity systems, transport, agricultural supply chains, and other background processes.

This project evaluates PLA production from both **economy-wide** and **process-level** perspectives.

The study combines:

- **Environmentally Extended Input-Output (EEIO) analysis** using EXIOBASE 3
- **Structural Path Analysis (SPA)** to identify supply-chain hotspots
- **Process-based Life Cycle Assessment (LCA)** of PLA production
- **Prospective LCA** under SSP1 and SSP2 scenarios
- **Environmental learning curves** to represent technological improvement
- **Backcasting** to estimate learning conditions required to meet future environmental targets
- **Absolute Sustainability Assessment (ASA)** to evaluate performance relative to an allocated Safe Operating Space

The functional unit is **1 kg of industrial-grade PLA granulate**, assessed using a cradle-to-gate system boundary.

---

## Methodology

### 1. EEIO and Macro-sector Analysis

PLA production was mapped to the EXIOBASE 3 sector:

> **“Plastics, basic” (Sector 24.3)**

A Python-based workflow was used to analyse the Danish plastics sector and its upstream supply-chain structure.

The analysis included:

- production-based and consumption-based environmental impacts
- sectoral output and self-sufficiency
- GHG emission intensity
- identification of major contributing sectors
- Structural Path Analysis across multiple supply-chain tiers

The accompanying Jupyter notebook is available in:

`code/eeio-analysis.ipynb`

### 2. Prospective Life Cycle Assessment

A representative PLA production process from ecoinvent was modelled using **Activity Browser** and **premise**.

Future background systems were generated using the **REMIND Integrated Assessment Model** under two Shared Socioeconomic Pathways:

- **SSP1** — faster decarbonization and stronger climate-policy ambition
- **SSP2** — a moderate, middle-of-the-road transition pathway

Environmental impacts were evaluated from **2020 to 2050**.

Three impact categories were considered:

- Climate change — kg CO₂-eq
- Ozone depletion — kg CFC-11-eq
- Material resources — kg Sb-eq

### 3. Environmental Learning

Foreground technological development was represented using a **quasi S-curve environmental learning model**.

Environmental learning rates (eLR) of **3.3%, 5%, 10%, and 15%** were explored to investigate how technological capability affects future environmental performance.

Technology growth was represented using doubling time (`Td`), including:

- `Td = 3.56 years` — rapid market expansion
- `Td = 10 years` — conservative growth scenario

A backcasting approach was subsequently used to estimate the learning conditions required to achieve predefined environmental targets.

### 4. Absolute Sustainability

An Absolute Sustainability Assessment was used to compare the estimated environmental impact of the Danish PLA system with its allocated share of the global **Safe Operating Space (SOS)**.

This provides a complementary perspective to conventional relative impact reductions by asking whether future improvements are sufficient in absolute sustainability terms.

---

## Key Findings

### Denmark relies on embodied emissions from international supply chains

For the Danish basic plastics sector, consumption-based GHG emissions were estimated at **17.73 Mt CO₂e**, compared with production-based emissions of **10.83 Mt CO₂e**.

This indicates that a substantial share of environmental pressure associated with Danish plastics consumption occurs outside domestic production.

The sector showed a self-sufficiency ratio of approximately **90.78%**, with the remaining demand supplied through imports.

### Supply-chain hotspots extend beyond direct PLA production

The GHG intensity of the Danish basic plastics sector was estimated at approximately:

**0.286 kg CO₂e/EUR**

Structural Path Analysis showed that important environmental hotspots occur in upstream supply chains, particularly among first-tier suppliers.

Major contributors included:

- sea and coastal water transportation
- direct basic-plastics production
- steam and hot-water supply

This highlights the importance of considering international logistics and energy supply when evaluating PLA sustainability.

### Decarbonization substantially reduces climate impacts

Under SSP1, the climate-change impact of PLA production decreases from approximately:

**2.63 → 0.79 kg CO₂-eq/FU**

between 2020 and 2050.

Under SSP2, the corresponding reduction is:

**2.67 → 1.41 kg CO₂-eq/FU**

The stronger reduction under SSP1 reflects faster decarbonization of the background energy system.

### Lower carbon impacts can create burden shifting

Climate performance improves substantially toward 2050, but other environmental indicators do not necessarily follow the same trend.

Under SSP1, material-resource impacts increase from approximately:

**1.36 × 10⁻⁵ → 2.05 × 10⁻⁵ kg Sb-eq/FU**

Ozone-depletion impacts also increase under both scenarios.

These results demonstrate that decarbonization can shift environmental pressure toward resource extraction, infrastructure, and upstream supply chains.

### Technological learning and market growth work together

At an environmental learning rate of **5%**, the comprehensive environmental impact in 2050 was estimated at:

| Technology doubling time | 2050 impact |
| --- | ---: |
| 3.56 years | 0.26 kg CO₂-eq/FU |
| 10 years | 0.59 kg CO₂-eq/FU |

Faster market expansion therefore accelerates cumulative learning and substantially improves long-term environmental performance.

For the carbon-neutrality backcasting analysis, an estimated eLR of **8.52%** was required with a 3.56-year doubling time, whereas a slower 10-year doubling time increased the required learning rate to **22.14%**.

### Relative improvement does not automatically imply absolute sustainability

The Absolute Sustainability Assessment estimated that the current Danish PLA system exceeds its allocated climate Safe Operating Space by approximately:

**77.6×**

This suggests that incremental efficiency improvements alone are insufficient.

The proposed long-term pathway therefore combines technological learning with renewable electricity, process optimization, low-carbon transport, and broader supply-chain decarbonization.

---

## Sustainability Roadmap

The results suggest a possible pathway toward lower-impact PLA production:

**Before 2030**
- accelerate renewable electricity integration
- improve production efficiency
- identify and reduce major upstream supply-chain hotspots

**By 2040**
- achieve large-scale energy-system decarbonization
- reduce dependence on fossil-based heat and transport
- strengthen low-carbon supply chains

**Toward 2050**
- combine background-system decarbonization with sustained technological learning
- approach climate-neutral PLA production
- mitigate burden shifting in resource use and ozone depletion

The analysis emphasizes that technological improvement in PLA production alone is not sufficient; transformation of the wider energy, transport, and material systems is also required.

---

## Tools & Methods

| Category | Tools / Methods |
| --- | --- |
| Programming | Python, Jupyter Notebook |
| EEIO | EXIOBASE 3 |
| Supply-chain analysis | Structural Path Analysis (SPA) |
| LCA | Activity Browser, ecoinvent |
| Prospective LCA | premise |
| Integrated assessment | REMIND |
| Future scenarios | SSP1, SSP2 |
| Impact assessment | Environmental Footprint (EF) |
| Technology modelling | Environmental learning curves, quasi S-curve |
| Target assessment | Backcasting, Absolute Sustainability Assessment |

---

## My Contribution

This was a **three-person group project**.

My main contributions included:

- developing and interpreting parts of the **prospective LCA framework**
- contributing to the **Life Cycle Inventory (LCI)** and **Life Cycle Impact Assessment (LCIA)**
- analysing prospective environmental impacts under **SSP1 and SSP2**
- contributing to the **background-system analysis**
- modelling and interpreting **environmental learning effects and technological doubling-time scenarios**
- contributing to the discussion of **burden shifting, technological learning, and methodological limitations**
- supporting the integration and interpretation of results in the final report

The EEIO analysis notebook included in this repository documents the computational workflow used for the input-output and supply-chain analysis component of the project.

---

## Repository Structure

```text
prospective-lca-pla-denmark/
│
├── README.md
│
├── code/
│   └── eeio-analysis.ipynb
│
└── report/
    └── prospective-lca-pla-denmark-report.pdf
```

### `code/`

Contains the Jupyter notebook used for the EEIO and supply-chain analysis, including EXIOBASE processing and Structural Path Analysis.

### `report/`

Contains the complete group project report, including the prospective LCA methodology, scenario analysis, environmental learning assessment, sustainability roadmap, discussion, and appendices.

---

## Main Takeaway

> **Decarbonizing the background energy system can substantially reduce the climate impact of PLA production, but achieving long-term sustainability also requires technological learning, rapid deployment, and mitigation of environmental burden shifting across global supply chains.**

---

## Project Information

**Course:** 12773 Advanced Life-Cycle Assessment Methods  
**Institution:** Technical University of Denmark (DTU)  
**Semester:** Spring 2026  
**Project type:** Group project  
**Case study:** Polylactic acid (PLA) production in Denmark  
**Time horizon:** 2020–2050
