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
 
