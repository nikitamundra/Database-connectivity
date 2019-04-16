var mongoclient = require('mongodb').MongoClient;
var url = "mongodb://localhost:27017/";
mongoclient.connect(url,function(err,db){
    if(err) throw err;
    var dbo = db.db("mynewdb");
  
  //Insertion
    var myobj = [{name: "sachi" ,lastname: "shah",age: "25",eid:"1"},{name: "prachi" ,lastname: "shah", age: "45",eid:"2"},{name: "ranchi" ,lastname: "shah", age: "22",eid:"3"}] ;
    dbo.collection("newaggrecollection").insertMany(myobj , function(err , res){
   
   // Find
     dbo.collection("collection_name").find({'age': {$gt : "43"}}).toArray(function(err , res){
     
   if(err) throw err;
        console.log(res);
        db.close();
    });
})
