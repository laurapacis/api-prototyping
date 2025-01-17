# API Prototyping

## What is an API Prototype?

An API Prototype is a minified version of our API which just returns "hardcoded" data on all routes.

An API prototype therefore works with a very limited structure:
- no database
- no models & schemas
- no controllers
- no middleware (even though can be added already to test validation error responses...)
- no token authentication (even though can be added already...)

## Why an API prototype?

API prototyping helps us to fulfill a common fullstack development concept:

<b>EARLY INTEGRATION</b>

A common issue in fullstack development is a misunderstanding of the DATA EXCHANGE format between frontend & backend.

The whole backend structure HIGHLY depends on the data model (so the data collection and their relationships). Changes of the data model structure often result in changes of the whole backend structure (schemas, routes, controllers, validators, etc)

Quite often the frontend developers have a different expectation of the data to receive from the backend than the backend developers, who maybe will provide the data in the routes differently than expected by the frontend (e.g. other format of date fields, missing fields or unexpected structure or nesting of items). This will result in failed frontend renderings.

An API prototype can help to spot those misunderstandings - which are very normal - early and help clarifying (!) them early before a lot of unnecessary work is done on both sides.

An API prototype usually can be developed much quicker than an actual full-fledged API where we would need to setup the database connection, models, schemas, controllers, middleware etc.

Integrating a minimal API into our frontend instead provides us with very valuable benefits:

- testing the complete flow of information exchange between frontend and backend
  - e.g. sending new items to backend and receiving them back
  - storing received items in state. and redirect to other page

- clarifiying the data exchange formats and resolve misunderstanding between developers early!
  - which data does the frontend expects to get from API in order to render the frontend correctly?
  - the backend can provide routes as early as possible with necessary information
  - data fields & formats can be discussed early, before heave database schemas, models and seed scripts are created
  - once the exchange formats are clarified, the backend developer can implement a database

- test error response handling
  - do we correctly receive errors from backend so we can display them in frontend?

## Samples

Find an example of an API prototype in the folder "server"

Frontend Demo for intergrating the API prototype will follow...
