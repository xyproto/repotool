A utility that deals with git repositories and AI.

1. Open "repotool" in a directory that has a .git folder
2. Offer a REPL with actions:
   * p = git pull
   * f = git fetch
   * c = git commit, in a controlled way: be an interface for git commit -a -p or something, let the user select what to commit in steps
   * r = git rebase -i origin/main ("main" or whatever the default branch of the repo is)
   * b = ask AI to find a bug
   * t = ask AI to find a typo
   * r = ask AI to refactor
   * a = add AI to add code to a file
   * i = instruct the AI to do something


The AI must have tools/function calling and be able to:

* Add a function
* Remove a function
* Modify a function

* Add a line
* Remove a line
* Modify a line

* Add a blank file
* Remove a file
* Rename a file

* Run the compilation step
* Add an argument to the program run configuration
* Remove an argument from the program run configuration
* Modify an argument in the program run configuration

* Add an environment variable to the program run configuration
* Remove an environment variable from the program run configuration
* Modify an environment variable in the program run configuration

* Run the program with no arguments or environment variables
* Run the program with the stored arguments and environment variables

etc

The main idea here is:

* Git repository folder + REPL + AI tool calling

Start out by creating a Go package for abstracting a folder that is a git checkout.
