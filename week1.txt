Week 1 Notes - Ruby

  Order of Operations

  -"&&" and "||" have higher precedence than "and" and "or"
    -"and" and "or" evaluate after "="

  -"not" is evaluated right before "and" and "or"


  Classes

    -Factory that makes objects
      -better description than "blueprint"

    -Self refers to the current class or method (the scope)
      -When outside of either (ie. irb), it refers to the program being run (which is the current scope)

    -A rule of thumb for when to use class methods vs. instance methods
      -Take a database for example
        -Spawning multiple databases would generally be unwanted, so it works
         best as class method.

    -A smell test for methods is only declaring and calling it. That type of
     method is probably not suited to instances.
    -Use instances for storing persistent data.

    b = Beer.new
    b.song

    ^ Good example of when spawning instances is overkill.

  Return

    -Exits the entire method when called inside a loop.
    -It exits the current scope.


  Integers

    -.downto instance method


  Functional languages use immutable variables.


  Recursion

    -Analogy:
      -If you are home, stop moving.
      -Else take one small step toward home.
      -Once home, speak the path.

    -Tail recursion
      -can replace loops
      -head is isolated (0 index) from tail (rest of array)
      -head is then compared to the new head (new 0 index)

      given a = [1, 2, 3, 4]

      method 1) head, *tail = a

      method 2) head: a[0]
                tail: a[1, -1]  # returns an array of everything but the [0] element


    -Break the problem down to simplest possible form and aggregate results

    -Fibonacci recursion
      n = (n - 1) + (n - 2)
        -where n[0] =  1 and n[1] = 1
      def fib(n)
        if n == 1 || n == 2
          return 1
        else
          return fib(n - 1) + fib (n - 2)
        end
      end

    -Real world examples of recursion:
      -Showing which navbar item is active
      -When a user has other users that belong to them


  Algorithm Design

    1) Requirements
    2) Build toolbox
    3) Whiteboard (physically draw logic on whiteboard/paper)
    4) Test/spec
    5) Write code (ideally the shortest step)
    6) Refactor


  Modulo

    -Picture a circle or wheel with the numbers 1 through the modulo number.
    -Those numbers are the only numbers in the universe to that modulo
    -It then returns the extra steps around the circle that do not make a
      complete revolution (360 degrees).


  each vs. map

    each
      -Does something with every element and does nothing with the returned
       object in particular.
    map
      -Also does something with every element but instead returns an array with
       the new elements inside.

    Aliases

      -map = collect
      -reduce = inject


  Sublime Snippets

    -Tab Shortcuts
      -$1, $2, $3, etc
      -Pressing tab will sequentially jump between the points marked with a
       shortcut.
      -$(1:sometext) = text inside parentheses will autohighlight when tabbed to
       for easy text insertion into elements.

    -Shortcuts
      -Apple D = multicursor
      -Apple G = multiselection?


  Arity
    -The number of arguments accepted by a function (different from number given
     to function).

