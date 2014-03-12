var express = require('express'),
	 wines = requre('./routes/wines'),
	 app = express();

	//MongoClient = require('mongodb').MongoClient,
	//Server = require('mongodb').Server;

//var http = require('http');
/*
http.createServer(function (req, res) {
	res.writeHead(200, {'Content-Type': 'text/plain'});
	res.end('Hello World\n');
}).listen(3000, '127.0.0.1');
*/


// using express
// for index page
app.get('/', function(req, res) {
	res.send('Hello World!');	
});

// using routes
app.get('/wines', wines.findAll);
app.get('/wines/:id', wines.findById);

//	for pages that do not exists
app.get('*', function(req, res){
    res.send('Page Not Found', 404);
});

/*	before setting up routes
// wines catalog page
app.get('/wines', function(req, res) {
	res.send([{name:'wine1'}, {name:'wine2'}]);
});
// individual wine page
app.get('/wines/:id', function(req, res) {
	res.send({id:req.params.id, name: "The Name", description: "description"});
});
*/


app.listen(3000);

console.log('Server running on port 3000');
