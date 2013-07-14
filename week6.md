Week 6 Notes - Rails Cont.

  Routes

    -the routes file is read and processed from top to bottom
    -topmost route will catch many case, so care has to be taken with ordering

    -resources:
      -7 total
      -CRUD 4
      -index
      -edit
      -new


  Databases

    -types:

      -relational
        -similar to an excel spreadsheet
        -contains tables of attributes
        -a majority of databases are relational

      -object
        -stores actual objects
        -used when performance is critical
        -mongoDB is one example of an object database

      -graph
        -contains a listing of relationships
        -shows how nodes of the same type are connected
        -this is differentiated from relational databases, which track
         relationships between different nodes

      -key/value
        -looks like JSON
        -used primarily for caching


  Controllers

    -methods
      -will render an HTML file with the same name as it unless it
       explicitly returned or yielded

    -instance variables
      -act weird and different in Rails (vs Ruby)
      -Rails uses its magic to make instance variables available in the view
       files
      -besides their availability in Rails views, they act identical to Ruby
       instance varialbes