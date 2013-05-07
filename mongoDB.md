# MonogDB

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
	
	

````



