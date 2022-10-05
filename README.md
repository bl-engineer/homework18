# homework18: Social Network API

## Your Task

MongoDB is a popular choice for many social networks due to its speed with large amounts of data and flexibility with unstructured data. Over the last part of this course, you’ll use several of the technologies that social networking platforms use in their full-stack applications. Because the foundation of these applications is data, it’s important that you understand how to build and structure the API first.

Your Challenge is to build an API for a social network web application where users can share their thoughts, react to friends’ thoughts, and create a friend list. You’ll use Express.js for routing, a MongoDB database, and the Mongoose ODM. In addition to using the [Express.js](https://www.npmjs.com/package/express) and [Mongoose](https://www.npmjs.com/package/mongoose) packages, you may also optionally use a JavaScript date library of your choice or the native JavaScript `Date` object to format timestamps.

No seed data is provided, so you’ll need to create your own data using Insomnia after you’ve created your API.

Because this application won’t be deployed, you’ll also need to create a walkthrough video that demonstrates its functionality and all of the following acceptance criteria being met. You’ll need to submit a link to the video and add it to the README of your project.

## User Story

```md
AS A social media startup
I WANT an API for my social network that uses a NoSQL database
SO THAT my website can handle large amounts of unstructured data
```

## Acceptance Criteria

```md
GIVEN a social network API
WHEN I enter the command to invoke the application
THEN my server is started and the Mongoose models are synced to the MongoDB database
WHEN I open API GET routes in Insomnia for users and thoughts
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete users and thoughts in my database
WHEN I test API POST and DELETE routes in Insomnia
THEN I am able to successfully create and delete reactions to thoughts and add and remove friends to a user’s friend list
```


### API Routes

**`/api/users`**

* `GET` all users

* `GET` a single user by its `_id` and populated thought and friend data

* `POST` a new user:

```json
// example data
{
  "username": "lernantino",
  "email": "lernantino@gmail.com"
}
```

* `PUT` to update a user by its `_id`

* `DELETE` to remove user by its `_id`

**BONUS**: Remove a user's associated thoughts when deleted.

---

**`/api/users/:userId/friends/:friendId`**

* `POST` to add a new friend to a user's friend list

* `DELETE` to remove a friend from a user's friend list

---

**`/api/thoughts`**

* `GET` to get all thoughts

* `GET` to get a single thought by its `_id`

* `POST` to create a new thought (don't forget to push the created thought's `_id` to the associated user's `thoughts` array field)

```json
// example data
{
  "thoughtText": "Here's a cool thought...",
  "username": "lernantino",
  "userId": "5edff358a0fcb779aa7b118b"
}
```

* `PUT` to update a thought by its `_id`

* `DELETE` to remove a thought by its `_id`

---

**`/api/thoughts/:thoughtId/reactions`**

* `POST` to create a reaction stored in a single thought's `reactions` array field

* `DELETE` to pull and remove a reaction by the reaction's `reactionId` value


## Review

You are required to submit BOTH of the following for review:

* A walkthrough video demonstrating the functionality of the application and all of the acceptance criteria being met.

* The URL of the GitHub repository. Give the repository a unique name and include a README describing the project.

## Random Screenshots of Result: Social Network API

<img width="2152" alt="Screen Shot 2022-10-05 at 5 16 43 AM" src="https://user-images.githubusercontent.com/15242022/194029080-0b2e46f9-4dd2-426d-9964-682c8478359a.png">

<img width="2152" alt="Screen Shot 2022-10-05 at 5 16 54 AM" src="https://user-images.githubusercontent.com/15242022/194029350-4cfc9b33-5b83-45bb-9025-405a49091bab.png">

<img width="2152" alt="Screen Shot 2022-10-05 at 5 17 29 AM" src="https://user-images.githubusercontent.com/15242022/194029417-04a95b2d-8676-488d-96f0-de172f1b08ad.png">

<img width="2152" alt="Screen Shot 2022-10-05 at 5 18 57 AM" src="https://user-images.githubusercontent.com/15242022/194029501-4843b4e6-1060-4a7a-8a4a-e90f45aa0885.png">

<img width="2152" alt="Screen Shot 2022-10-05 at 5 20 14 AM" src="https://user-images.githubusercontent.com/15242022/194029557-40f65486-e693-4058-821d-fc2b59c38fe5.png">

<img width="2141" alt="Screen Shot 2022-10-05 at 5 21 34 AM" src="https://user-images.githubusercontent.com/15242022/194029623-21a7c9b7-18cd-4034-9f82-5faa488457a1.png">


## 3 Walktrough Videos: Social Network API

## Walktrough Videos 1:
https://drive.google.com/file/d/1WOTvEBl2QW5M_ECXZBO977nb5OnaWlSe/view

## Walktrough Videos 2:
https://drive.google.com/file/d/1DrC5Ub3DEyAjL1bREt5sDr5R8GythtZ6/view

## Walktrough Videos 3:

---
© Done by: Bocar Ly
Assigment: Week 18 Homework 

[Github_URL](https://github.com/bl-engineer/homework18/)
