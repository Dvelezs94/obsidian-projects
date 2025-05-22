As we continue building Uptinio, we thought it’d be worth sharing some of the challenges we have faced along the way. Some were quick wins. Others pushed us to our limits as developers and system designers.

Here’s a look behind the curtain.
### Low cost resilient system architecture
Building resilient systems is nothing new for us - as cloud natives we have resiliency and self-healing baked in our DNA. 

What we want is an architecture with **99.999%** availability

In order to achieve this we need to build a good self-healable distributed system, this means a system that not just operates in different physical locations, but that also monitors and heals itself in case of a disaster, all within a budget of under $100/mo. As you can see it's not as straightforward as building a simple website.

What we did:
1. Hosting
2. Database
3. Workers
4. Load balancers

### 0 downtime on deployments
We get this feature thanks to AWS load balancers and ECS, thanks to them we can perform rolling deployments without worrying the application going down

Shutdown signals are sent before the container dies, so all jobs should finish gracefully - and for the ones who don't, well those they just get retried by another worker.

### Distributed load across components
The heaviest load in our system comes from the network checks and reporting tools - here is where workers come into play

The database does some of the work too by using timescaledb we can perform database operations in time buckets, which drastically improves the load and computation of your performance data.

As you can see all our components, help the load distribute across them, however this is a double edge weapon

### Low network usage
The main concern here is that we dont want the hosting to block our requests

### Pluggable system
When I hear plugins in monitoring tools, I think about nagios. Nagios have hands down the best plugin system, you can create your own custom checks and alerts with these plugins, and I want the same idea implemented in uptinio.

### Avoid false positives
Having lousy alerting tools is worse for the business than having no alerting at all - and this is why we have by design double checking before opening any incident.

## The future
And of course we have many plans and features going on, here are some of them...

- AI capabilities
- MCP and connectivity with chatbots
- Data export
- Improved data visualization
- Develop and use your own custom checks (just like nagios)
