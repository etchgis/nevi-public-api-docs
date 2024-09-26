---
title: NEVI API
layout: home
---

## API Endpoints

- **locations.js**: This endpoint will send data from all current locations in the database. The query would look something like this: [https://api.etch.app/nevi/locations]

- **locationID.js**: This endpoint will send data from a specific location specified with an ID. All of the data for the location's ports and related connectors will be sent. The ID that needs to be used is the one correpsonding to the primary key attribute in the database labled "id". Here is an example of this: [https://api.etch.app/nevi/locations/53]

- **sessions.js**: This endpoint will send session data from a sepcified amount of time. There are two ways to query this endpoint.

    The first one is through date time format that may look something like this: [https://api.etch.app/nevi/locations/53/session?date_from=2024-04-09T00:00:00.000Z&date_to=2024-04-11T00:00:00.000Z]. All sessions in the database between this time period will be taken into account for the totals and averages calculated. The "date_to" param is not needed, the endpoint can just be queries using "date_from" and all sessions from that time period until now will be represented in the calculations.

    The second way to query the endpoint is by a specified timeframe, which looks like this: [https://api.etch.app/nevi/locations/53/session?timeframe=week]. The timeframe can be sepcified by day, week, month, and year. For the day timeframe session data is summed in hour intervals, for week timeframe day intervals, for month timeframe week intervals, and for year timeframe month intervals.
