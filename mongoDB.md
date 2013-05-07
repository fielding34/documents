# MonogDB

## CRUD
```javascript
	db.bios.insert({
		_id:1, name:{first:'John', last: 'Backus'}, 
		birth: new Date('1984-01-01'), 
		awards: [
			{award: 'x', year: 1962, by: 'ACM'}, 
			{award: 'y', year: 1978, by: 'ACM1'}
        	]
   	});
   	
   	> db.bios.find({}, {_id:0, name: 1});
	{ "name" : { "first" : "John", "last" : "Backus" } }

	> db.bios.find({'name.first': 'John'}, {_id:0, name: 1});
	{ "name" : { "first" : "John", "last" : "Backus" } }

	> db.bios.find({'awards.award': 'x'}, {_id:0, name: 1});
	{ "name" : { "first" : "John", "last" : "Backus" } }
	
	# insert without _id
	> db.bios.insert({name:{first:'Tom', last: 'Backus'}, birth: new Date('1984-02-02'), awards: [{award: 'xx', year: 1962, by: 'ACM'}, {award: 'yy', year: 1978, by: 'ACM1'}]});
	> db.bios.find({_id: ObjectId("5188babdb6e6b4f579286c54")});
	{ "_id" : ObjectId("5188babdb6e6b4f579286c54"), "name" : { "first" : "Tom", "last" : "Backus" }, "birth" : ISODate("1984-02-02T00:00:00Z"), "awards" : [        {       "award" : "xx",  "year" : 1962,  "by" : "ACM" },         {       "award" : "yy",         "year" : 1978,  "by" : "ACM1" } ] }

````



