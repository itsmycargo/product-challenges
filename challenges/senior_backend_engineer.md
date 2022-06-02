# LIVE CODING CHALLENGE

## Rate Distribution

Here at ItsMyCargo we deal with rates all the time. We parse them, adjust them, insert them and of course calculate quotes with them. One of the major challenges we face is keeping all this data in check, while still allowing for one Organization to share its rates with another. This is often further complicated by the region based nature of freight, meaning that only certain tradelanes should be viewable by certain downstream Organizations

## The Task

Spin up a new rails app (using Postgres and Rspec) and generate the two models mentioned below. Migrations and factories are provided to get you going.
Beyond what is stipulated you are free to achieve the goals however you want, using whatever gems or design patterns you find useful.
Understanding time constraints pseudo code is acceptable if properly explained. The purpose of the task is not to inspect the finished product, but rather see how you approach a problem.
Questions are encouraged :)

Using some extremely simplified models for Organizations and Rates come up with a way to share Organization A's Rates with Organizations B & C. Bonus points for flexibility and features!


## Requirements
Given the following list of constraints create  FeeFinder class that when provided with an organization and a trade lane will return the Rate for that Organization and tradelane. If the Organization does not have a Rate on the tradelane, it will take the Rate from Organization A (if it has access to it), otherwise raise a not found error.

## Constraints
- All of Organization A's Rates can be seen by Organization B
- All rates going from 'DEHAM' to 'CNSGH' of Organization A can be seen by Organization C
- All rates EXCEPT those going from 'DEHAM' to 'CNSGH' of Organization A can be seen by Organization D
- Whenever a new Rate is added to Organization A, Organizations B, C & D are able to access based on their existing limitations
- Whenever a Rate is deleted from A, it is not accessible by B, C or D


## Model Definitions

- Organization:
  The Organization represents a customer of ItsMyCargo. These customers can upload their own rates to the system and manage the Rates themselves. However, in the real world some of these business have direct relationships with others and source their Rates from them already. So we must be able to provide access to the rates of the other Organizations.

```ruby
# Migration
create_table :organizations, id: :uuid do |t|
  t.string :slug, index: {unique: true}

  t.timestamps
end

# FactoryBot
factory :organization do
  sequence(:slug) { |n| "test_#{n}" }
end
```

- Rate:
  The Rate we will be using here will be simplified to this: A Rate is defined as the fee to be charged to move the desired cargo from location A to location B on a particular service.

```ruby
# Migration
create_table :rates, id: :uuid do |t|
  t.references :organization, foreign_key: {to_table: :organizations}, type: :uuid, index: true
  t.string :origin
  t.string :destination
  t.string :service
  t.decimal :fee
  t.timestamps
end

# FactoryBot
factory :rate do
  fee { 100 }
  origin { "DEHAM" }
  destination { "CNSGH" }
  service { "standard" }
end
```


- Location:
For this example we will just use UN/LOCODES to represent locations. Here are some tradelanes as seed data. A tradelane is a pairing of origin and destination

```ruby
tradelanes = [
  %w[DEHAM CNSGH],
  %w[CNSGH DEHAM],
  %w[CNSGH BEANR],
  %w[CNSGH NLRTM],
  %w[CNNGB NLRTM],
  %w[NLRTM CNSGH],
  %w[NLRTM THPKK]
]
```