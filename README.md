# assignment-2-29-affansidd-joshuaemerson
assignment-2-29-affansidd-joshuaemerson created by GitHub Classroom

# Project URL
URL: https://group-29-covid-api.herokuapp.com/

Note: The time series name "TEST" is already pre defined in our database for our unit tests. The same applies for daily report as well. All other names are available to use.

## Pair Programming 

When using the pair programming practice, my partner and I were able to implement every feature of the API as described on swaggerhub. Along the way, we faced several obstacles which were often in the form of asynchronous JavaScript and difficulties working with our MongoDB instance. We solved these challenges by dividing the work in a way that best suited our individual skill sets. Affan is well versed in using Mongo and was thus served as the driver for this section and was able to explain the methodologies and techniques he implemented to solve the problems relating to Mongo. In the meantime, the navigator in this situation absorbed the information presented and chipped in whenever debugging was required. On the other hand, for issues relating to asynchronous JavaScript, Joshua served as the driver in this situation as he has more experience using JavaScript. The navigator was able to better understand how to deal with asynchronous javascript calls which played a crucial part in developing this API. We also implemented this pair programming dynamic to complete the functionality of the routes defined in the API. Affan served as the driver when developing the routes for the time_series data while Joshua served as the driver when working on the routes for the daily_reports data. When we ran into issues, we debugged our code together rather than having each team member debug their individual code alone. This allowed us to solve our problems in a more efficient manner and improve the overall development experience.

Overall, the pair programming paradigm was a success as we were able to complete the full specification of our API without many obstacles. Moreover, the pair programming dynamic allowed us to play to each other's strengths and allowed us to grow as software developers. One of the aspects of pair programming which we liked was that it allowed us to make equal contributions to the code base since we alternated between the driver and navigator positions. Moreover, pair programming made the debugging process much simpler as having two sets of eyes to spot issues and test the code greatly reduced the amount of time wasted. One aspect of pair programming that was difficult to cope with at times was the difficulty in scheduling a time to meet so that we could work on the project concurrently. 

## Programming Design
In terms of the implementation details, we decided to create a Node.js app that uses an Express backend and MongoDB as the database of choice. We choose to work with Express as both of us have used this framework in previous projects and applications and thus have a certain level of familiarity with the technology. Moreover, Express is relatively lightweight and allowed us to develop a Node.js application quickly and easily. We choose MongoDB as our database as a non-relational database was easier to both set up and use based on the specifications of the COVID19 API on swaggerhub. Likewise, it is very simple to connect Express with MongoDB which made CRUD operations on our database straightforward to complete. We stored our data in a JSON format on our database where each row in the CSV file represented an object in the database. We choose to set the keys in our JSON data to match the headers in the example CSV files. For the time-series data, we kept all the dates in our object since we would have to query these dates later on. In the daily report's data, we removed FIPS, Admin2, Incident_Rate, and Case_Fatality_Ratio columns since these values are never queried. Express also made it very simple to define routes on our application based on HTTP methods and URLs which ultimately helped us in the construction of our endpoints. Our endpoints are modeled after the specifications described on swaggerhub and thus return the appropriate responses to the user based on whether their request to our endpoint was successful or not. Our application handles all of the specified endpoints and performs the necessary error checking to determine whether the users' request is valid or not. In order to improve the organization of the overall codebase, we made sure that the cohesion of our code was high by ensuring components were self-contained, had a defined purpose, and belonged together. Likewise, the coupling between our different components was low since the different components were not heavily dependent on one another. This allowed us to make changes in certain parts of the codebase that did not impact the functionality of other components. Note: our group did not add our YAML file for the CI integration on GitHub actions on the main branch but did so on our forked branch as mentioned in the handout.

## Test Coverage Values
The images relating to the test coverage values are shown below

Test Coverage Values in Shell:
![image](https://user-images.githubusercontent.com/60104396/160253796-a8ae4b4d-adda-424b-9de1-93a847c1eeb2.png)

Test Coverage Values HTTP version:
![image](https://user-images.githubusercontent.com/60104396/160253831-72ef393b-d81d-4de8-9c62-51b996968842.png)

## CD Integration
The images relating to CD Integration are also provided below

CD Summary on Github Actions:
![image](https://user-images.githubusercontent.com/60104396/160253865-d14573bd-55e8-4298-b724-ac714f231c98.png)

CD on Github Actions expanded:
![image](https://user-images.githubusercontent.com/60104396/160253873-9d119970-b2ef-45b7-a147-3b986e67003a.png)
![image](https://user-images.githubusercontent.com/60104396/160253882-22a90506-e451-4f4b-a313-bea86a93fba2.png)


CD (deploy) being shown on Github Actions:
![image](https://user-images.githubusercontent.com/60104396/160253899-2b2e182e-2705-4f15-819c-ab01fc779d29.png)







