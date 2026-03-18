# 📊 Procurement Forecast Engine

A browser-based forecasting tool for procurement planning. Runs entirely client-side — no server, no data leaves your browser.

## Features

- **PAR Attrition** — forecast based on stock levels and attrition rates, scaled by occupancy
- **Holt-Winters Seasonal** — triple exponential smoothing on historical sales data
- **Event Overrides** — manual override for event-driven demand
- **First-Time Buys** — flat demand projection for new SKUs with no history
- **Safety Stock & Reorder Points** — automatic calculation with configurable service levels
- **CSV Export** — download full forecast results

## Deploy to GitHub Pages

1. Create a new GitHub repository
2. Push the `index.html` file to the `main` branch
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch** → `main` → `/ (root)`
5. Your forecast engine will be live at `https://<username>.github.io/<repo>/`

## Usage

1. **Upload Data** — drag and drop your CSV files (only SKU Master is required)
2. **Map Categories** — assign forecast methods to each SKU
3. **First-Time Buys** — add any new SKUs without history
4. **Settings & Run** — choose a horizon and run the forecast
5. **Results** — view, sort, filter, and export your forecast

## CSV Format

### SKU Master (required)
```
SKU, Category, Lead Time, On Hand, On PO, Orders Per Month
```

### PAR Table (optional)
```
SKU, Property, PAR, Attrition Rate, Baseline Occupancy
```

### Occupancy Forecast (optional)
```
Property, Month, Occupancy Rate
```

### Sales History (optional)
```
Order Date, SKU, Property, Quantity
```

## License

MIT
