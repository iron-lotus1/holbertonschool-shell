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

#### SYNOPSIS
       cat [OPTION]... [FILE]...
<h4>cat<h4> concatenate files and print on the standard output

## [What about 2?](./3-twofiles) 
#### Script...
       cat /etc/passwd /etc/hosts
#### SYNOPSIS
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
#### SYPNOPSIS
       head [OPTION]... [FILE]...

 Print the first 10 lines of each FILE to standard output. With more than one FILE, precede each with a header giving the file name
#### OPTION
      -n, --lines=[-]NUM print  the  first NUM lines instead of the first 10; with the leading '-',
              print all but the last NUM lines of each file
## [Line #2](./6-third_line)
#### Script...
       head -n 3 iacta | tail -n 1

#### SYNOPSIS
       head [OPTION]... [FILE]...
out put the first part of the file
#### OPTION
       -n, --lines=[-]NUM

print the first NUM lines instead of the first 10; with the leading '-', print all but the last NUM lines of each file

#### Special characters
       |
Pipe " | " - Sends the output from one command to the input of another command. This is a method of chaining commands together

#### SYNOPSIS
       tail [OPTION]... [FILE]...

output the last part of the file

#### OPTION
       -n, --lines=[+]NUM

output the last NUM lines, instead of the last 10; or use -n +NUM to skip NUM-1 lines at the start
  
## [It is a good file that cuts iron without making noise](./7-file)
#### Script...
       echo "Best School" > '\''*\''\'"'"'"Best School"''\'"'"'\''\''*$\''?\''*\''*\''*
#### SYNOPSIS
       echo LONG-OPTION
#### Special Characters
       ''
Single quotes — protect the text inside them so that it has a literal meaning. With them, generally any kind of interpretation by Bash is ignored: special characters are passed over and multiple words are prevented from being split

       ""
Double quotes — protect the text inside them from being split into multiple words or arguments, yet allow substitutions to occur; the meaning of most other special characters is usually prevented.

       $
Expansion — introduces various types of expansion: parameter expansion

       \
Escape — (backslash) prevents the next character from being interpreted as a special character. This works outside of quoting, inside double quotes, and generally ignored in single quotes.

       *, ?
"wildcard" characters which match parts of filenames

## [Save current state of directory](./8-cwd_state)
#### Script...
       ls -la > ls_cwd_content
#### SYNOPSIS
       ls [OPTION]... [FILE]...

List information about the FILEs (the current directory by default). Sort entries alphabetically if none of -cftuvSUX nor --sort is specified
#### OPTION
        -a, --all       do not ignore entries starting with .
        -l              use a long listing format
#### Special Characters        
        >               Overwrite output - Sends command output to a file, deleting existing data

## [Duplicate last line](./9-duplicate_last_line)
#### Script...
       tail -n 1 iacta >> iacta
#### SYNOPSIS
       tail [OPTION]... [FILE]...
Print the last 10 lines of each FILE to standard output. With more than one FILE, precede each with a header giving the file name.
#### OPTION
       -n, --lines=[+]NUM
output the last NUM lines, instead of the last 10; or use -n +NUM to skip NUM-1 lines at the start

        >>              Append Output - Sends command output to a file, adding to the end without erasing

## [No more Javascript](./10-no_more_js)
#### Script... 
       find . -type f -name '*.js' -delete
#### SYNOPSIS
* find - search for files in a directory hierarchy
#### OPTION
       -type  f      
regular file

       -name pattern
Base  of  file  name (the path with the leading directories removed) matches
shell pattern pattern.  Because the leading  directories  are  removed, the file  names considered for a match with -name will never include a slash, so `-name a/b' will never match anything (you probably need to  use  -path)

       -delete

Delete files or directories; true if  removal  succeeded.   If  the  removal failed, an error message is issued and find's exit status will be nonzero (when it eventually exits).

## [Don't just count your directories, make your directories count](./11-directories)
#### Script...
       find . -mindepth 1 -type d | wc -l
#### SYNOPSIS
       find
#### OPTION
       -mindepth levels

Do not apply any tests or actions at levels less than levels (a non-negative integer). Using -mindepth 1 means process all files except the starting-points.

       -type d
directory
#### Special characters
       |
Pipe " | " - Sends the output from one command to the input of another command. This is a method of chaining commands together

#### SYNOPSIS
       wc [OPTION]... [FILE]

Print newline, word, and byte counts for each FILE, and a total line if more than one FILE is specified.  A word is a nonempty sequence of non white space delimited by white space characters or by start or end of input
#### OPTION
       -l, --lines

print the newline counts
## [What's new](./12-newest_files) 
#### Script...
       ls -t | head -n 10
#### SYNOPSIS
       ls [OPTION]... [FILE]
list directory contents
#### OPTION
            -t     sort by time, newest first; see --time
#### Special characters
       |
Pipe " | " - Sends the output from one command to the input of another command. This is a method of chaining commands together
#### SYNOPSIS
       head [OPTION]... [FILE]...
#### OPTION
       -n, --lines=[-]NUM

print the first NUM lines instead of the first 10; with the leading '-', print all but the last NUM lines of each file
## [Being unique is better than being perfect](./13-unique)
#### Script...
       sort | uniq -u
#### SYNOPSIS
       sort [OPTION]... [FILE]
sort lines of text files
#### Special characters
       |
Pipe " | " - Sends the output from one command to the input of another command. This is a method of chaining commands together
#### SYNOPSIS
       uniq [OPTION].. [INPUT [OUTPUT]]
report or omit repeated lines
Filter adjacent matching lines from INPUT (or standard input), writing to OUTPUT (or standard output).
#### OPTION
       -u, --unique      only print unique lines

## [It must be in that file](./14findthatword) 
#### Script...
       grep -E 'root' /etc/passwd
grep - print lines that match patterns
### SYNOPSIS
       grep [OPTION...] PATTERNS [FILE...]
       grep [OPTION...] -e PATTERNS ... [FILE...]
       grep [OPTION...] -f PATTERN_FILE ... [FILE...]

Pattern Syntax
       -E, --extended-regexp
              Interpret PATTERNS as extended regular expressions (EREs, see below).

## [Count that word](./15-countthatword) 
#### Script...
       grep -c "bin" /etc/passwd
#### SYNOPSIS
       grep [OPTION]... PATTERNS[FILE]
grep - print lines that match patterns
#### OPTION
       -c, --count
Suppress normal output; instead print a count of matching lines for each input  file.  With the -v, --invert-match option (see above), count non-matching lines.

## [What's next?](./16-whatsnext)
#### Script...
       grep -A 3 "root" /etc/passwd

#### SYNOPSIS
       grep [OPTION]... PATTERNS[FILE]
grep - print lines that match a pattern

#### OPTION
       -A NUM, --after-context=NUM
Print NUM lines of trailing context after matching lines.  Places a line
              containing a group separator (--) between contiguous groups of  matches.
              With  the -o or --only-matching option, this has no effect and a warning
              is given.
## [I hate bins](./17-hidethisword)
#### Script...
       grep -v "bin" /etc/passwd
#### SYNOPSIS
       grep [OPTION]... PATTERNS[FILE]
       
       print lines that match a pattern

#### OPTION
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
