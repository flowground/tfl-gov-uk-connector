# ![LOGO](logo.png) Transport for London Unified **flow**ground Connector

## Description

A generated **flow**ground connector for the Transport for London Unified API (version v1).

Generated from: https://api.apis.guru/v2/specs/tfl.gov.uk/v1/swagger.json<br/>
Generated at: 2019-05-07T17:44:22+03:00

## API Description

Our unified API brings together data across all modes of transport into a single RESTful API. This API provides access to the most highly requested realtime and status infomation across all the modes of transport, in a single and consistent way. Access to the developer documentation is available at https://api.tfl.gov.uk

## Authorization

Supported authorization schemes:
- API Key- API Key
## Actions

### Gets all accident details for accidents occuring in the specified year

*Tags:* `AccidentStats`

#### Input Parameters
* `year` - _required_ - The year for which to filter the accidents on.

### Gets air quality data feed

*Tags:* `AirQuality`

### Gets all bike point locations. The Place object has an addtionalProperties array which contains the nbBikes, nbDocks and nbSpaces<br/>
>             numbers which give the status of the BikePoint. A mismatch in these numbers i.e. nbDocks - (nbBikes + nbSpaces) != 0 indicates broken docks.

*Tags:* `BikePoint`

### Search for bike stations by their name, a bike point's name often contains information about the name of the street<br/>
>             or nearby landmarks, for example. Note that the search result does not contain the PlaceProperties i.e. the status<br/>
>             or occupancy of the BikePoint, to get that information you should retrieve the BikePoint by its id on /BikePoint/id.

*Tags:* `BikePoint`

#### Input Parameters
* `query` - _required_ - The search term e.g. "St. James"

### Gets the bike point with the given id.

*Tags:* `BikePoint`

#### Input Parameters
* `id` - _required_ - A bike point id (a list of ids can be obtained from the above BikePoint call)

### Gets taxis and minicabs contact information

*Tags:* `Cabwise`

#### Input Parameters
* `lat` - _required_ - Latitude
* `lon` - _required_ - Longitude
* `optype` - _optional_ - Operator Type e.g Minicab, Executive, Limousine
* `wc` - _optional_ - Wheelchair accessible
* `radius` - _optional_ - The radius of the bounding circle in metres
* `name` - _optional_ - Trading name of operating company
* `maxResults` - _optional_ - An optional parameter to limit the number of results return. Default and maximum is 20.
* `legacyFormat` - _optional_ - Legacy Format
* `forceXml` - _optional_ - Force Xml
* `twentyFourSevenOnly` - _optional_ - Twenty Four Seven Only

### Perform a Journey Planner search from the parameters specified in simple types

*Tags:* `Journey`

#### Input Parameters
* `from` - _required_ - Origin of the journey. Can be WGS84 coordinates expressed as "lat,long", a UK postcode, a Naptan (StopPoint) id, an ICS StopId, or a free-text string (will cause disambiguation unless it exactly matches a point of interest name).
* `to` - _required_ - Destination of the journey. Can be WGS84 coordinates expressed as "lat,long", a UK postcode, a Naptan (StopPoint) id, an ICS StopId, or a free-text string (will cause disambiguation unless it exactly matches a point of interest name).
* `via` - _optional_ - Travel through point on the journey. Can be WGS84 coordinates expressed as "lat,long", a UK postcode, a Naptan (StopPoint) id, an ICS StopId, or a free-text string (will cause disambiguation unless it exactly matches a point of interest name).
* `nationalSearch` - _optional_ - Does the journey cover stops outside London? eg. "nationalSearch=true"
* `date` - _optional_ - The date must be in yyyyMMdd format
* `time` - _optional_ - The time must be in HHmm format
* `timeIs` - _optional_ - Does the time given relate to arrival or leaving time? Possible options: "departing" | "arriving"
    Possible values: Arriving, Departing.
* `journeyPreference` - _optional_ - The journey preference eg possible options: "leastinterchange" | "leasttime" | "leastwalking"
    Possible values: LeastInterchange, LeastTime, LeastWalking.
* `mode` - _optional_ - The mode must be a comma separated list of modes. eg possible options: "public-bus,overground,train,tube,coach,dlr,cablecar,tram,river,walking,cycle"
* `accessibilityPreference` - _optional_ - The accessibility preference must be a comma separated list eg. "noSolidStairs,noEscalators,noElevators,stepFreeToVehicle,stepFreeToPlatform"
* `fromName` - _optional_ - An optional name to associate with the origin of the journey in the results.
* `toName` - _optional_ - An optional name to associate with the destination of the journey in the results.
* `viaName` - _optional_ - An optional name to associate with the via point of the journey in the results.
* `maxTransferMinutes` - _optional_ - The max walking time in minutes for transfer eg. "120"
* `maxWalkingMinutes` - _optional_ - The max walking time in minutes for journeys eg. "120"
* `walkingSpeed` - _optional_ - The walking speed. eg possible options: "slow" | "average" | "fast".
    Possible values: Slow, Average, Fast.
* `cyclePreference` - _optional_ - The cycle preference. eg possible options: "allTheWay" | "leaveAtStation" | "takeOnTransport" | "cycleHire"
    Possible values: None, LeaveAtStation, TakeOnTransport, AllTheWay, CycleHire.
* `adjustment` - _optional_ - Time adjustment command. eg possible options: "TripFirst" | "TripLast"
* `bikeProficiency` - _optional_ - A comma separated list of cycling proficiency levels. eg possible options: "easy,moderate,fast"
* `alternativeCycle` - _optional_ - Option to determine whether to return alternative cycling journey
* `alternativeWalking` - _optional_ - Option to determine whether to return alternative walking journey
* `applyHtmlMarkup` - _optional_ - Flag to determine whether certain text (e.g. walking instructions) should be output with HTML tags or not.
* `useMultiModalCall` - _optional_ - A boolean to indicate whether or not to return 3 public transport journeys, a bus journey, a cycle hire journey, a personal cycle journey and a walking journey
* `walkingOptimization` - _optional_ - A boolean to indicate whether to optimize journeys using walking
* `taxiOnlyTrip` - _optional_ - A boolean to indicate whether to return one or more taxi journeys. Note, setting this to true will override "useMultiModalCall".

### Gets a list of all of the available journey planner modes

*Tags:* `Journey`

### Gets a list of valid disruption categories

*Tags:* `Line`

### Gets a list of valid modes

*Tags:* `Line`

### Gets a list of valid ServiceTypes to filter on

*Tags:* `Line`

### Gets a list of valid severity codes

*Tags:* `Line`

### Gets lines that serve the given modes.

*Tags:* `Line`

#### Input Parameters
* `modes` - _required_ - A comma-separated list of modes e.g. tube,dlr

### Get disruptions for all lines of the given modes.

*Tags:* `Line`

#### Input Parameters
* `modes` - _required_ - A comma-separated list of modes e.g. tube,dlr

### Gets all lines and their valid routes for given modes, including the name and id of the originating and terminating stops for each route

*Tags:* `Line`

#### Input Parameters
* `modes` - _required_ - A comma-separated list of modes e.g. tube,dlr
* `serviceTypes` - _optional_ - A comma seperated list of service types to filter on. Supported values: Regular, Night. Defaulted to 'Regular' if not specified

### Gets the line status of for all lines for the given modes

*Tags:* `Line`

#### Input Parameters
* `modes` - _required_ - A comma-separated list of modes to filter by. e.g. tube,dlr
* `detail` - _optional_ - Include details of the disruptions that are causing the line status including the affected stops and routes

### Get all valid routes for all lines, including the name and id of the originating and terminating stops for each route.

*Tags:* `Line`

#### Input Parameters
* `serviceTypes` - _optional_ - A comma seperated list of service types to filter on. Supported values: Regular, Night. Defaulted to 'Regular' if not specified

### Search for lines or routes matching the query string

*Tags:* `Line`

#### Input Parameters
* `query` - _required_ - Search term e.g victoria
* `modes` - _optional_ - Optionally filter by the specified modes
* `serviceTypes` - _optional_ - A comma seperated list of service types to filter on. Supported values: Regular, Night. Defaulted to 'Regular' if not specified

### Gets the line status for all lines with a given severity<br/>
>             A list of valid severity codes can be obtained from a call to Line/Meta/Severity

*Tags:* `Line`

#### Input Parameters
* `severity` - _required_ - The level of severity (eg: a number from 0 to 14)

### Gets lines that match the specified line ids.

*Tags:* `Line`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of line ids e.g. victoria,circle,N133. Max. approx. 20 ids.

### Get the list of arrival predictions for given line ids based at the given stop

*Tags:* `Line`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of line ids e.g. victoria,circle,N133. Max. approx. 20 ids.
* `stopPointId` - _required_ - Optional. Id of stop to get arrival predictions for (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)
* `direction` - _optional_ - Optional. The direction of travel. Can be inbound or outbound or all. If left blank, and destinationStopId is set, will default to all
    Possible values: inbound, outbound, all.
* `destinationStationId` - _optional_ - Optional. Id of destination stop

### Get disruptions for the given line ids

*Tags:* `Line`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of line ids e.g. victoria,circle,N133. Max. approx. 20 ids.

### Get all valid routes for given line ids, including the name and id of the originating and terminating stops for each route.

*Tags:* `Line`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of line ids e.g. victoria,circle,N133. Max. approx. 20 ids.
* `serviceTypes` - _optional_ - A comma seperated list of service types to filter on. Supported values: Regular, Night. Defaulted to 'Regular' if not specified

### Gets the line status of for given line ids e.g Minor Delays

*Tags:* `Line`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of line ids e.g. victoria,circle,N133. Max. approx. 20 ids.
* `detail` - _optional_ - Include details of the disruptions that are causing the line status including the affected stops and routes

### Gets the line status for given line ids during the provided dates e.g Minor Delays

*Tags:* `Line`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of line ids e.g. victoria,circle,N133. Max. approx. 20 ids.
* `detail` - _optional_ - Include details of the disruptions that are causing the line status including the affected stops and routes
* `startDate` - _required_
* `endDate` - _required_
* `dateRange.startDate` - _optional_
* `dateRange.endDate` - _optional_
* `StartDate` - _required_
* `EndDate` - _required_

### Gets all valid routes for given line id, including the sequence of stops on each route.

*Tags:* `Line`

#### Input Parameters
* `id` - _required_ - A single line id e.g. victoria
* `direction` - _required_ - The direction of travel. Can be inbound or outbound.
    Possible values: inbound, outbound, all.
* `serviceTypes` - _optional_ - A comma seperated list of service types to filter on. Supported values: Regular, Night. Defaulted to 'Regular' if not specified
* `excludeCrowding` - _optional_ - That excludes crowding from line disruptions. Can be true or false.

### Gets a list of the stations that serve the given line id

*Tags:* `Line`

#### Input Parameters
* `id` - _required_ - A single line id e.g. victoria
* `tflOperatedNationalRailStationsOnly` - _optional_ - If the national-rail line is requested, this flag will filter the national rail stations so that only those operated by TfL are returned

### Gets the timetable for a specified station on the give line

*Tags:* `Line`

#### Input Parameters
* `fromStopPointId` - _required_ - The originating station's stop point id (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)
* `id` - _required_ - A single line id e.g. victoria

### Gets the timetable for a specified station on the give line with specified destination

*Tags:* `Line`

#### Input Parameters
* `fromStopPointId` - _required_ - The originating station's stop point id (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)
* `id` - _required_ - A single line id e.g. victoria
* `toStopPointId` - _required_ - The destination stations's Naptan code

### Returns the service type active for a mode.<br/>
>             Currently only supports tube

*Tags:* `Mode`

### Gets the next arrival predictions for all stops of a given mode

*Tags:* `Mode`

#### Input Parameters
* `mode` - _required_ - A mode name e.g. tube, dlr
* `count` - _optional_ - A number of arrivals to return for each stop, -1 to return all available.

### Get the occupancy for bike points.

*Tags:* `Occupancy`

#### Input Parameters
* `ids` - _required_

### Gets the occupancy for all car parks that have occupancy data

*Tags:* `Occupancy`

### Gets the occupancy for a car park with a given id

*Tags:* `Occupancy`

#### Input Parameters
* `id` - _required_

### Gets the occupancy for all charge connectors

*Tags:* `Occupancy`

### Gets the occupancy for a charge connectors with a given id (sourceSystemPlaceId)

*Tags:* `Occupancy`

#### Input Parameters
* `ids` - _required_

### Gets the places that lie within the bounding box defined by the lat/lon of its north-west and south-east corners. Optionally filters<br/>
>             on type and can strip properties for a smaller payload.

*Tags:* `Place`

#### Input Parameters
* `categories` - _optional_ - an optional list of comma separated property categories to return in the Place's property bag. If null or empty, all categories of property are returned. Pass the keyword "none" to return no properties (a valid list of categories can be obtained from the /Place/Meta/categories endpoint)
* `includeChildren` - _optional_ - Defaults to false. If true child places e.g. individual charging stations at a charge point while be included, otherwise just the URLs of any child places will be returned
* `type` - _optional_ - place types to filter on, or null to return all types
* `activeOnly` - _optional_ - An optional parameter to limit the results to active records only (Currently only the 'VariableMessageSign' place type is supported)
* `bbBoxpoints.swLat` - _required_
* `bbBoxpoints.swLon` - _required_
* `bbBoxpoints.neLat` - _required_
* `bbBoxpoints.neLon` - _required_

### Gets the set of streets associated with a post code.

*Tags:* `Place`

#### Input Parameters
* `postcode` - _required_
* `postcodeInput.postcode` - _optional_
* `Postcode` - _required_

### Gets a list of all of the available place property categories and keys.

*Tags:* `Place`

### Gets a list of the available types of Place.

*Tags:* `Place`

### Gets all places that matches the given query

*Tags:* `Place`

#### Input Parameters
* `name` - _required_ - The name of the place, you can use the /Place/Types/{types} endpoint to get a list of places for a given type including their names.
* `types` - _optional_ - A comma-separated list of the types to return. Max. approx 12 types.

### Gets all places of a given type

*Tags:* `Place`

#### Input Parameters
* `types` - _required_ - A comma-separated list of the types to return. Max. approx 12 types.
            A valid list of place types can be obtained from the /Place/Meta/placeTypes endpoint.
* `activeOnly` - _optional_ - An optional parameter to limit the results to active records only (Currently only the 'VariableMessageSign' place type is supported)

### Gets the place with the given id.

*Tags:* `Place`

#### Input Parameters
* `id` - _required_ - The id of the place, you can use the /Place/Types/{types} endpoint to get a list of places for a given type including their ids
* `includeChildren` - _optional_ - Defaults to false. If true child places e.g. individual charging stations at a charge point while be included, otherwise just the URLs of any child places will be returned

### Gets any places of the given type whose geography intersects the given latitude and longitude. In practice this means the Place<br/>
>             must be polygonal e.g. a BoroughBoundary.

*Tags:* `Place`

#### Input Parameters
* `type` - _required_ - The place type (a valid list of place types can be obtained from the /Place/Meta/placeTypes endpoint)
* `lat` - _required_
* `lon` - _required_
* `location.lat` - _required_
* `location.lon` - _required_
* `Lat` - _required_
* `Lon` - _required_

### Gets the place overlay for a given set of co-ordinates and a given width/height.

*Tags:* `Place`

#### Input Parameters
* `z` - _required_ - The zoom level
* `type` - _required_ - The place type (a valid list of place types can be obtained from the /Place/Meta/placeTypes endpoint)
* `width` - _required_ - The width of the requested overlay.
* `height` - _required_ - The height of the requested overlay.
* `lat` - _required_
* `lon` - _required_
* `location.lat` - _required_
* `location.lon` - _required_
* `Lat` - _required_
* `Lon` - _required_

### Gets all roads managed by TfL

*Tags:* `Road`

### Gets a list of valid RoadDisruption categories

*Tags:* `Road`

### Gets a list of valid RoadDisruption severity codes

*Tags:* `Road`

### Gets a list of active disruptions filtered by disruption Ids.

*Tags:* `Road`

#### Input Parameters
* `disruptionIds` - _required_ - Comma-separated list of disruption identifiers to filter by.
* `stripContent` - _optional_ - Optional, defaults to false. When true, removes every property/node except for id, point, severity, severityDescription, startDate, endDate, corridor details, location and comments.

### Gets a list of disrupted streets. If no date filters are provided, current disruptions are returned.

*Tags:* `Road`

#### Input Parameters
* `startDate` - _required_ - Optional, the start time to filter on.
* `endDate` - _required_ - Optional, The end time to filter on.

### Gets the road with the specified id (e.g. A1)

*Tags:* `Road`

#### Input Parameters
* `ids` - _required_ - Comma-separated list of road identifiers e.g. "A406, A2" (a full list of supported road identifiers can be found at the /Road/ endpoint)

### Get active disruptions, filtered by road ids

*Tags:* `Road`

#### Input Parameters
* `ids` - _required_ - Comma-separated list of road identifiers e.g. "A406, A2" use all for all to ignore id filter (a full list of supported road identifiers can be found at the /Road/ endpoint)
* `stripContent` - _optional_ - Optional, defaults to false. When true, removes every property/node except for id, point, severity, severityDescription, startDate, endDate, corridor details, location, comments and streets
* `severities` - _optional_ - an optional list of Severity names to filter on (a valid list of severities can be obtained from the /Road/Meta/severities endpoint)
* `categories` - _optional_ - an optional list of category names to filter on (a valid list of categories can be obtained from the /Road/Meta/categories endpoint)
* `closures` - _optional_ - Optional, defaults to true. When true, always includes disruptions that have road closures, regardless of the severity filter. When false, the severity filter works as normal.

### Gets the specified roads with the status aggregated over the date range specified, or now until the end of today if no dates are passed.

*Tags:* `Road`

#### Input Parameters
* `ids` - _required_ - Comma-separated list of road identifiers e.g. "A406, A2" or use "all" to ignore id filter (a full list of supported road identifiers can be found at the /Road/ endpoint)
* `dateRangeNullable.startDate` - _optional_
* `dateRangeNullable.endDate` - _optional_

### Search the site for occurrences of the query string. The maximum number of results returned is equal to the maximum page size<br/>
>             of 100. To return subsequent pages, use the paginated overload.

*Tags:* `Search`

#### Input Parameters
* `query` - _required_ - The search query

### Searches the bus schedules folder on S3 for a given bus number.

*Tags:* `Search`

#### Input Parameters
* `query` - _required_ - The search query

### Gets the available search categories.

*Tags:* `Search`

### Gets the available searchProvider names.

*Tags:* `Search`

### Gets the available sorting options.

*Tags:* `Search`

### Gets a list of StopPoints within {radius} by the specified criteria

*Tags:* `StopPoint`

#### Input Parameters
* `stopTypes` - _required_ - a list of stopTypes that should be returned (a list of valid stop types can be obtained from the StopPoint/meta/stoptypes endpoint)
* `radius` - _optional_ - the radius of the bounding circle in metres (default : 200)
* `useStopPointHierarchy` - _optional_ - Re-arrange the output into a parent/child hierarchy
* `modes` - _optional_ - the list of modes to search (comma separated mode names e.g. tube,dlr)
* `categories` - _optional_ - an optional list of comma separated property categories to return in the StopPoint's property bag. If null or empty, all categories of property are returned. Pass the keyword "none" to return no properties (a valid list of categories can be obtained from the /StopPoint/Meta/categories endpoint)
* `returnLines` - _optional_ - true to return the lines that each stop point serves as a nested resource
* `location.lat` - _required_
* `location.lon` - _required_

### Gets the list of available StopPoint additional information categories

*Tags:* `StopPoint`

### Gets the list of available StopPoint modes

*Tags:* `StopPoint`

### Gets the list of available StopPoint types

*Tags:* `StopPoint`

### Gets a list of StopPoints filtered by the modes available at that StopPoint.

*Tags:* `StopPoint`

#### Input Parameters
* `modes` - _required_ - A comma-seperated list of modes e.g. tube,dlr
* `page` - _optional_ - The data set page to return. Page 1 equates to the first 1000 stop points, page 2 equates to 1001-2000 etc. Must be entered for bus mode as data set is too large.

### Gets a distinct list of disrupted stop points for the given modes

*Tags:* `StopPoint`

#### Input Parameters
* `modes` - _required_ - A comma-seperated list of modes e.g. tube,dlr
* `includeRouteBlockedStops` - _optional_

### Search StopPoints by their common name, or their 5-digit Countdown Bus Stop Code.

*Tags:* `StopPoint`

#### Input Parameters
* `query` - _required_ - The query string, case-insensitive. Leading and trailing wildcards are applied automatically.
* `modes` - _optional_ - An optional, parameter separated list of the modes to filter by
* `faresOnly` - _optional_ - True to only return stations in that have Fares data available for single fares to another station.
* `maxResults` - _optional_ - An optional result limit, defaulting to and with a maximum of 50. Since children of the stop point heirarchy are returned for matches,
            it is possible that the flattened result set will contain more than 50 items.
* `lines` - _optional_ - An optional, parameter separated list of the lines to filter by
* `includeHubs` - _optional_ - If true, returns results including HUBs.
* `tflOperatedNationalRailStationsOnly` - _optional_ - If the national-rail mode is included, this flag will filter the national rail stations so that only those operated by TfL are returned

### Search StopPoints by their common name, or their 5-digit Countdown Bus Stop Code.

*Tags:* `StopPoint`

#### Input Parameters
* `query` - _required_ - The query string, case-insensitive. Leading and trailing wildcards are applied automatically.
* `modes` - _optional_ - An optional, parameter separated list of the modes to filter by
* `faresOnly` - _optional_ - True to only return stations in that have Fares data available for single fares to another station.
* `maxResults` - _optional_ - An optional result limit, defaulting to and with a maximum of 50. Since children of the stop point heirarchy are returned for matches,
            it is possible that the flattened result set will contain more than 50 items.
* `lines` - _optional_ - An optional, parameter separated list of the lines to filter by
* `includeHubs` - _optional_ - If true, returns results including HUBs.
* `tflOperatedNationalRailStationsOnly` - _optional_ - If the national-rail mode is included, this flag will filter the national rail stations so that only those operated by TfL are returned

### Gets the service types for a given stoppoint

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - The Naptan id of the stop
* `lineIds` - _optional_ - The lines which contain the given Naptan id (all lines relevant to the given stoppoint if empty)
* `modes` - _optional_ - The modes which the lines are relevant to (all if empty)

### Gets a StopPoint for a given sms code.

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - A 5-digit Countdown Bus Stop Code e.g. 73241, 50435, 56334.
* `output` - _optional_ - If set to "web", a 302 redirect to relevant website bus stop page is returned. Valid values are : web. All other values are ignored.

### Gets all stop points of a given type

*Tags:* `StopPoint`

#### Input Parameters
* `types` - _required_ - A comma-separated list of the types to return. Max. approx. 12 types. 
            A list of valid stop types can be obtained from the StopPoint/meta/stoptypes endpoint.

### Gets all the stop points of given type(s) with a page number

*Tags:* `StopPoint`

#### Input Parameters
* `types` - _required_
* `page` - _required_

### Gets a list of StopPoints corresponding to the given list of stop ids.

*Tags:* `StopPoint`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of stop point ids (station naptan code e.g. 940GZZLUASL). Max. approx. 20 ids.
            You can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name.
* `includeCrowdingData` - _optional_ - Include the crowding data (static). To Filter further use: /StopPoint/{ids}/Crowding/{line}

### Gets all disruptions for the specified StopPointId, plus disruptions for any child Naptan records it may have.

*Tags:* `StopPoint`

#### Input Parameters
* `ids` - _required_ - A comma-seperated list of stop point ids. Max. approx. 20 ids.
            You can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name.
* `getFamily` - _optional_ - Specify true to return disruptions for entire family, or false to return disruptions for just this stop point. Defaults to false.
* `includeRouteBlockedStops` - _optional_
* `flattenResponse` - _optional_ - Specify true to associate all disruptions with parent stop point. (Only applicable when getFamily is true).

### Gets the list of arrival predictions for the given stop point id

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - A StopPoint id (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)

### Gets Stopoints that are reachable from a station/line combination.

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - The id (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name) of the stop point to filter by
* `lineId` - _required_ - Line id of the line to filter by (e.g. victoria)
* `serviceTypes` - _optional_ - A comma-separated list of service types to filter on. If not specified. Supported values: Regular, Night. Defaulted to 'Regular' if not specified

### Gets all the Crowding data (static) for the StopPointId, plus crowding data for a given line and optionally a particular direction.

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - The Naptan id of the stop
* `line` - _required_ - A particular line e.g. victoria, circle, northern etc.
* `direction` - _required_ - The direction of travel. Can be inbound or outbound.
    Possible values: inbound, outbound, all.

### Returns the canonical direction, "inbound" or "outbound", for a given pair of stop point Ids in the direction from -&gt; to.

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - Originating stop id (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)
* `toStopPointId` - _required_ - Destination stop id (station naptan code e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)
* `lineId` - _optional_ - Optional line id filter e.g. victoria

### Returns the route sections for all the lines that service the given stop point ids

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - A stop point id (station naptan codes e.g. 940GZZLUASL, you can use /StopPoint/Search/{query} endpoint to find a stop point id from a station name)
* `serviceTypes` - _optional_ - A comma-separated list of service types to filter on. If not specified. Supported values: Regular, Night. Defaulted to 'Regular' if not specified

### Get a list of places corresponding to a given id and place types.

*Tags:* `StopPoint`

#### Input Parameters
* `id` - _required_ - A naptan id for a stop point (station naptan code e.g. 940GZZLUASL).
* `placeTypes` - _required_ - A comcomma-separated value representing the place types.

### Get car parks corresponding to the given stop point id.

*Tags:* `StopPoint`

#### Input Parameters
* `stopPointId` - _required_ - stopPointId is required to get the car parks.

### Gets a list of taxi ranks corresponding to the given stop point id.

*Tags:* `StopPoint`

#### Input Parameters
* `stopPointId` - _required_ - stopPointId is required to get the taxi ranks.

### Gets the TravelTime overlay.

*Tags:* `TravelTime`

#### Input Parameters
* `z` - _required_ - The zoom level.
* `pinLat` - _required_ - The latitude of the pin.
* `pinLon` - _required_ - The longitude of the pin.
* `mapCenterLat` - _required_ - The map center latitude.
* `mapCenterLon` - _required_ - The map center longitude.
* `scenarioTitle` - _required_ - The title of the scenario.
* `timeOfDayId` - _required_ - The id for the time of day (AM/INTER/PM)
* `modeId` - _required_ - The id of the mode.
* `width` - _required_ - The width of the requested overlay.
* `height` - _required_ - The height of the requested overlay.
* `direction` - _required_ - The direction of travel.
    Possible values: Average, From, To.
* `travelTimeInterval` - _required_ - The total minutes between the travel time bands
* `compareType` - _required_
* `compareValue` - _required_

### Gets the TravelTime overlay.

*Tags:* `TravelTime`

#### Input Parameters
* `z` - _required_ - The zoom level.
* `pinLat` - _required_ - The latitude of the pin.
* `pinLon` - _required_ - The longitude of the pin.
* `mapCenterLat` - _required_ - The map center latitude.
* `mapCenterLon` - _required_ - The map center longitude.
* `scenarioTitle` - _required_ - The title of the scenario.
* `timeOfDayId` - _required_ - The id for the time of day (AM/INTER/PM)
* `modeId` - _required_ - The id of the mode.
* `width` - _required_ - The width of the requested overlay.
* `height` - _required_ - The height of the requested overlay.
* `direction` - _required_ - The direction of travel.
    Possible values: Average, From, To.
* `travelTimeInterval` - _required_ - The total minutes between the travel time bands

### Gets the Emissions Surcharge compliance for the Vehicle

*Tags:* `Vehicle`

#### Input Parameters
* `vrm` - _required_ - The Vehicle Registration Mark

### Gets the Ulez Surcharge compliance for the Vehicle

*Tags:* `Vehicle`

#### Input Parameters
* `vrm` - _required_ - The Vehicle Registration Mark

### Gets the predictions for a given list of vehicle Id's.

*Tags:* `Vehicle`

#### Input Parameters
* `ids` - _required_ - A comma-separated list of vehicle ids e.g. LX58CFV,LX11AZB,LX58CFE. Max approx. 25 ids.

## License

**flow**ground :- Telekom iPaaS / tfl-gov-uk-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
