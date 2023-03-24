# Flask-Blog-Project


Let's say we have an URL / Function / Package which receives some data and returns data accordingly, we can call it an *API (Application Programming Interface)*

Example 2 - In google search bar you give some inputs or search query and it returns you the results accordingly, so google is using an API to receive search parameters and returns you the result based on those parameters.

Suppose You're a developer and working in a firm related to weather forcasting and there is a team which collects all the data related to weather. Now they need a way to store that data into database and also share with the world via a mobile app or a website.

Now you as a developer will provide them an endpoint (an URL) which accepts the data (let's say, that data contains a date and the temprature) and store that data into database. So other developers who will design the front-end (Mobile app, Website) will use that endpoint to store the data into database. In the end, that team can use the website or mobile app to store that data.

Now to share that data with the world, you'll create another endpoint that will accept a date and will return the temprature fetched from the database on that particular date. Again the mobile app and web developers will use that end-point to fetch the data and show it on their app where the world can see that data.

![image](https://user-images.githubusercontent.com/124021133/227544656-73402d87-9259-4dfe-9d35-bc435572bc9d.png)


*HTTPS Methods*

*GET* - We make GET type of request when we want to receive something from the web server like a JSON Object, HTML or bytecode for a file.
Example - GET http:/localhost:5000/item/1 or GET https://google.com/images  , when you type something relevent on google it is get request .

*POST* - When we want to create something, we use this method.
Example - POST http://localhost:5000/item with body  , when you order something from amazon it is a post request .


```
{
    "name":"School bag",
    "id": 2,
    "price":670
}
```

*PUT* - When we want to update or replace an existing record.
Example - PUT http://localhost:5000/item/ with body
```
{
    "name":"School bag",
    "id": 2,
    "price":650
}
```
*DELETE* - When we want to delete a record.
Example - DELETE http://localhost:5000/item/2

There are few other HTTP Methods are available like COPY, HEAD, PATCH, OPTIONS and many more.

Difference between an API and REST API-

While an API is a set of functions / procedures that allows a developer to share the features of an application with another in the way of packages/URL/functions/applications. But on other hand Rest APIs are more limited, It follows some rules and guidelines for applications on the web (HTTP). There are alot of other ways to build a web API, but REST is more effiecient and standard way of doing it which makes it easy for other developers or third parties to understand the functionality of an API very easily. Unlike common APIs, we don't need to install anything software, libraries or pacakges to use those APIs. Using REST APIs, one can return the data in the form of JSON, XML, YAML and others.

 Principles that make an API a REST API
 
* Uniform Interface - APIs should follow a common interface, if a developer knows how to use one of your API, he should be able to work with other API of yours related to that resource without looking into the documentation.

* Client-Server - There should be no dependency between Client and Server, they should only communicate through the provided URI.

* Stateless - No information stored in between, No history, No session. Each request will be treated as new request. Authentication or Authorization details will only be passed in the request itself.

* Cacheable (When possible) - Improves the speed by storing cache. It can be implemented on both sides (Client or Server)

* Layered System -  A client can't ordinarily tell whether it is connected directly to the end server or to an intermediary along the way.

* Code on Demand - You can also send the code while calling an API to render the widgets dynamically.

To explain all the points in simple words lets take a example i) you have get put delete and post request without using any documentation you can perform all these operations ii) if any changes takes place in fronted then it should not affect backend and any change in backend should not affect frontend . iii) Suppose you need authentication to access some data then authentication will happen through api not through backend so any data about you will not stored . iv)Cacheable will happens sometime it will fast your data accessing . vi) code can be send through api if needed .
