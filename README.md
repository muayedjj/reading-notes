# Reading Notes
 - *An ongoing documentation of new knowledge acquired and related resources.*
   - This repository is meant to keep track of and document pesonal progress in the coding field in terms of new learning experiences and studies.
<br/><br/>
### Author: [Muayad Al Shareef](https://github.com/muayedjj)
<br/>

## **1. Code 102** - Intro to Software Development
## **2. Code 201** - Foundations of Software Development
## **3. Code 301** - Intermediate Software Development
## **4. Code 401** - Advanced Software Development
<br/>

| Day/Date | Subject | Resources | Remarks |
| -------- | ------- | --------- | ------- |
| Day 1 <br/> May 26th 2022 | <ul><li>Python</li><li>MD features</li><li>The Command Line</li></ul> |     <ul><li>https://www.sololearn.com</li><li>https://www.markdownguide.org/extended-syntax/</li><li>https://ryanstutorials.net/linuxtutorial/</li></ul> | Python Core - new |
| DAy 2 <br/> | - | - | None |

<br/><hr/>
### **CLI Tips & Tricks:**
- **The `man`ual pages:** A set of pages that explain every command available on your system.
  - **`man <command to look up>`**
  - _To exit the `man` pages press 'q' for quit._
- When you enter commands, they are actually stored in a history. You can traverse this history using the up and down arrow keys.
- Useful Commands:
    - `pwd`: Print Working Directory
    - `cd [location]`: Move around ^^
      - `/etc`: Stores config files for the system.
      - `/var/log` :Stores log files for various system programs.
      - `/bin` and `/usr/bin`: The location of several commonly used programs.
      - _Note that If you run the command cd without any arguments then it will always take you back to your home directory._
        
    - `ls [options] [location]`: _Arguments within the square brackets ( `[ ]` ) are optional_, but the can be put to use as follows:
      - `ls -l` : long listing
      - `ls /etc` : used to not to list our current directory but instead to list that directories contents.
      - `ls -a` : list **all**; as in: "list everything, even hidden contents."
    - `file`: obtain information about what type of file a file or directory is.
    - `mkdir`: Make Directory - ie. Create a directory.
    - `rmdir`: Remove Directory - ie. Delete a directory.
    - `touch`: Create a blank file.
    - `cp`: Copy a file or directory.
    - `mv`: Move a file or directory _(can also be used to rename)_.
    - `rm`: Remove - ie. Delete a file.


- Paths:
    - Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( `/` ).
    - Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.
- **Tab Completion:** When you start typing a path you may hit the Tab key on your keyboard at any time which will invoke an auto complete action.
  - As long as you're operating within Linux:
    - Everything is a File.
    - Linux is an Extensionless System: _Linux the system actually ignores the extension and looks inside the file to determine what type of file it is._
    - Linux is Case Sensitive.
    - Spaces in file and directory names are perfectly valid but we need to be a little careful with them. As you would remember, a space on the command line is how we seperate items. To avoid issues you have three options:
      - Quotes **' '** <br/> `cd 'Whatever Name With Spaces'`
      - Escape Characters <br/> `cd Whatever\ Name\ With\ Spaces`
      - The aforementioned **Tab Completion**
- Searching
  - `man -k <search term>`: <br/> It is possible to do a keyword search on the Manual pages. This can be helpful if you're not quite sure of what command you may want to use but you know what you want to achieve.
    - `man -k <search term>` <br/> 
    Do a keyword search for all manual pages containing the given search term.
    - `/<term>` Within a manual page, perform a search for 'term'.
    - **`n`** After performing a search within a manual page, select the next found item.
    - **`q`** exit the man pages.
- Long hand command line options begin with two dashes ( -- ) and short hand options begin with a single dash ( - ) <br/> example: `ls -a` **==** `ls --all`
- **No undo** <br/>
The Linux command line does not have an undo feature. Perform destructive actions carefully.
 - ### More in [**The CL Cheat Sheet**](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
