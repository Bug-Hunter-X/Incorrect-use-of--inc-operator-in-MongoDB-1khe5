# Incorrect use of $inc operator in MongoDB
This example demonstrates an incorrect use of the $inc operator in MongoDB. The $inc operator is used to increment or decrement a numeric field in a document.  However, the following code snippet provides an incorrect usage:

```javascript
db.collection.updateOne({"_id": 1}, {"$inc": {"field": "1"}});
```

The error occurs because the increment value ("1") is a string, not a number. This will result in an error in MongoDB.

## Solution
To correct the error, use a number as the increment value:
```javascript
db.collection.updateOne({"_id": 1}, {"$inc": {"field": 1}});
```