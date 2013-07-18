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
       instance variables

    def set_scrabble
      @scrabble = scrabble.find(params[:id])
    end

    -set_scrabbled can then be called to access @scrabble in other methods
    -this method is the same as using a before filter/before action, which
     calls the method passed as an argument
    -a good rule of thumb is that if an instance variable is instantiated more
     than two times in a controller, set_method should be used

    -redirect_to @scrabble can be used instead of the standard Rails
     controller/method argument

    -form_for can intelligently know what form to render
    -if @scrabble has an id, it knows to render an edit form
    -if @scrabble does not have an id, it will render a form to create a new
     entry

    -respond_with
      -added as a single line at the top of a controller
      -responds to JSON, HTML, XML, whatever
      -seldom used, but offers powerful functionality


  Strong Params

    -params are no longer a hash
    -in Rails 4 they are an instance of ActionController::Params
    -only way to turn these new params into a hash is with the .permit() method
    -similarly, views no longer render standard strings and instead render safe
     strings, which are more secure