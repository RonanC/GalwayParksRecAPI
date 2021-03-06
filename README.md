###### Semantic Web and Linked Data - Project
# Galway Parks and Recreation API
**by Ronan Connolly**  

![Parks and Recreation Logo](https://upload.wikimedia.org/wikipedia/commons/4/4d/Parks_And_Recreation_Logo.png "Parks and Recreation")

Contents:
---------
1. About
2. Datasets used
3. How to Query the API
4. Example use of the API
5. Tools & Environment used
6. Installation
7. References
8. Team
  
1 - About
---
The aim of this project is to showcase the use of a node api using two or more open Irish datasets  
The [project](https://gist.github.com/ianmcloughlin/53d5f1655bc276373625) is for Dr Ian Mc'Loughlin, Semantic Web & Linked Data Module, GMIT.    
  
I chose irish datasets in relation to [Arts, Culture and Heritage](https://data.gov.ie/data/search?res_format=CSV&theme-primary=Arts).  
  
I chose this theme/topic due to the vast interest people have in finding and exploring local parks, protected buildings, playgrounds, churches and other places.  
  
Many people want explore but they just don't know about all these amazing structures and places around them.  
This api will open this data up for people to consume.  
  
A website with google maps integration, mapping the co-ordinates from this api would be a perfect mix.  
  
With all the talk of [Galway 2020](http://galway2020.ie/en/), I think this api is fitting.  
  
![park](http://www.destateparks.com/images/parks/alapocas-run/alapocas-run.jpg "Park")  
  
2 - Datasets used
---
**Arts, Culture and Heritage Section at [Data.gov.ie](https://data.gov.ie/data)**  
https://data.gov.ie/data/search?res_format=CSV&theme-primary=Arts  
  
**The first dataset:**  
[Community_Facilities_2012_Galway_County](https://data.gov.ie/dataset/community-facilities-2012-galway-county)  
  
**Second:**  
[Galway_County_Record_of_Protected_Structures](https://data.gov.ie/dataset/galway-county-record-of-protected-structures)  
  
**Third (possibly):**  
[Playgrounds_County_Galway](https://data.gov.ie/dataset/playgrounds-county-galway)  
  
3 -  How to Query the API
---
It's a RESTful api with self-describing urls.  
With which you can use the GET, PUT, POST and DELETE HTTP verbs on to do various actions.  
When the urls are queried a JSON object will be passed back.  
  
### general actions  
 - server.com/  
 - server.com/facilities  
 - server.com/playgrounds  
 - server.com/protected_buildings  
  
### specific actions  
 - server.com/:id
 - server.com/facilities/:id
 - server.com/playgrounds/:id
 - server.com/protected_buildings/:id
  
  
4 - Example use of the API
---
### Basic api message  
**req**  
```
server.com/  
```
**res**  
```json
{"message": "Welcome to the parks and recreation API"}
```

### Retrieves all items  
**req**  
```
server.com/playgrounds  
```
**res**  
```json
[{"id": "0", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"},
{"id": "1", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"},
{"id": "2", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"},
{"id": "3", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}]
```
  
### Specific api query  
**req**   
```
server.com/playgrounds/3    
```
**res**  
```json
{"id": "3", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}, {"id": "1", "x": "-1104192", "y": "7056858", "location": "Roundstone (Cloch na Ron)", "area": "West Galway - Conamara", "name": "Roundstone Village, Connemara", "age_group": "0 to 16 Years", "Activities": "Climber and Slide, Climber with Rope, Flat Swings, Cradle Swings, Crazy Goose, Springer, Spring SeeSaw, Platform & Slide"}
```
  
5 - Tools & Environment used
---
### API  
 - Created the web service with node, npm, express
 - MongoDB database
 - Deployed to Heroku
 - Used datasets as listed above from Data.gov.ie, Arts, Culture and Heritage Section
  
### Front-end website  
 - Created a front end web app with angular to consume the api
 - Bootstrap
 - Google Maps API
  
6 - Installation
---
### Dependencies  
Once you have cloned the git repo, you need to run the 'npm install' command.  
This will install all the depencies that are listed in the package.json file.
```sh
> npm install
```

7 - References
---
- I adapted some MEAN stack code from the [Getting MEAN](https://www.manning.com/books/getting-mean-with-mongo-express-angular-and-node) book for the front end website that is consuming this API.
  
8 - Team
---
This project was created by Ronan Connolly, Software Development student in fourth year, term 1, GMIT.  
<a href="http://ronanconnolly.ie"><img src="https://github.com/RonanC/DodgySpike/blob/master/PromoImages/Ronan.png" width="100px" height="100px" title="Ronan" alt="Ronan Image"/></a>
