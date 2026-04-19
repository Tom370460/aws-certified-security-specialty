# Route 53 routing policies
## Simple Routing
## Weighted Routing
Define a % of request to go to a specific resource
* Relative weight so doesnt need to add up to 100 (0 means no traffic)
* If all records have weight of 0, they will all recieve equal load
* Records must be of the same types
* Can be used with Health Checks
* Use cases: Load balancing between regions, testing applications
## Latency Based
Route to the resource with the lowest latency, based on traffic and regions 
* Can also be used with Health Checks with a failover capability
## Failover
Route to the specified main record, with option for failover record
* Use main record if health check is healthy
* Failover to secondary record if main fails
## Geolocation
Specify the location based one country, state, city, etc
* Different from lateny based
* Use cases: Website localisation, restrict content distribution, load balancing
* Default location in case there are no match
* Example: Locations set to US, Asia and Default. Connections from USA will go to US, any country in Asia to Asia,
  and all other locations not specified to the default. Regardless of latency
## Geolproximity
Focuses on physical distance between resources and users
* A positive bias can be set to increase the coverage area of the resource (1 to 99)
* A negative bias can be set to decrease the coverage area of the resource (-1 to -99)
* Easier shifting traffic to another region
## IP based 
Routing based on the IP of the users
* Define locations with CIDR blocks
* Users with matching IP will be routed to that location
