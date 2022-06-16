# zet
----
This has been inspired and influenced by [Rob Muhlestein](https://youtube.com/rwxrob).

Zet is a command line tool for creating and maintaining a personal Zettelkasten
(if you want to learn more about Zettelkasten, check mine out
[here](https://gitlab.com/michaelarn0ld/zettelkasten-public)). Please note that
this tool only works with Bash >= 4.0.

### GETTING STARTED
Before using this tool, there are a few prerequisites:
* Download ```zet``` from this repo to your machine and make sure that it is in
a place accessible by your ```$PATH``` environment variable
* In ~/.bashrc set the ```$EDITOR``` environment variable to your editor of choice
* Create a local directory where your Zettelkasten will live; make it a Git repo
and add a remote origin to your favorite Git repository hosting service.
* In this local zettelkasten directory, create a registry file ```REGISTRY.md```
* It's also a good idea to create a ```README.md``` file to describe your
objectives for the Zettelkasten
* Determine the location of bash by running: ```which bash```

### CONFIGURATION
Now that all the prerequisites have been met, you can configure ```zet``` so
it runs on your machine. Open ```zet``` in a text editor to make changes:
* Change the interpreter on ```zet``` to the output of ```which bash```
* Change ```PUBLIC``` to your local Zettelkasten directory
* If you want to have a private Zettelkasten, you may do the same thing for
```PRIVATE```. If you do not make a private Zettelkasten, please change this
line accordingly (note that you will not be able to use the ```-p``` or
```--private``` options).

### USAGE
```bash
zet [OPTION] [COMMAND] [ARGS...]
```
|   Command                  |   Usage                                                        |
|   :-:                      |   -                                                            |
|   all                      |   prints a list of all zettel ids in the zettelkasten          |
|   create [ZETTEL_NAME]     |   creates a new zettel                                         |
|   dir                      |   prints the session directory                                 |
|   edit [ZETTEL_ID]         |   edits an already existing zettel                             |
|   show [ZETTEL_TAG]        |   prints all zettels that have a matching tag                  |
|   isomin                   |   prints the current UTC datetime (YYYYMMDDHHMM)               |
|   link [ZETTEL_ID]         |   prints the markdown needed to link to a zettel               |
|   post [ZETTEL_ID]         |   tweets a zettelkasten title, tags, and url                   |
|   pull                     |   pulls the zettelkasten from its Git remote repository        |
|   push [MESSAGE]           |   pushes the local zettelkasten to its Git remote repository   |
|   read [ZETTEL_ID]         |   prints the contents of a zettel                              |
|   register [ZETTEL_TAG]    |   adds a tag to the registry if it is not there                |
|   tags [ZETTEL_ID]         |   prints all tags associated with a zettel                     |
|   topics                   |   prints all tags in the registry                              |
|   zk                       |   show all zettels in friendly format

----
|   Option                   |   Usage                                                        |
|   :-:                      |   -                                                            |
|   -h, --help               |   shows usages of zet                                          |
|   -p, --private            |   changes default session directory from PUBLIC to PRIVATE     |

