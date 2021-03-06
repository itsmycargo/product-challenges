# DevOps Challenge

We like to thank you for taking part in our technical challenge. What we would like to see from you with this challenge
is your way to think and solve problems and research solutions. We care more about how you get to a solution than the actual
solution itself. If you encounter any difficulties or get stuck, don’t worry. Just send us back what you have managed to
complete.

## Challenge

The task is simple, create an application deployment that contains two components that are linked together.

* Web backend: Use docker image `dockercloud/hello-world`
* Web frontend: Use nginx (or any other simple web server that can reverse proxy to backend)

**Please note**: Ingress controller is considered to be part of Kubernetes deployment and not application deployment.
Deploying nginx-ingress doesn't remove need for deploying Nginx (or other web server) as part of application.

For the Kubernetes cluster, you can use anything that you already have access to, or easily launch a test cluster.
For example, on macOS you can install Docker for Mac and then enable a local Kubernetes cluster from the settings.

What we want to see from you, is that you are able to explain how you deployed the services and, if you had any challenges,
how you found answers for the problems, as well as service descriptions you used to deploy the services to Kubernetes.

Best of luck, and if you have any questions, don’t hesitate to contact us!
