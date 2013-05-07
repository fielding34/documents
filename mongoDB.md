** MonogDB **
	<code>
		  db.bios.insert({
				_id:1, name:{first:'John', last: 'Backus'}, 
				birth: new Date('1984-01-01'), 
				awards: [
					{award: 'x', year: 1962, by: 'ACM'}, 
					{award: 'y', year: 1978, by: 'ACM1'}
        			]
   		});
	</code>
