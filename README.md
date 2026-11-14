# Cyclone Hudhud Track Visualization

A Jupyter Notebook visualization of Cyclone Hudhud (2014) using India Meteorological Department (IMD) best-track observations. The notebook plots the complete recorded track and highlights locations at four-day intervals.

## Features

- Reads the 2014 worksheet from the IMD best-track Excel workbook.
- Selects observations for Hudhud.
- Cleans and sorts dates and latitude/longitude coordinates.
- Displays a table of positions selected at four-day intervals, including wind speed and grade when those fields are available.
- Plots the full track on a geographic map, with interval dates labeled on the map.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- `pandas`
- `numpy`
- `openpyxl`
- `plotly`

Install the packages from a notebook cell if needed:

```python
%pip install pandas numpy openpyxl plotly
```

## Data

The notebook uses the workbook `IMD_Best_Tracks_Data_1982-2025 (1).xlsx`. The workbook should contain a worksheet named `2014` and columns for the cyclone name, date, latitude, and longitude. Wind and grade columns are optional.

Update the `FILE` variable in the first notebook cell to the workbook's location on your computer. For example:

```python
FILE = r"C:\path\to\IMD_Best_Tracks_Data_1982-2025 (1).xlsx"
```

## Run the notebook

1. Place `HUDHUD.ipynb` and the IMD Excel workbook in a convenient folder, or set `FILE` to the workbook's full path.
2. Open `HUDHUD.ipynb` in Jupyter Notebook or JupyterLab.
3. Run the cells from top to bottom.
4. Review the four-day interval positions table and the Hudhud track map.

The notebook sets `INTERVAL_DAYS = 4`. Change this value in the first cell if you want a different interval.

## How the plot works

The blue line connects all valid Hudhud observations in date order. Red markers show the observation closest to each four-day target date, including the final observation. Hover over the track or markers to view the date and coordinates.

## Data note

The visualization shows the positions recorded in the supplied IMD best-track workbook. The map is an exploratory view of the track and does not independently estimate cyclone intensity, impacts, or forecast movement.
