Week 5 Notes - Rails and Sinatra

  Sinatra

    URL.com/users/:user

    ^ passing params in URL


  MVC

    -Dispatcher
      -located outside of Rails
      -can serve assets such as: images
                                 JavaScript/CoffeeScript files
                                 stylesheets
      -client doesn't have to load Rails to access these assets
      -Rails takes ~500ms to load SCSS, Coffeescript, etc.


  RESTful

    -use HTTP (only GET/POST)
    -use URL to clearly pass information ie. params
    -send CRUD using these restraints


  Rails Views

    -Rails has templates, not real views
    -traditional views have much more power than what Rails offers
    -in production, a professional app will pass the Rails views through a
     decorator/presenter
    -Rails is better thought of as Mr. T
      -model/router/template
    -assets never get to have acces to actual data
    -never use ERB in SCSS!
      -it prevents the precompiling of assets if any logic has to be processed
       by the stylesheet


  Presenters/Decorators

    -often an individual one is used per model
    -can turn data into JSON
    -make views more secure

    Presenters
      -allow us to see only data we need

    Decorators
      -style data for us
      -some examples:
        -add parens and dashes to phone numbers
        -cut floating point number down to two decimals to represent money


  Rails Models and Databases

    -some Rails models may not interact with the database at all. They may, for
     example, handle API calls or process data held in the lib folder
    -databases are super fast, so we want to rely on them when accessing data,
     which is their specialty
    -models are all about data persistence


  Rails Testing

    -controller specs are often redundant
    -views get tested through integration tests
    -views often contain a lot of bugs, but the tests for them are extremely
     unreliable. Integration tests are better because they use actual controller
     data
    -controllers and views should be so stupid that nothing breaks, but the
     interaction between the two will break often
