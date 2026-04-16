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
