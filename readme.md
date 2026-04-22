# Energy Data Documentation (Our World in Data)

## 1. Introduction

This document provides a structured overview of two datasets from Our World in Data (OWID):

- **Energy Consumption by Source**
- **Energy Use per Person**

These datasets offer complementary perspectives on global energy use. The first captures total energy consumption disaggregated by energy source, while the second normalizes consumption on a per capita basis, enabling cross-country comparisons.

---

## 2. Data Structure

Both datasets share a common tabular structure.

### 2.1 Core Variables

- **Entity**: Name of the country or region  
- **Code**: OWID identifier (generally aligned with ISO alpha-3 codes)  
- **Year / Day**:  
  - *Year*: integer (annual observations)  
  - *Day*: date string (YYYY-MM-DD), if applicable  

### 2.2 Data Columns

- **Energy consumption by source**: multiple columns, each representing a distinct energy source  
- **Energy use per person**: a single column representing per capita energy consumption  

---

## 3. Metadata

Each dataset includes a `.metadata.json` file containing:

- Chart-level information (e.g., title, subtitle)
- Column-level metadata:
  - Units of measurement  
  - Temporal coverage  
  - Source attribution and citations  

This structure supports reproducibility and transparency.

---

## 4. Data Sources and Processing

### 4.1 Source Attribution

The datasets are compiled from multiple external sources, including:

- Energy Institute – *Statistical Review of World Energy*  
- U.S. Energy Information Administration (EIA)  
- Population data from various sources  

### 4.2 Data Processing

Data preparation involves:

- Standardization of country names and regional classifications  
- Unit conversion  
- Construction of derived indicators (e.g., per capita values)  
- Harmonization of metadata  

Users are responsible for complying with the licensing conditions of the original data providers.

---

## 5. Energy Consumption by Source

### 5.1 Overview

- **Unit**: Terawatt-hours (TWh)  
- **Time range**: 1965–2024  
- **Last updated**: June 27, 2025  

### 5.2 Energy Categories

#### Renewable and Low-Carbon Sources

- Solar  
- Wind  
- Hydropower  
- Nuclear  
- Biofuels  
- Other renewables (including geothermal and biomass)  

#### Fossil Fuels

- Oil  
- Gas  
- Coal  

---

### 5.3 Methodology

#### 5.3.1 Input-Equivalent Energy

Electricity-based energy sources are expressed using the **substitution method**, which estimates the equivalent amount of primary energy required in fossil fuel power plants.

- Approximate conversion efficiency: **41%** (solar, wind, hydro, nuclear)  
- Biomass-specific efficiency: **32%**  

#### 5.3.2 Methodological Change

In 2025, the underlying source adopted the **Physical Energy Content method**. OWID continues to apply the substitution method to ensure consistency across time series.

---

### 5.4 Fossil Fuel Measurement Notes

- **Gas**: Includes gas used in transformation processes; excludes gas converted into liquid fuels  
- **Coal**: Includes commercial solid fuels; excludes conversion into liquid or gaseous fuels  
- **Oil**: Includes aviation and marine bunkers; excludes biofuels  

---

### 5.5 Source

Energy Institute (2025). *Statistical Review of World Energy*.  
https://www.energyinst.org/statistical-review/

---

## 6. Energy Use per Person

### 6.1 Overview

- **Indicator**: Primary energy consumption per capita  
- **Unit**: Kilowatt-hours per person  
- **Time range**: 1965–2024  
- **Last updated**: June 27, 2025  

---

## 6.2 Methodology

This dataset combines:

- Energy consumption data from:
  - Energy Institute (EI)  
  - U.S. Energy Information Administration (EIA)  
- Population data from multiple sources  

### Data Integration Strategy

- EI data is used where available  
- EIA data is used to fill gaps  

### Calculation

Energy consumption per capita is defined as:

Energy per capita = Total energy consumption / Population

---

## 6.3 Sources

- U.S. Energy Information Administration (2025). *International Energy Data*  
- Energy Institute (2025). *Statistical Review of World Energy*  
- Various sources (2024). Population data compiled by Our World in Data  

---

## 7. Comparison of Datasets

| Dimension | Energy Consumption by Source | Energy Use per Person |
|----------|-----------------------------|----------------------|
| Analytical focus | Total energy consumption | Per capita consumption |
| Structure | Multiple variables | Single variable |
| Unit | Terawatt-hours (TWh) | kWh per person |
| Derived metric | No | Yes |
| Data sources | Energy Institute | EI, EIA, population data |

---

## 8. Concluding Remarks

The two datasets provide complementary analytical value. The energy-by-source dataset enables examination of energy composition and transitions, while the per capita dataset supports comparative analysis of energy use across populations.

When using these datasets jointly, attention should be paid to differences in methodology, source integration, and unit definitions to ensure consistent interpretation.

---

## 9. References

- Energy Institute (2025). *Statistical Review of World Energy*  
- U.S. Energy Information Administration (2025). *International Energy Data*  
- Our World in Data. Population datasets and documentation  



    
