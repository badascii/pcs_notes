Week 7 Notes - Rails and Databases
==================================

  Git
  ---

    -fetch brings us up to date with the master but does not move HEAD
    -when merge/rebase is used it then actually updates the local files
     (current working directory)

    Branches
      -origin = GitHub
      -master = a specific branch, either local or remote
      -it is a good idea to always make a new branch when working on an
       established project
      -origin is just a random branch name that is widely adopted due to GitHub
       using it as the default branch when cloning
      -"github" could easily replace "origin" as the default branch and may
       in the near future

      merge multiple branches:

        -git checkout master
        -git merge all

        -a branch is simply a pointer
        -it is a different place in the code's history


  Git Worlflow
  ------------

    -git checkout master
    -git checkout -b new_branch
    -git pull upstream master

    // make your changes

    -git commit -m "message"
    -git push origin branch_name

    // then make pull request on GitHub


  Open Source Contributions
  -------------------------

    -fork the repo
    -make a new branch
    -make a pull request


Types of Databases
------------------

  -MySQL

    -development has plateaued
    -currently being phased out in favor of other database options

  -Postgres

    -very simlilar to the SQL spec
    -extremely compact

  -Sqlite

    -unlike actual databases, it is just a file hosted locally
    -used locally in development and test environments


Foreign Keys
------------



