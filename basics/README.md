## Shell basic commands

* [Where am I](./0-current_working_directory) pwd = Print the name of the current working directory
* [What's in there](./1-listit) ls = List information about the files (the current directory by default)
* [There is no place like home](./2bring_me_home) cd = Change the current directory to DIR. The default DIR is the value of the HOME shell variable
* [The Long format](./3-listfiles) ls -l = Use a long listing format
* [Hidden files](./4-listmorefiles) ls -a = Include names starting with .
* [I love numbers](./5-listfilesdigitonly) ls -lna = List numeric UIDs and GIDs instead of names
* [Welcome](./6-firstdirectory) mkdir filename = Create Directory
* [Betty in my first directory](./7-movethatfile) mv filename = Rename source to dest or move source to directory
* [Bye bye Betty](./8-firstdelete) rm filename = Remove or unlink file
* [Bye bye my first directory](./9-firstdirdeletion) rmdir DIRname = Remove directory if it is empty
* [Back to the future](./10-back) cd - = Change Directory to the previous directory
* [List](./11-lists)
* [File type](./12-file_type) file [OPTION...] [FILE...] = Determine type of FILEs
* [We are symbols, and inhabit symbols](./13-symbolic_link) ln [OPTION]... TARGET = Create a link to the TARGET in the current directory || -s, --symbolic = Make symbolic links instead of hard links
* [Copy HTML files](./14-copy_html) Copy SOURCE to DEST, or multiple SOURCEs to DIRECTORY
* [List's move](./15-lets_move) Rename SOURCE to DEST, or move SOURCEs to DIRECTORY
* [Clean Emacs](./16-clean_emacs)
* [Tree](./17-tree) Create the DIR if they do not already exist || -p, --parents = no error if existing, make parent directories as needed
