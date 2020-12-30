# ORMAE_PLAN

1. First we  need to create docker images for all the services which are involved in application's microservices
2. We can use kubernetes over here to deploy each service in a single node or multiple nodes.
3. Since our requirement is for 100k users, we need to use it different nodes.
4. For the deployment in multiple nodes, we can use any configuration management tools like ansible or chef here.
5. We can use kubernetes services like "loadbalancer" and "ClusterIP" here to connect all these services.
6. since we want to run these each micro service on a different nodes, we can easyly deploy the new tests on each micro service.
7. Create individual branch in GitHub for each microservice, and create individual job for each microservice in Jenkins.
8. So that we can easily deploy the builds on to each microservice by monitoring each branch in the GitHub.
9. As we have multiple nodes here, we can invoke any configuration tool here to deploy that perticular build from Jenkins server.
10. As you mentioned , Staging setup needs to be less in terms of operating cost, We can use all these microservices on a single node and 	can operate from here.
11. If it is everything goes well, we can deploy to Prod environment.
12. We can use kubernetes logs here to monitor each service.
13. We can build dashboards in elastic stack by using these logs.
14. For the monitoring components and alerts we can use Nagios.
15. However we are using kubernetes, we don't need to bother about containers.We only need to bother about nodes.So we need to install          Nagios on each node to get alerts if there is anything wrong.
16. We can use autoscaling option on nodes here to optomize our cost.
