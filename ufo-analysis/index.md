---
layout: default
title: UFO Analysis
---

# UFO Sightings Analysis

## Visualization 1: Nationwide UFO Reports Map

### Description
This plot visualizes UFO sightings across the United States, aggregated by state. The color encoding represents different shapes or years. Users can filter the data by selecting a specific state or adjusting the year group slider.

### Design Choices
- **Encoding:** Color represents different shapes or year groups.
- **Interactivity:** Dropdown menu and slider allow users to filter data by state and year range.

### Data Transformation
- Transformed state abbreviations to full state names.
- Grouped years into two-year intervals for clarity.

### Interactivity Explanation
The interactivity allows the user to focus on specific states and time periods, enhancing clarity and analytical potential.

---

## Visualization 2: Time Series Line Plot

### Description
This plot shows the trend of UFO reports over time for each state. Users can compare states by filtering through the dropdown menu and adjusting the year group slider.

### Design Choices
- **Encoding:** Different colors are used to represent different states.
- **Interactivity:** Tooltip and red dot provide detailed information for each point.

### Data Transformation
- Transformed state abbreviations to full state names.
- Grouped years into two-year intervals for clarity.

### Interactivity Explanation
The hovering effect with a red dot and tooltip enhances data comprehension by providing precise values upon inspection.

---

## Links

- [The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)
- [The Plots](ufo_analysis.html)

### Embedded Plots:
<iframe src="ufo_analysis.html" width="100%" height="600px" style="border:none;"></iframe>

- [The Code](ufo_analysis.ipynb)
