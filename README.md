# Hermes (general authentication micro-service)

User subscription management micro-service for websites. Build in React components on a semi-transparent background sitting on top of your app during
authentication.

# What is general authentication micro-service ?
In a microservices architecture, a user interacts with a collection of services, each with a potential need of knowing who the user is. A naive solution is to apply the same pattern in a microservices system as in a monolithic system, but then the problem of how to give all services access to the user data arises. When using a shared user database, updating the schema becomes a hard problem since all services must be upgraded at the same time. When distributing the same data to all services, there is the problem of how to make each service know when a user is authenticated.

## GUI Demo

Showing off some build in screens  _(ReactJs, GraphQL client Apollo)_

![Demo](https://media.giphy.com/media/26gR1OLV9ebnFgjQI/giphy.gif)

## Installation overview

 1. [Installing/Configuration of PostgreSQL back-end and DB objects creation](docs/installing-postgresql96-centos7.md)

 Simple usage

 ```javascript

   import { hermes } from 'hermes';
   import { app } from 'express';

   app.use('/usr-auth', hermes({
     mailGunApiKey: 'ZERSFCSzerzer235', // your api key from mailgun
     dbName:'bookbarter',
     dbUser:'bookbarter',
     dbPassword: 'xxxxx'
   });
 ```

