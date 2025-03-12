# belly-button-challenge
# Belly Button Biodiversity Dashboard

## Overview
This project is an interactive dashboard that visualizes microbial data from belly button samples. It uses **D3.js** to fetch data, **Plotly.js** to create dynamic charts, and **JavaScript** to update visualizations based on user selections. The dataset is sourced from an external JSON file.

## Features
- **Dropdown Menu**: Select a sample ID to view data for different individuals.
- **Metadata Panel**: Displays demographic information for the selected sample.
- **Bar Chart**: Shows the top 10 bacterial species present in the sample.
- **Bubble Chart**: Displays all bacterial cultures found per sample with size and color variations.
- **Dynamic Updates**: Charts and metadata panel update based on user selection.

## Technologies Used
- **HTML**: Structure of the webpage.
- **CSS**: Basic styling.
- **JavaScript**: Core functionality.
- **D3.js**: Fetching and handling data.
- **Plotly.js**: Creating interactive visualizations.

## File Structure
```
📂 project-folder
 ├── 📄 index.html      # Main HTML file
 ├── 📄 app.js         # Main JavaScript logic
 ├── 📄 samples.json   # Data file (or fetched from external URL)
 ├── 📄 README.md      # Project documentation
```

## How to Run the Project
### Option 1: Using Python HTTP Server
1. Open the project directory in a terminal.
2. Run the following command:
   ```sh
   python -m http.server 8000
   ```
3. Open a browser and go to: `http://localhost:8000`

### Option 2: Using Node.js HTTP Server
1. Install `http-server` globally (if not already installed):
   ```sh
   npm install -g http-server
   ```
2. Run the server:
   ```sh
   http-server
   ```
3. Open the browser and go to `http://localhost:8080`

## Code Breakdown
### `init()` Function
- Fetches data and populates the dropdown menu.
- Loads the first sample's metadata and charts.

### `buildMetadata(sample)`
- Extracts and displays metadata for the selected sample.
- Uses D3 to update the panel dynamically.

### `buildCharts(sample)`
- Retrieves bacterial sample data.
- Generates a **Bubble Chart** for all OTUs.
- Creates a **Bar Chart** for the top 10 OTUs.

### `optionChanged(newSample)`
- Updates the charts and metadata when a new sample is selected from the dropdown.

## Troubleshooting
**Issue: Localhost not connecting**
- Ensure a local server is running.
- Check for firewall or antivirus restrictions.
- Verify the correct URL in `d3.json()`.

**Issue: CORS errors when loading JSON**
- Run a local server instead of opening `index.html` directly in a browser.

## Future Improvements
- Add more interactivity (e.g., hover effects, tooltips).
- Improve UI design with CSS or Bootstrap.
- Include additional statistical insights.

## Credits
This project is part of an educational module on data visualization using D3.js and Plotly.js. The dataset is publicly available for learning purposes.

