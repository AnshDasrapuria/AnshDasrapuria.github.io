---
layout: default
title: UFO Sightings Visualization
---

# UFO Sightings Data Visualization

## 1. UFO Sightings Over the Years

This visualization shows the number of UFO sightings reported annually from the dataset. It highlights patterns of increased interest in UFOs over time, particularly a significant spike in the late 1990s and early 2000s. To create this plot, I first converted the `date_time` column to a datetime object and then extracted the `year` to aggregate the number of sightings per year. I used a line chart in Altair with `year` encoded as a quantitative variable on the x-axis and the total `count` on the y-axis. To improve readability, I applied `tickCount` to control label density and added tooltips for hover-based interactivity. No color scheme was applied in order to keep the focus on trend clarity.

<iframe src="charts/chart1.html" width="100%" height="500" style="border:none;"></iframe>

---

## 2. UFO Sightings by Shape and Location

This second visualization shows UFO sightings plotted on a map by geographic coordinates, colored by the shape of the reported UFO. Latitude and longitude were used as quantitative encodings on the y and x axes respectively. I dropped rows with missing geolocation data to ensure accurate plotting. The `shape` variable was encoded as a nominal scale with a color scheme that distinguishes each shape clearly. I included tooltips to display details such as city, state, time, and shape on hover. In addition to Altair’s built-in `.interactive()` for zoom/pan, the tooltip interactivity makes it easier to explore individual sightings in different regions, enhancing both clarity and depth of insight.

<iframe src="charts/chart2.html" width="100%" height="500" style="border:none;"></iframe>

---

## Interactivity

In the first chart, interactivity is provided via hover tooltips, allowing users to explore specific years and their corresponding number of sightings. This goes beyond basic `.interactive()` features by offering targeted value feedback. The second chart enhances user experience through hover tooltips and pan/zoom interactivity, allowing geographic exploration and identification of sighting details at a granular level.

---

## Homework #5 Overlap

This project uses the same UFO dataset, but **both plots are completely different** from Homework #5. The first plot is a time-series analysis using a line chart with yearly aggregation, and the second is a geospatial visualization using shape and location encodings. There is no reused code or visualization type from the prior homework — all charts were re-built using Altair for this web-focused assignment.

---

## View the Data and Notebook

- [The Data](cleaned_ufo_data.csv)  
- [The Analysis](https://github.com/AnshDasrapuria/AnshDasrapuria.github.io/blob/main/code.ipynb)
