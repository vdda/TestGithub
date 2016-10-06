# TestGithub
Getting a Git Repository

You can get a Git project using two main approaches. 
 - The first takes an existing project or directory and imports it into Git. 
 - The second clones an existing Git repository from another server.

== Initializing a Repository in an Existing Directory ==

If you’re starting to track an existing project in Git, you need to go to the project’s directory and type

$ git init

This creates a new subdirectory named .git that contains all of your necessary repository files — a Git repository skeleton. At this point, nothing in your project is tracked yet. 


$ git add *.c
$ git add README
$ git commit -m 'initial project version'


If you want to get a copy of an existing Git repository — for example, a project you’d like to contribute to — the command you need is git clone. If you’re familiar with other VCS systems such as Subversion, you’ll notice that the command is clone and not checkout. This is an important distinction — Git receives a copy of nearly all data that the server has. Every version of every file for the history of the project is pulled down when you run git clone. In fact, if your server disk gets corrupted, you can use any of the clones on any client to set the server back to the state it was in when it was cloned (you may lose some server-side hooks and such, but all the versioned data would be there
You clone a repository with git clone [url]. For example, if you want to clone the Ruby Git library called Grit, you can do so like this:

$ git clone git://github.com/schacon/grit.git

That creates a directory named grit, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new grit directory, you’ll see the project files in there, ready to be worked on or used. 
If you want to clone the repository into a directory named something other than grit, you can specify that as the next command-line option:

$ git clone git://github.com/schacon/grit.git mygrit

That command does the same thing as the previous one, but the target directory is called mygrit.

$ git status
$ git add README
$ git commit -m "Story 182: Fix benchmarks for speed"

AND

$git log
