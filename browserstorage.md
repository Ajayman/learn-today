# Browser Storage
  browser can store key/value much more intuitive(true even without consious reasoning) way than cookies

  ### Session Storage
    stores data only for a session, means until the browser is closed.
    data is never transfered to server
    storage limit is larger than cookie more than 5 mb.
    
  ### Local Storage
      same thing like session storage but remains even the browser is closed 
      no expiration date and get cleared through JS or clearing browser cache/locally stored data
      maxium storage amoung three

  ### Index DB(offline browser storage)
      => low level API for storing significant amount of structured data
     => IndexedDB is a transactional database system, like an SQL-based RDBMS.
     => if you would prefer simple API then use libraries like  localForage, dexie.js, ZangoDB, PouchDB, idb, idb-keyval, JsStore and lovefield that make IndexedDB more programmer-friendly.
     => However, unlike SQL-based RDBMSes, which use fixed-column tables, IndexedDB is a JavaScript-based object-oriented database
     => IndexedDB lets you store and retrieve objects that are indexed with a key; any objects supported by the structured clone                               algorithm can be stored.
     => Operations performed using IndexedDB are done asynchronously, so as not to block applications
     => Support verisoning
     
     Stages
     =>idb.open(name, version, {upgradeCallBack})
     
     indexedDb provides an object store in browser
-> non-relational db
-> store: js objects,files, blobs, etc
-> add data to object store
-> there might be multiple object store
-> unique key or indexes to
for accessing object store 

-> idb.open(name, version, {upgradeCallback})
->  upgrade Callback function to manage the object store.
operations like -> add, get, pul, delete getAll cursor
transactions -> a wrapper around a series of operations
working with data
->	get database object from idb.open
-> open transaction on db
-> open object store on transaction
-> optionlly open index on object store
-> perform operation on object store or index

add data
dbPromise.then(function(db){
	var transaction = db.transation('ppl', 'readwrite');
var store = transaction.objectStore('ppl');
store.add({name: 'fred'});
return transaction.complete;
})

read data
	dbPromise.then(function(db){
	var tx = db.transaction('ppl', 'readonly');
var store = tx.objectStore('ppl');
return store.get('Fred');
})

update Data
 dbPromise.then(function(db){
	var tx = db.transaction('store', 'readwrite');
var store = tx.objectStore('store');
var item  = {name: 'Fred', email: 'fred@example.com'}
store.put(item);
return tx.complete;
})

dbPromise.then(function(db){
	var tx = db.transaction('ppl', 'readwrite');
 	var store = tx.objectStore('ppl');
	store.delete('Fred');
	return tx.complete;
})
 
reference to -> https://www.youtube.com/watch?v=vCumk1sXHcY
