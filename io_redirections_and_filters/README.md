# Shell, I/O Redirection and Filters
## [Hello World](./0-hello_world) 
#### Script...
       echo "Hello, World"
echo "TEXT HERE" display a line of text
## [Confused smiley](./1-confused_smiley)
#### Script...
      echo "\"(Ôo)'"
 <h4>Escape - (backslash)<h4> prevents the next character from being interpreted as a special charicter. This works outside of quoting, inside double quotes, and generally ignored in single quotes. To specify a plain left-bracket use \

### 
      ' '
###       
<h4>Single quotes<h4> protect the text inside them so that it has a literal meaning. With them, generally any kind of interpretation by Bash is ignored: special characters are passed over and multiple words are prevented from being split

###
       " "
###      
<h4>Double quotes<h4> protect the text inside them from being split into multiple words or arguments, yet allow substitutions to occur: the meaning of most other special charicters is usually prevented

## [Let's display a file](./2-hellofile)
#### Script...
       cat /etc/passwd

<h4>cat<h4> concatenate files and print on the standard output

#### SYNOPSIS
       cat [OPTION]... [FILE]...
## [What about 2?](./3-twofiles) 
#### Script...
       cat /etc/passwd /etc/hosts
#### SYNOPSIS
#### Same concept as previious, but adding another file path

       cat [FILE]... [FILE]...
## [Last lines of a file](./4-lastlines) 
#### Script...
       tail -n 10 /etc/passwd
tail - output the last part of file.
#### SYNOPSIS
       tail [OPTION]... [FILE]...
#### OPTION
       -n, --lines=[+]NUM
###
output the last NUM lines, instead of the last 10; or use -n +NUM to skip NUM-1 lines at the start
## [I'd prefer the first one actually](./5-firstlines) 
#### Script...
       head -n 10 /etc/passwd
head - output the first part of files
###
      -n, --lines=[-]NUM print  the  first NUM lines instead of the first 10; with the leading '-',
              print all but the last NUM lines of each file
## [Line #2](./6-third_line)
#### Script...
       head -n 3 iacta | tail -n 1
head - out put the first part of the file
tail - output the last part of the file
   | - Pipe "|" send the output from one command to the input of another command. This is a method of chaining commands together
  
## [It is a good file that cuts iron without making noise](./7-file)
#### Script...
       echo "Best School" > '\''*\''\'"'"'"Best School"''\'"'"'\''\''*$\''?\''*\''*\''*


## [Save current state of directory](./8-cwd_state)
#### Script...
       ls -la > ls_cwd_content

ls - list directory contents
        -a, --all       do not ignore entries starting with .
        -l              use a long listing format
        >               Overwrite output - Sends command output to a file, deleting existing data

## [Duplicate last line](./9-duplicate_last_line)
#### Script...
       tail -n 1 iacta >> iacta
###
        >>              Append Output - Sends command output to a file, adding to the end without erasing

## [No more Javascript](./10-no_more_js)
#### Script... 
       find . -type f -name '*.js' -delete

* find - search for files in a directory hierarchy

-type c  File is of type c:

              b      block (buffered) special

              c      character (unbuffered) special

              d      directory

              p      named pipe (FIFO)

              f      regular file

              l      symbolic link; this is never true if the -L option or the -follow op‐
                     tion  is  in effect, unless the symbolic link is broken.  If you want
                     to search for symbolic links when -L is in effect, use -xtype.

              s      socket

              D      door (Solaris)

              To search for more than one type at once, you can supply the  combined  list
              of type letters separated by a comma `,'


-name pattern
              Base  of  file  name (the path with the leading directories removed) matches
              shell pattern pattern.  Because the leading  directories  are  removed,  the
              file  names considered for a match with -name will never include a slash, so
              `-name a/b' will never match anything (you probably need to  use  -path

-delete
              Delete files or directories; true if  removal  succeeded.   If  the  removal
              failed,  an  error  message is issued and find's exit status will be nonzero
              (when it eventually exits).

## [Don't just count your directories, make your directories count](./11-directories)
#### Script...
       find . -mindepth 1 -type d | wc -l

## [What's new](./12-newest_files) 
#### Script...
       ls -t | head -n 10

ls - list directory contents
            -t     sort by time, newest first; see --time

## [Being unique is better than being perfect](./13-unique)
#### Script...
       sort | uniq -u
sort - sort lines of text files

uniq - report or omit repeated lines
            -u, --unique      only print unique lines

## [It must be in that file](./14findthatword) 
#### Script...
       grep -E 'root' /etc/passwd
grep - print lines that match patterns
SYNOPSIS
       grep [OPTION...] PATTERNS [FILE...]
       grep [OPTION...] -e PATTERNS ... [FILE...]
       grep [OPTION...] -f PATTERN_FILE ... [FILE...]

Pattern Syntax
       -E, --extended-regexp
              Interpret PATTERNS as extended regular expressions (EREs, see below).

## [Count that word](./15-countthatword) 
#### Script...
       grep -c "bin" /etc/passwd

grep - print lines that match patterns

General Output Control
       -c, --count
              Suppress normal output; instead print a count of matching lines for each
              input  file.  With the -v, --invert-match option (see above), count non-
              matching lines.

## [What's next?](./16-whatsnext)
#### Script...
       grep -A 3 "root" /etc/passwd
grep - print lines that match a pattern

Context Line Control
       -A NUM, --after-context=NUM
              Print NUM lines of trailing context after matching lines.  Places a line
              containing a group separator (--) between contiguous groups of  matches.
              With  the -o or --only-matching option, this has no effect and a warning
              is given.
## [I hate bins](./17-hidethisword)
#### Script...
       grep -v "bin" /etc/passwd
grep - print lines that match a pattern

-v, --invert-match
              Invert the sense of matching, to select non-matching lines.

## [Letters only please](./18-letteronly)
#### Script...
       grep '^[[:alpha:]]'  /etc/ssh/ssdh_config

Character Classes and Bracket Expressions 
certain  named  classes  of  characters are predefined within bracket expressions, as follows. Their  names  are  self  explanatory,  and  they  are:
*      [:alnum:]
*      [:alpha:]  
*      [:blank:]  
*      [:cntrl:] 
*      [:digit:] 
*      [:graph:] 
*      [:lower:]
*      [:print:] 
*      [:punct:]
*      [:space:]  
*      [:upper:]
*      [:xdigit:]

For  example, [[:alnum:]]  means  the  character  class of numbers and letters in the current locale.

#### Anchoring
###
       ^ 
       $
The  caret ^ and the dollar sign $ are meta-characters that respectively match the empty string at the beginning and end of a line.
##### ^ represents the start of the current line in multi-line mode, otherwise the start of the string
##### \$ represents the end of the current line in multi-line mode, otherwise the end of the string

## [A to Z](./19-AZ) 
#### Script...
       tr 'Ac' 'Ze'
tr - translate or delete characters

## [Without C, you would live in hiago](./20-hiago) 
#### Script...
       tr -d Cc

<h4>tr<h4> translate or delete characters

#### SYNOPSIS
       tr [OPTION]... STRING1 
#### OPTION
         -d, --delete  delete characters in ARRAY1, do not translate
## [esreveR](./21-reverse)
#### Script...
       rev
rev - reverse lines characterwise
#### SYNOPSIS
       rev [option] [file...]

## [DJ Cut Killer](./22-users_and_homes)
#### Script...
       cut -f 1,6 -d : /etc/passwd | sort
