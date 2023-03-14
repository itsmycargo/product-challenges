# Frontend Engineer

One integral part of our system is to be able to show important business metrics and  overall status to client with one view. As the client signs in, they should be able to quickly see what has happened since last time, how many new shipments have been made etc..

## Task

Write a program that

  - Connects to our API server (OAuth authentication with simple username/password)
  - Fetches a list of shipments and builds a dashboard. The dashboard should show at least the following metrics:
    - Show the last 3-5 shipments made
    - Show, at a glance, how many shipments have been made since yesterday, in the last 7 days and in the last month

### API Endpoint
We provide a simple mock API server for you to use. The API endpoint is at https://imc-fe-challenge.herokuapp.com and
the API documentation can be found at https://imc-fe-challenge.herokuapp.com/docs.

To authenticate, the system has two different users:

  - `jane@itsmycargo.test` with password `hellocargo`
  - `john@itsmycargo.test` with password `hellocargo`

### How to deliver your code/app

- Please demonstrate that you have an understanding of how to use more complex concepts like flux-architecture, observables etc. that are in general advantageous to making a complex and big application scale better
- We're strict on tests, testability, clean and readable code
- We care about whether or not the app meets the given requirements
- Think about performance, edge-cases and error handling, SOLID principles
- Think about usability and the experience of using the app
- We understand that making things pretty with styling is a lot of work, we do expect solution to look usable and have some thoughts on how it looks.

Once you're finished, email us your solution.

**Please attach your solution as a [git bundle](https://git-scm.com/docs/git-bundle)!**

**Please don't push to a public repo e.g. on Github!!**

### Estimated duration

We're looking for an app and code that you're proud of. It shouldn't take more than a few hours, but there's no set time limit. Within a week is fine. Ultimately we're going to make a judgement about your skill level and approach on this basis, so if you're not happy with it, don't send it! But at the same time, don’t over-engineer it.

Other than that: **Have fun! ;-)**
