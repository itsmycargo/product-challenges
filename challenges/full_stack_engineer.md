# Full Stack Developer Position - Home Task

## Background Information

One integral part of our system is the ability to deal with Hubs. A hub can be an Ocean Port, an Airport, a Railyard, or even a Truck-Terminal. When you combine two hubs, we call that a Route. We then attach Pricings to these routes, but also to single hubs (local charges at ports for example). Usually, these pricings are handled in large Excel sheets.

In order to uniquely identify a hub, when we attach a pricing to it, we use the so called “UN/LOCODE”. The UN constantly updates the LOCODES. A complete version of the list can be downloaded here: https://www.unece.org/cefact/codesfortrade/codes_index.html.

## Task
Write a program that

- Downloads the CSV data (comes as zip file in 3 parts)
- Loads the data into a well designed DB
- Lets a user search through the DB in a web application as well as filtering / sorting it. If there are no results, display a nice message. There is explicitly no CSS styling needed!
- Lets a user enter any address and find the nearest hub to that (the coordinates are included in the data, but may need to be converted into a standard lat/lon format)
- Bonus: Button next to search entries that lets you display the hub on a map

## How to deliver your code/app:

- We're strict on tests, testability, clean and readable code
- We care about whether or not the app meets the given requirements
- Think about performance, edge-cases and error handling, SOLID principles
- Think about usability and the experience of using the app (excluding CSS styling)

Once you're finished, deploy your solution. Email us back a link to the deployed application and attach your code as a git bundle ([documentation](https://git-scm.com/docs/git-bundle)).

**Please don't push to a public repo e.g. on Github!!**

### Estimated duration

We're looking for an app and code that you're proud of.
It shouldn't take more than a few hours, but there's no set time limit. Within a week is fine. Ultimately we're going to make a judgement about your skill level and approach on this basis, so if you're not happy with it, don't send it! But at the same time, don’t over-engineer it.

Other than that: **Have fun! ;-)**
