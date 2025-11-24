## Bread & Bean Café Chain

Data on store profitability and operational characteristics for the **Bread & Bean** case.
There are 60 existing cafés and 10 potential new locations.
The predictive model should be trained on data from the existing 60 stores.

### Variables

* STORE_ID: Unique café identifier
* CITY_NAME: City in which the café is located (provided for new outlets only)
* PROFIT: Annual operating profit ($1,000) — calculated as sales minus variable operating costs.
  Variable costs include salaries, utilities, supplies, and inventories.
  Fixed property and equipment costs are borne by headquarters and excluded from the profit measure.
* CAPITAL: Total investment in property, remodeling, and equipment ($1,000)
* AREA: Total indoor area of the café (square meters)
* STAFF: Number of employees (for potential cafés, not yet determined)
* AGE_A: Population aged 15–24 within a 3 km radius (in thousands)
* AGE_B: Population aged 25–34 within a 3 km radius (in thousands)
* AGE_C: Population aged 35–44 within a 3 km radius (in thousands)
* AGE_D: Population aged 45–54 within a 3 km radius (in thousands)
* AGE_E: Population aged 55 and above within a 3 km radius (in thousands)
* POP_TOTAL: Total population within a 3 km radius (in thousands)
* INCOME: Average household income in the surrounding area ($1,000)
* COMPETITOR_COUNT: Number of direct competitors (cafés, fast food restaurants, or bars offering lunch) within 1 km
* NONCOMPETITOR_COUNT: Number of restaurants in the area that do not compete directly with Bread & Bean
* OTHER_BUSINESS_COUNT: Number of non-restaurant businesses within 1 km
* RENT_RATE: Monthly rent per square meter of retail properties in the same area
* COST_INDEX: Local cost-of-living index measuring neighborhood expense level
* CITY_NAME: City name (for potential new café sites)
