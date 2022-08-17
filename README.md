# Mongo Queries Practice
For Below Questions, use data provided with the ‘restaurants.json’ file and load it to a MongoDB instance.

## [MongoDB CheetSheet](https://www.mongodb.com/developer/products/mongodb/cheat-sheet/#crud)

- How to load JSON file to MongoDB instance?
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```  
<br>
<br>
<br>


1. Write a MongoDB query to display all the documents in the collection `restaurants`.
```js
db.restaurants.find({})
```
<br>
<br>
<br>

2. Write a MongoDB query to display the fields `restaurant_id`, `name`, `borough`, and `cuisine` for all the documents in the collection `restaurant`.
```js
db.restaurants.find({},{restaurant_id:true, name:true, borough:true,cuisine:true})
```
<br>
<br>
<br>

3. Write a MongoDB query to display the fields `restaurant_id`, `name`, `borough`, and `cuisine`, but exclude the field `_id` for all the documents in the collection `restaurant`.
```js
db.restaurants.find({},{_id:0,restaurant_id:true, name:true, borough:true,cuisine:true})
```
<br>
<br>
<br>

4. Write a MongoDB query to display the fields `zip code`, but exclude the field `_id` for all the documents in the collection `restaurant`.
```js
db.restaurants.find({},{_id:0,'address.zipcode':true})
```
<br>
<br>
<br>

5. Write a MongoDB query to display all the restaurants which are in the `borough` **Brooklyn**.
```js
db.restaurants.find({borough:"Brooklyn"},{ name:true, borough:true,cuisine:true})
```
<br>
<br>
<br>

6. Write a MongoDB query to display the first **5 restaurants** which are in the `borough` **Brooklyn**.
```js
db.restaurants.find({borough:"Brooklyn"},{ name:true, borough:true,cuisine:true}).limit(5)
```
<br>
<br>
<br>

7. Write a MongoDB query to display the **next 5 restaurants** after skipping the first 5 which are in the `borough` **Brooklyn**.
```js
db.restaurants.find({borough:"Brooklyn"},{ name:true, borough:true,cuisine:true}).skip(5).limit(5)
```
<br>
<br>
<br>

8. Write a MongoDB query to find the restaurants that achieved a score of more than 70.
```js
db.restaurants.find({borough:"Brooklyn"},{ name:true, borough:true,cuisine:true})
```
<br>
<br>
<br>

9. Write a MongoDB query to find the restaurants that achieved a score, of more than 70 but less than 100.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

10. Write a MongoDB query to find the restaurants which do not prepare any cuisine of ‘American’ and achieved a grade point ‘A’ not belonging to the borough Brooklyn. The document must be displayed according to the cuisine in descending order.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

11. Write a MongoDB query to find the restaurants which belong to the borough Bronx and prepared either American or Chinese dishes.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

12. Write a MongoDB query to find the restaurant Id, name, borough, and cuisine for those restaurants which prepared dishes except ‘American’ and ‘Chinese’ or the restaurant’s name begins with the letter ‘Sea’.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

13. Write a MongoDB query to arrange the name of the cuisine in ascending order and for that same cuisine, the borough should be in descending order.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

14. Write a MongoDB query to find the restaurant Id, name, and grades for those restaurants which achieved a grade of “A” and scored 11 on an ISODate “2013–09–11T00:00:00Z” among many of the survey dates.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

15. Write a MongoDB query to arrange the name of the restaurants in ascending order along with all the columns.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>

16. Write an aggregation pipeline to count the number of restaurants in the borough “Bronx” for each cuisine type. Display the number of restaurants that prepare Caribbean cuisine. A single query is expected that satisfies all the above requirements.
```js
mongoimport --jsonArray --db day44 --collection restaurants --file restaurants.json
```
<br>
<br>
<br>
