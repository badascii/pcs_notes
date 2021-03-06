Week 2 Notes - Ruby Testing

  Consistent Naming

    -There are only two hard things in Computer Science: cache invalidation and
     naming things. -Phil Karlton


  Debuggers

    debugger:
    1) require 'debugger'
    2) add the word debugger to a problem area of the code
    3) the logic will freeze at that point
    4) the code can then be stepped through in rdb
    5) commands: step, next, continue

    vlad:
    -debugs a frozen program

    pry:
    -fully functional irb
    -cannot be stepped through

  -puts vs. p
  puts generally applies to_s
  p prints the result of inspecting the object


  Testing

    KPI: Key Performance Indicators
      -most important sections of code where tests should be focused
      -critical parts should be tested no matter what


  What to Test

    -every significant input and output
    -any complicated bits
    -things coworkers can break
    -things coworkers won't test manually
    -anything unreliable (ie. APIs and anything network based)


  How to Test

    -exercise the code until you have a basic understanding
    -comment above each function
    -use an ignore file to bypass unneeded tests
    -use a rating system:
      1) add 1 to methods that are hard to decipher
      2) add 1 to methods that are used by another method
      3) subtract 1 from methods that are private
      4) subtract 1 from methods that only query
      5) write a test for any method with a score of 1 or higher


  File Structure

    /directory
      bob.rb <- store loops here
      /lib
        bob.rb <- store class here
      /test
        bob_test.rb

  Capturing puts

    opt. 1) variable = capture_IO do
         puts "string"
        end

      -this captures the puts data in a variable

    opt. 2) ruby filename.rb >> output.text


  Gems

    -simply a library/package of code
    -same as a module, except for location where they are stored
    -gems are usually packaged as modules

    ruby-toolbox.com


  TDD

    -tests w/o code

    1) require files that don't exist

    2) create required files

    3) add test class and get "uninitialized constant"

    4) create class

    5) test undefined class method and get "undefined method for <Main>"

    6) create class method

    7) test undefined class method and get "#<ClassName0X....>"

    8) create instance method


  Regex

    captures = ()

      -stores captures regex in a variable

      $1, $2, $3, $4, etc access matches

    Top-dog regex:

      /"([^"]*)"/

      -captures anything not a quote
      -ex. <a href="([^"])">

