---
title: Documentation
layout: home
---

## API Endpoints

- **locations**: This endpoint will query data from all current locations available. [https://api.etch.app/nevi/locations](https://api.etch.app/nevi/locations){:target="_blank"}

- **location**: This endpoint will query data from a specific location by it's ID. All of the data for the location's ports and related connectors are included. The ID that needs to be used is the one included in the locations endpoint mentioned above, i.e. "id". Example: [https://api.etch.app/nevi/locations/53](https://api.etch.app/nevi/locations/53){:target="_blank"}

- **sessions**: This endpoint will query session data from a sepcified duration of time. There are two ways to query this endpoint.

    The first one is with the ISO date time format which should look something like this: [https://api.etch.app/nevi/locations/53/session?date_from=2024-04-09T00:00:00.000Z&date_to=2024-04-11T00:00:00.000Z](https://api.etch.app/nevi/locations/53/session?date_from=2024-04-09T00:00:00.000Z&date_to=2024-04-11T00:00:00.000Z){:target="_blank"}. All sessions during the specified duration will be taken into account for the totals and averages calculated. The "date_to" param is not needed, the endpoint can just be queried using "date_from" and all sessions from that time period until now will be represented in the calculations.

    The second way to query the endpoint is by a specified timeframe, which looks like this: [https://api.etch.app/nevi/locations/53/session?timeframe=week](https://api.etch.app/nevi/locations/53/session?timeframe=week){:target="_blank"}. The timeframe can be sepcified by day, week, month, and year. For the day timeframe session data is summed in hour intervals, for week by day intervals, for month by week intervals, and for year by month intervals.
