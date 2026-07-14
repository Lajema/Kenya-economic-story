# 🏛️ Kenya Economic Pulse: Macroeconomic Storyboard

An interactive, multi-page data application built with Streamlit that transforms decades of complex historical numbers into a structured, narrative-driven exploration of Kenya’s macroeconomic vitals using World Bank Open Data.

## 🎨 Visual Philosophy: Modern Humanist
Unlike the industrial grid layout used in the environmental platform, the Economic Pulse platform leverages a **modern corporate analytics framework**:
* **Lato Typography Integration:** Injected via custom global CSS containers to apply a highly scannable, geometric sans-serif type hierarchy across all Markdown headers, metric nodes, and plot text layers.
* **Streamlined Chart Layouts:** Cleaner plotting footprints focusing on unified hover labels and intuitive color styling (`#10b981` for expansion metrics, `#ef4444` for economic constraints).
* **Plain-English "Translator Notes":** Built-in narrative windows that swap cold financial formulas for real-world analogies (e.g., comparing inflation to windshield wind resistance) so any visitor can immediately trace why the indicators matter.

---

## 📖 The Dashboard Storyline

The financial platform groups complex public tracking data into a fluid, logical three-stage narrative:

### 1. 🏛️ Executive Summary (The Pulse)
* **The Story:** A high-level financial health screening displaying essential vital signs: Annual Real GDP growth speed, Inflation velocity, Diaspora Remittance volumes, and Central Bank hard currency rainy-day savings.
* **The Translation:** Focuses on the immediate tug-of-war between growth speeds and inflation costs. If the inflation timeline climbs too close to the growth line, it indicates a cost-of-living squeeze on household purchasing power.

### 2. 🔄 Growth & Stability Deep Dive (The Engine)
* **The Story:** A comparative look under the hood to analyze internal domestic budgeting habits and structural saving levels.
* **The Translation:** * *The Budget Tightrope:* Explains how a rising interest-to-revenue ratio chips away at public spending power, restricting what the state has left to build schools, supply hospitals, or pave roads.
  * *The Piggy Bank vs. Mega Projects:* Contrasts national domestic savings pools directly against structural asset building (Capital Formation), showing how a deficit between savings and development spending triggers a reliance on foreign loans.

### 3. 🌐 External Trade & Remittances (The Bridges)
* **The Story:** Tracks how money and commodities move across borders, highlighting trade imbalances and structural safety valves.
* **The Translation:** Evaluates Kenya's structural *Trade Deficit* (buying more from global suppliers than we sell outward). It introduces the diaspora workforce as an "invisible hero" whose inbound currency wires directly refill the central bank's foreign exchange cushions to protect the local currency from crashing.

### 4. 🔮 Future Horizons (5-Year Predictive Modeling)
* **The Story:** An algorithmic projection workbench letting users select a baseline financial metric and chart its projected pathway through the next 5 sequence intervals.
* **The Translation:** Employs a rolling linear trend model to show exactly where modern structural momentum will carry key variables by 2030, provided macro habits remain steady.

---

## 🛠️ Key Bug Fixes & Code Stability

### Mitigating Axis Auto-Zoom Crashing
When timeline sliders were manipulated into narrow, single-year time slices (e.g., examining data from just 2011), Plotly’s default layout engine auto-zoomed directly into microscopic decimals. This behavior resulted in completely unreadable, overlapping text clusters along the axis boundaries.

**The Fix Implemented:**
1. **Clean Array Extraction:** Modified data extraction paths from raw multi-dimensional blocks (`.values`) to strict index parsing (`['Value']`) to ensure reliable data alignment.
2. **Fixed Range Bounds:** Added fixed range limitations to prevent layout compression and stabilize the chart framework.
3. **Truncated Decimal Formatting (`tickformat=".1f"`):** Locked display labels into single-decimal float strings, transforming long overlapping numbers like `6.32103524...` into crisp, scannable milestones (e.g., `6.3%`).

---

## 🚀 Technical Requirements & Execution

### 1. Data File Configuration
Ensure that the World Bank database target file `API_KEN_DS2_en_csv_v2_5938.csv` is saved directly inside your root project directory.

### 2. Running the Application
Install dependencies and launch the dashboard ecosystem:

```bash
pip install streamlit pandas numpy plotly scikit-learn
streamlit run economic_app.py
