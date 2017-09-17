# San Francisco Interactive Parks Map

An interactive map of some popular parks in San Francisco with view of the city. The map includes makrers indicating each park's location, which the user can click to access the park's website.

## Getting Started
This was created using leaflet for R 

```
install.packages("leaflet")
library(leaflet)
```
Once installed, you can use this package within R markdown documents or shiny applications.

## Data

* df: A dataframe of the latitudes and longitudes of San Francisco city parks collected from Google Maps. 
* sfparkIcon: SF park logo obtained from the [San Francisco Recreation and Park Website](http://sfrecpark.org/wp-content/uploads/SF_RecPark_Logo4.png)
* sfparkSites: A list of the websites for each park.

## Example

Once you install the leaflet package you can add various layers to the map.  This interative map includes tiles to mark the park locations and map markers with links to each park website. 
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
