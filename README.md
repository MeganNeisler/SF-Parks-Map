# San Francisco Interative Parks Map

An interactive map of some popular parks in San Francisco with view of the city. The map includes makrers indicating each park's location, which the user can click to access the park's website.

## Getting Started
This was created using leaflet for R 

```
install.packages("leaflet")
library(leaflet)
```
Once installed, you can use this package within R markdown documents or shiny applications.

## Data

A dataframe was created using the latitudes and longitudes of San Francisco city parks collected from Google Maps. I also created a list of websites to the parks.

## Example

The interative map includes tiles to mark the park locations and map markers with links to each park website.
```
sfpark_map <- df %>% 
  leaflet() %>%
  addTiles() %>%
  addMarkers(icon = sfparkIcon, popup = sfparkSites)
sfpark_map

```

## Author
* Megan Neisler

## Acknowledgements
* This was completed as part of Coursera's Johns Hopkins Data Science Specialization.
