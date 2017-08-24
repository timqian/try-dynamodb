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


##

You can use the query method to retrieve data from a table. You must specify a partition key value; the sort key is optional.