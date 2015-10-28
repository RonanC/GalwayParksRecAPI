# Galway Parks and Recreation API
**by Ronan Connolly**  
Project that showcases the use of a node api using two open Irish datasets 

I chose irish datasets in relation to [Arts, Culture and Heritage](https://data.gov.ie/data/search?res_format=CSV&theme-primary=Arts)

I chose this theme/topic due to the vast interest people have in finding and exploring local parks, protected buildings, playgrounds, churches and other places.

Many people just don't know about these places.
This api will open this data up for people to consume.

A website with google maps api mapping the co-ordinates from the api would be perfect.

With all the talk of [Galway 2020](http://galway2020.ie/en/), I think this api is fitting.


![park](http://www.destateparks.com/images/parks/alapocas-run/alapocas-run.jpg "Park")

## Datasets used
**Link to the Community Facilities Data Sets on Data.Gov.IE:**  
https://data.gov.ie/dataset/community-facilities-2012-galway-county

**The first dataset:**  
[Community_Facilities_2012_Galway_County](https://data.gov.ie/dataset/community-facilities-2012-galway-county)  

**Second:**  
[Galway_County_Record_of_Protected_Structures](https://data.gov.ie/dataset/galway-county-record-of-protected-structures)  

**Third (possibly):**  
[Playgrounds_County_Galway](https://data.gov.ie/dataset/playgrounds-county-galway)  

## How to Query the API
It's a RESTful api with self-describing urls.
With which you can use the GET, PUT, POST and DELETE HTTP verbs on to do various actions.
When the urls are queried a JSON object will be passed back.

### general actions
server.com/
server.com/facilities
server.com/playgrounds
server.com/protected_buildings

### specific actions
server.com/:id
server.com/facilities/:id
server.com/playgrounds/:id
server.com/protected_buildings/:id


## Example use of the API
### Basic api message
**req**  
server.com/  
**res**  
{"message": "Welcome to the parks and recreation API"}

### Retrives all items
**req**  
server.com/playgrounds  
**res**  
[{"id": "0", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}, {"id": "1", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}, {"id": "2", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}, {"id": "3", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}]

### Specific api query
**req**  
server.com/playgrounds/3  
**res**  
{"id": "3", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}, {"id": "1", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}

## Other Information
 - I will deploy this (node) api on Heroku
 - On a seperate Heroku dyno I will deploy a front end angular web app to consume the node api

## References
- I adapted some MEAN stack code from the [Getting MEAN](https://www.manning.com/books/getting-mean-with-mongo-express-angular-and-node) book for the front end website that is consuming this API.
This front end api is using an AJAX SPA created in Angular. It's using Bootstrap and the Google Maps API. It's deployed on Heroku.
