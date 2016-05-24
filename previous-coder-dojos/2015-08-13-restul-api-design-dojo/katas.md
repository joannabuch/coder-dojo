## Lighting API

Because we are too lazy to get up from the couch to turn on the light we have a house automation system that allows us to control all our lighting appliances via our smartphones. Since we are geek it also has advanced features like energy saving rules etc. To run it from our RaspberryPI we design a RESTful API for. The requirements are numbered by priority:

- Be able to turn on and off regular light bulbs
- There are also multi-color light bulbs. We want to be able to set their color
- There are also luminosity light bulbs. We want to be able to set their luminosity
- Luminosity light bulbs should be able to have gradients (turning on very slow, very fast, …)
- There are movement detector light bulbs, we want to be able to set their sensitivity and duration
- We want to be able to set energy-saving settings for single lamps, e.g. turning off after 10 minutes or turning off at 10 p.m.
We want to be able to set energy-saving settings globally

## Router

We have a Microservice Architecture with lots of services. And as we have so many services, we need to have one entrypoint to our website for our clients. We name this one entrypoint The Router. The Router is responsible for getting a request from customer website and route, transform it, and passing it further to the microservices. The microservices will give a response back to the router and the router will forward the response back to the customer.
Design an API that will manage the routes of The Router.

We have the following requirements:
A route is composed of three parts:

- a matching part
- a filter part
- an endpoint part

The matching part can match full urls, or regexes
The filter part can add headers to the initial request, can remove headers, can override the path
The endpoint can be an http or https endpoint
After a route has been created, it won’t directly go live, there will be an approval process.
Some users will have the right to create routes, some will have the right to approve them

## Fantasy Football

We want to launch a Zalando-wide Fantasy Football League to better integrate with colleagues from different sites. In our Fantasy Football League App the following things are possible:

- choose names and slogans for your team
- draft players to your teams
- there is a global list of players (but not two players can be drafted to two teams)
- teams have matches against each other and score respectively
- you can see which players shot which goal in which minute in the game
- there is a league table that reflects the current ranking of all teams regarding their scoring
- teams can buy and sell players from other teams
