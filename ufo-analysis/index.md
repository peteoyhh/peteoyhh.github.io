---
layout: default
title: UFO Sightings Analysis
---

<style>
  h1 {
    font-size: 2em; /* Adjust font size of h1 */
    margin-top: 20px; /* Add space between the title and the top */
  }
  h2 {
    font-size: 1.8em; /* Adjust font size of h2 */
  }
  h3 {
    font-size: 1.5em; /* Adjust font size of h3 */
  }
  .section-title {
    font-size: 1.6em; /* Adjust the font size for section titles */
  }
</style>

# UFO Sightings Analysis

## **Visualization 1: Nationwide UFO Reports Map**

### **Description**
This plot visualizes UFO sightings across the United States, aggregated by state. The map shows points for each UFO sighting, with users being able to filter the data by state and year. The first map shows sightings across the entire United States, while the second map zooms in on the selected state. The color encoding represents the frequency of sightings in different locations.

### **Design Choices**
- **Encoding:** The map uses geographic shapes to represent different states. Points are plotted based on the latitude and longitude of UFO sightings, with color indicating their number of occurrences in each state.
- **Interactivity:** 
  - A dropdown menu allows users to select specific states to focus on. 
  - A slider is provided to filter the data by year, enabling users to explore trends over time.
  - The nationwide map (left) will only show reports for the nation, while the state map (right) will zoom into the selected state, showing the reports for that particular state.

### **Data Transformation**
- State abbreviations were transformed into full state names for better clarity.
- The dataset is filtered to focus on the continental United States, excluding Alaska and Hawaii.
- The sightings are aggregated by year for better visualization and trends analysis.

### **Interactivity Explanation**
The interactivity allows the user to focus on specific states by selecting them from the dropdown menu. Users can also adjust the timeline by using the year slider to observe trends and patterns of UFO sightings over time. When a state is selected, the nationwide map will only display sightings for that state, while the state map will zoom in on the selected state and show sightings specifically for that region.

---
<iframe src="Map.html" width="100%" height="600px" style="border:none;"></iframe>
---

## Visualization 2: Time Series Line Plot

### Description
This plot shows the trend of UFO reports over time, grouped by two-year intervals. It aggregates the sightings by state and visualizes the number of reports for each state within each year group. Users can filter the data by selecting a specific state from a dropdown and adjusting the year range using a slider.

### Design Choices
- **Encoding:** The X-axis represents the years, grouped into two-year intervals. The Y-axis shows the number of UFO reports per group. Each state is represented by a different color.
- **Interactivity:** 
  - A dropdown menu allows users to select specific states to focus on.
  - A slider allows users to adjust the year group range, enabling them to see trends for different periods.
  - Hovering over the chart provides detailed tooltips showing the number of UFO sightings for the selected year group.

### Data Transformation
- The "Year" data is grouped into two-year intervals to facilitate clearer trend analysis.
- State abbreviations are mapped to full state names for better readability.
- The dataset is cleaned to exclude any rows with missing data for `Date_Time` or `StateName`.

### Interactivity Explanation
- Users can select a state from the dropdown menu to filter the data. 
- The year range slider enables users to focus on specific periods. 
- Hovering over data points displays the exact number of reports for that year group and state, providing further insights into the trends.

---
<iframe src="Linechart.html" width="100%" height="600px" style="border:none;"></iframe>
---

## Visualization 3: UFO Report Counts by Shape

### Description
This plot visualizes the number of UFO sightings reported by shape, grouped by year. Users can adjust the year range using a slider to focus on specific periods. Each bar represents a specific UFO shape, and the height of the bar corresponds to the number of sightings for that shape within the selected year group.

### Design Choices
- **Encoding:** 
  - The X-axis represents the different UFO shapes.
  - The Y-axis represents the number of reports for each shape.
  - The color encoding differentiates the shapes with distinct colors.
- **Interactivity:** 
  - A slider allows users to adjust the year group range, enabling them to explore the data across different periods.
  - Hovering over each bar displays the exact number of sightings for the respective UFO shape and year group.

### Data Transformation
- The "Year" data is grouped into two-year intervals to facilitate clearer trend analysis.
- Only rows with valid UFO shapes and state names are included in the final dataset.
- The dataset is grouped by `Shape` and `Year_Group` to calculate the count of reports for each combination.

### Interactivity Explanation
- The slider allows users to filter the data by year group, focusing on specific periods of time.
- Hovering over each bar provides additional insights by showing the exact count of UFO sightings for each shape and year group.

---
<iframe src="BarChart.html" width="100%" height="600px" style="border:none;"></iframe>

---

## Links

- [The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)
- [The Analysis](https://github.com/peteoyhh/peteoyhh.github.io/blob/main/ufo-analysis/Workbook.ipynb)
