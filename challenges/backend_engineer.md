# Backend Engineer Position - Home Task

## Background Information

One integral part of our system is the ability to deal with Hubs. A hub can be
an Ocean Port, an Airport, a Railyard, or even a Truck-Terminal. When you
combine two hubs, we call that a Route. We then attach Pricings to these routes,
but also to single hubs (local charges at ports for example). Usually, these
pricings are handled in large Excel sheets.

In order to uniquely identify a hub, when we attach a pricing to it, we use the
so called “UN/LOCODE”. The UN constantly updates the LOCODES. A complete version
of the list can be downloaded here:
https://www.unece.org/cefact/codesfortrade/codes_index.html.

Your task is constructed of two parts: 1) Development of backend application
and 2) Deployment Task

## Development Task

Write a program that

- Downloads the CSV data (comes as zip file in 3 parts)
- Loads the data into a well designed DB
- Simple API endpoint to query data by:
	- country and/or city
	- search nearest LOCODEs by address

## Deployment Task

Write necessary bits to be able to

* Package your solution as Docker container
* Deploy it to Kubernetes Cluster

For the Kubernetes cluster, you can use anything that you already have access
to, or easily launch a test cluster. For example, on macOS you can install
Docker for Mac and then enable a local Kubernetes cluster from the settings.

What we want to see from you, is that you are able to explain how you deployed
the services and, if you had any challenges, how you found answers for the
problems, as well as service descriptions you used to deploy the services to
Kubernetes.

## How to deliver your code/app:

- We're strict on tests, testability, clean and readable code
- We care about whether or not the app meets the given requirements
- Think about performance, edge-cases and error handling, SOLID principles

Once you are finished, package your application and necessary Kubernetes
manifests within same GIT repository and email us your solution and attach your
code as GIT bundle ([documentation](https://git-scm.com/docs/git-bundle)).

**Please don't push to a public repo e.g. on Github!!**

### Estimated duration

We're looking for an app and code that you're proud of.
It shouldn't take more than a few hours, but there's no set time limit. Within a
week is fine. Ultimately we're going to make a judgement about your skill level
and approach on this basis, so if you're not happy with it, don't send it! But
at the same time, don’t over-engineer it.

If there is anhy question, or you feel you are getting stuck - feel free to
email us.

Other than that: **Have fun! ;-)**
