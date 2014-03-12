var express = require('express'),
	 wine = require('./routes/wines'),
	 app = express();


app.configure(function() {
	app.use(express.logger('dev'));
	app.use(express.bodyParser());
});


//// using express ////
// for index page
app.get('/', function(req, res) {
	res.send('Hello World!');	
});
//	for pages that do not exist
app.get('*', function(req, res){
    res.send('Page Not Found', 404);
});

// using routes
app.get('/wines', wine.findAll);
app.get('/wines/:id', wine.findById);
app.post('/wines', wine.addWine);
app.put('/wines/id', wine.updateWine);
app.delete('/wines/:id', wine.deleteWine);

// start server
app.listen(9000);
console.log('Server running on port 9000');
