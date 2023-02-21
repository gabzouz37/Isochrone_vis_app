# Isochrone Project - Communicating Data & Statistics

## Description

Isochrones delimit lines of equal travel time from an origin. They are important to investigate how well connected a location is and have many applications, from improving transport networks to any location-based optimisation. This project presents a visualization tool that plots isochrones from an origin using a set of user-defined parameters. The isochrones are generated using the TravelTime API (https://traveltime.com/). The visualization is largely inspired by byollin's work (https://github.com/byollin/Isolines), but uses an more precise API and provides additional data to the user such as the area of the isochrones.


## Usage
To use the interactive map, put your API key information (free from TravelTime website) in the api_keys.json file and run the server.R file. This will generate a window presenting a map and the user menu on the left, as seen in the picture below. 

![image](https://user-images.githubusercontent.com/73693706/220354645-8d04dccf-9ca8-4e46-a2bc-ffa989b5252c.png)


The menu allows the user to select 
- Origin of the isochrone (latitude-longitude coordinates or by clicking on the map), 
- Mode of transport (among driving, public transport, cycling, and walking),
- Departure time (takes into account traffic and scheduled public transport), 
- Times associated with the desired isochrones (minimum range representing the smallest isochrone, maximum the largest, and interval size the minute interval between these ranges for which the user wants isochrones). 

Once these parameters are set, use the request isolines button to generate the visualisation.

This button will generate and plot the desired isochrones in relation to the defined parameters as seen in the image below. The area and associated time of each isochrone is visible when passing the mouse over it, as well as the area of the polygon under consideration (isochrones are often composed of multiple polygons due to some areas being inaccessible during the set time).

![image](https://user-images.githubusercontent.com/73693706/220373966-293b3597-e88c-47e8-a643-362681c73948.png)

The numerical results can also be downloaded using the download results button that appears once the isochrones are generated. 


## Results

The download results button allows the user to download a zip file that contains the numerical results of the generated isochrones. The zip file contains 4 files in different formats containing the polygons composing the isochrones, and an additional results file in csv format where each row represents a polygon composing an isochrone, with the isochrone ID, origin, associated time, transport mode used, area of the polygon and total area of the isochrone it is a part of.




