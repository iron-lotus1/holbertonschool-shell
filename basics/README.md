# Shell basic commands

## [Where am I](.0-current_working_directory)  
pwd - print name of currentworking directory

SYNOPSIS
       pwd [OPTION]...

## [What's in there](.1-listit) 
ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

## [There is no place like home](.2bring_me_home) 
cd = Change the current directory to DIR. The default DIR is the value of the HOME shell variable

## [The Long format](.3-listfiles)
ls - list directory contents
-l     use a long listing format

## [Hidden files](.4-listmorefiles) 
ls - list directory contents
-a, --all        do not ignore entries starting with .

## [I love numbers](.5-listfilesdigitonly)
ls - list directory contents
-l     use a long listing format
-n, --numeric-uid-gid
              like -l, but list numeric user and group IDs
-a, --all
              do not ignore entries starting with .

## [Welcome](.6-firstdirectory) 
mkdir - make directories

SYNOPSIS         mkdir [OPTION]... DIRECTORY...

## [Betty in my first directory](.7-movethatfile) 
mv - move (rename) files

SYNOPSIS
       mv [OPTION]... [-T] SOURCE DEST
       mv [OPTION]... SOURCE... DIRECTORY
       mv [OPTION]... -t DIRECTORY SOURCE...

## [Bye bye Betty](.8-firstdelete)
rm - remove files or directories

SYNOPSIS
       rm [OPTION]... [FILE]...

## [Bye bye my first directory](.9-firstdirdeletion) 
rmdir - remove empty directories

SYNOPSIS
       rmdir [OPTION]... DIRECTORY...

## [Back to the future](.10-back) 
cd -  Change Directory to the previous directory
Change the current directory to DIR.  
The default DIR is the value of the
HOME shell variable. If DIR is -, it is converted to $OLDPWD

\$OLDPWD - is a built in shell environment variable in Unix like OS. The shell updates this variable automatically every time you successfully change directories using the cd command.

## [List](.list)
ls - list directory contents
-a, --all        do not ignore entries starting with . 
-l               use a long listing format

## [File type](.12-file_type) 
file [FILE...] = Determine type of FILEs

## [We are symbols, and inhabit symbols](.13-symbolic_link)
ln - make links between files

SYNOPSIS
       ln [OPTION]... [-T] TARGET LINK_NAME
       ln [OPTION]... TARGET
       ln [OPTION]... TARGET... DIRECTORY
       ln [OPTION]... -t DIRECTORY TARGET...

-s, --symbolic     Make symbolic links instead of hard links

## [Copy HTML files](.14-copy_html)
cp - copy files and directories
SYNOPSIS
       cp [OPTION]... [-T] SOURCE DEST
       cp [OPTION]... SOURCE... DIRECTORY
       cp [OPTION]... -t DIRECTORY SOURCE...

-a, --archive
              same as -dR --preserve=all

-R, -r, --recursive
              copy directories recursively

-u     equivalent to --update[=older]

## [List's move](.15-lets_move)
mv - move (rename) files

SYNOPSIS
       mv [OPTION]... [-T] SOURCE DEST
       mv [OPTION]... SOURCE... DIRECTORY
       mv [OPTION]... -t DIRECTORY SOURCE...

POSIX-style characters

[[upper]] - uppercase alphabetic charicters

more options

[[lower]] - lowercase alphabetic charicters
[[digit]] - numeric charicters
[[blank]] - space and TAB characters
[[punct]] - punctuation characters (characters that are not letters, digits, control characters, or spaces)

 - Wildcard character representing zero or mor characters 

## [Clean Emacs](.16-clean_emacs) 
rm - remove files or directories

 - Wildcard character representing zero or mor characters

~ - The literal tilde character

## [Tree](.17-tree)
mkdir - make directories

-p, --parents
              no  error  if existing, make parent directories as needed, with their file
              modes unaffected by any -m option.
