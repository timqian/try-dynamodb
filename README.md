## [Concepts](http://docs.aws.amazon.com/amazondynamodb/latest/gettingstartedguide/quick-intro.html)
- Tables: a table is a collection of data (`People`)
- Items: an item is a row/record/tuple stored in a table (`one person`)
- Attributes: an attribute is a fundamental data element(sth does not need to be broken down any further). An item is composed of one or more attributes(`person's name; gender`)
- Primary Key: uniquely identifies each item in the table. No two items can have the same key. You **must** specify the primary key to update, delete an item.
    * partition key (`hash attribute` of an item)
    * sort key (`range attribute` of an item)
- Secondary Indexes: read data using non-key attributes

## Refs

- [How dynamodb works](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.html)
- [nodejs and dynamodb](http://docs.aws.amazon.com/amazondynamodb/latest/gettingstartedguide/GettingStarted.NodeJs.html)
- [best practice for dynamodb](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/BestPractices.html)
- [example combained with graphql](https://github.com/serverless/serverless-graphql-blog/blob/master/blog/lib/dynamo.js)
- [dynamo db design example: forum](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SampleData.CreateTables.html)
- [a good cheatsheet](http://www.markomedia.com.au/dynamodb-for-javascript-cheatsheet/)

##

You can use the query method to retrieve data from a table. You must specify a partition key value; the sort key is optional.

Queries allow you to retrieve only a subset of items from a table.


### [differences between put and update](https://stackoverflow.com/questions/43667229/difference-between-dynamodb-putitem-vs-updateitem)

PutItem will Replace an entire item while UpdateItem will Update it.

using `put` you need to provide the whole item, with update, provide the key you would like to change

## differences between get and query

- `get`: You can only get an item by its primary key.
- `query`: 


## using secondary index
having one or more secondary (or alternate) keys available, to allow efficient access to data with attributes other than the primary key.

## de-normalize table when you need two primary keys for a table
https://stackoverflow.com/questions/12920884/is-there-a-way-to-enforce-unique-constraint-on-a-property-field-other-than-the

## How to do feature like star stargizars