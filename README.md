# dibs

an app for offering things up and letting people call dibs on it

## Tech Used

* [MongoDB 3.6's Change Streams](https://docs.mongodb.com/manual/changeStreams/)
* [Apollo GraphQL](https://www.apollographql.com/)
  * [Apollo Server](https://www.apollographql.com/docs/apollo-server/)
  * [Apollo React](https://www.apollographql.com/docs/react/)
* [React](https://reactjs.org/)
* [emotion](https://emotion.sh/)

## Development instructions

### Setup

#### You'll need to have already installed

1.  MongoDB 3.6+
2.  Node 8+

#### Instantiate the database

```
mkdir db
mongod --port 27017 --dbpath $(pwd)/db --replSet rs0
# instantiate the replica set. only need to run this one time.
mongo --eval "rs.initiate()"
```

#### Install deps

```
npm install
```

### Dev workflow

#### Start Mongo

```
npm run mongo
```

Keep the process open.

#### Start server and client

```
npm start
```

## Features TODO

* Add spinner when a user creates a dib, and when a user claims a dib
* Location of Dib.
* Price/bounty of Dib.
* Auth with Google
* Real-time comments on a Dib
* Able to edit Dibs that you created.
* Able to un-claim a Dib if you're the creator of the dib.
* Steal more features from eBay.
