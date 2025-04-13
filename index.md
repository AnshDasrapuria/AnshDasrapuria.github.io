---
layout: default
title: UFO Sightings Visualization
---

# UFO Sightings Data Visualization

## 1. UFO Sightings Over the Years

This visualization shows the number of UFO sightings reported annually from the available dataset. It highlights how interest in UFOs evolved over time, with a clear increase in reports around the late 20th century and early 2000s. To prepare the data, I converted the `date_time` column to datetime format and extracted the `year` to aggregate the number of sightings per year. I used a line chart with `year` encoded as a quantitative variable on the x-axis, and `count` of sightings encoded as a quantitative variable on the y-axis. This choice makes the trends more legible, especially after switching from ordinal to continuous scaling. The x-axis was customized using `tickCount` to reduce overlap, and the chart includes tooltips to show year-specific values on hover. This visualization was built from scratch for this assignment and is not reused from Homework #5.

## 2. UFO Sightings by Shape and Location

This second visualization maps UFO sightings based on latitude and longitude, using color to represent the reported shape of each UFO. I used a scatter plot where latitude and longitude were encoded as quantitative axes, and the `shape` variable was encoded using a nominal color scheme. This design helps visually separate different types of sightings across regions. Before visualizing, I filtered out rows with missing geographic data to ensure accuracy. The plot uses `.interactive()` to support panning and zooming, and also includes tooltips that provide contextual information like the city, state, timestamp, and shape of the UFO reported. The color scheme was chosen to make different shapes easy to distinguish. While `.interactive()` allows spatial exploration, the added tooltips offer a richer, clearer experience when analyzing individual sightings.

## Interactivity Discussion

The first visualization includes tooltips that enhance user understanding by showing the exact number of sightings when hovering over a given year. This interaction helps explore trends without crowding the visual space. The second visualization is also interactive, with both pan/zoom and informative tooltips. While `.interactive()` supports geographical navigation, the detailed hover tooltips truly add value by revealing individual sighting information, making the data exploration experience both intuitive and insightful.

---

## View the Data and Notebook

- [The Data](https://raw.githubusercontent.com/AnshDasrapuria/HW5.1/main/cleaned_ufo_data.csv)
- [The Analysis](https://github.com/AnshDasrapuria/HW5.1/blob/main/code.ipynb)
