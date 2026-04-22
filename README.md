# SPOTLOG Data Pipeline — Route Comparator

An interactive **Streamlit** application for analysing and comparing emissions and energy consumption between **Eco** and **Alternative** routes, based on data collected by PEMS (*Portable Emissions Measurement System*) equipment.

---

## Overview

This project is part of a research thesis on sustainable mobility. The application enables comparison of the environmental and energy performance of four distinct vehicles (combustion, hybrid, and electric) across six urban and peri-urban corridors in the Centro region of Portugal.

Data comes from real on-road measurements organised in the Excel dataset, and is processed and visualised dynamically within the application.

---

## Files

| File | Description |
|---|---|
| `comparador_rotas.py` | Main Streamlit application |
| `Organized Data_19_11_2025.xlsx` | Dataset with trip results measured by PEMS |
| `LASI_poster.pptx` | Scientific poster presented at the LASI conference |

---

## Vehicles

| ID | Vehicle | Powertrain |
|---|---|---|
| 37 | Citroën C4 | Diesel |
| 40 | Fiat Panda | Mild Hybrid (MHEV) |
| 43 | Volkswagen ID.3 | Electric |
| 46 | Peugeot 3008 | Mild Hybrid (MHEV) |

---

## Corridors

| Code | Route |
|---|---|
| AR / AL | Aveiro — University of Aveiro ↔ Ílhavo |
| CR / CL | Coimbra — Mercado de Santiago ↔ Hotel Mélia Ria |
| DR / DL | Sever do Vouga / Albergaria — Continente ↔ CM Sever do Vouga |

Each corridor has two variants: **Eco** (`_E`) and **Alternative** (`_G`).

---

## Available Metrics

**Combustion / hybrid vehicles:**
- CO₂ (g and g/km)
- Fuel consumption (L/100km)
- NOx, HC, CO (g and mg/km)
- Distance (km) and Travel time

**Electric vehicle:**
- Energy (kWh and kWh/km)
- Distance (km) and Travel time

---

## Getting Started

### Prerequisites

```bash
pip install streamlit pandas openpyxl plotly
```

### Run the application

```bash
streamlit run comparador_rotas.py
```

The app will open in your browser at `http://localhost:8501`.

### Usage

1. Select the **vehicle** in the sidebar
2. Choose the **corridor** (area and direction)
3. Select the **trip number**
4. Pick the **metrics** to compare
5. Navigate between tabs: **Comparison**, **Charts**, and **Summary**

---

## Data Structure

The Excel file contains two main sheets:

- **`Organized Data_No PEMS`** — trip metadata (ID, date, etc.)
- **`Results`** — measurement results per trip, route, and vehicle

---

## Author

Samuel Figueira — sfigueira0105@gmail.com
