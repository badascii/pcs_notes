Week 3 Notes - JavaScript

  Functions

    -it is very easy to pass functions around as variables

      var ted = function() {}

        is better than

      function ted () {}


  Falsey Values

    false
    null
    0
    ""
    []
    {}
    NaN
    undefined


  Local vs. Global Variables

    bacon = 3  <- global variable
                  climbs up through scopes searching for bacon

    var bacon = 3  <- local variable
                      var means not having to worry about overwriting variables


  Anonymous Functions

    -used to limit scope
    -used for one-off functions that are not reused
    -get pushed to the bottom of the stack


  Bind Events

    -ties an event (mouseclick, touch gesture, keypress) to an action
    -$('a').on('click', ted(e)) <- when calling a named function, do not pass
                                   an argument to the function or it will
                                   immediately execute and return null

     .on() is the main use for anonymous functions due to the fact that they are
     delayed to run at the bottom of the stack


