## Shell, init files, variables and expansions

## [<0>](./0-alias)
#### Script...
    alias ls="rm -f *"
#### SYPNOPSIS
    alias [alias-name[=string]...]
    
    The alias utility shall create or redefine alias definitions or write the values of existing alias definitions to standard output. An alias definition provides a string value that shall replace a command name when it is encountered
## [Hello You](./1-hello_you)
#### Script...
    echo "hello $USER"
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### SHORT-OPTION
    "hello"
#### Environment Variable
    $USER
    
    Contains the alphanumeric username of the current logged in user

## [The path to success is to take massive, determined action](./2-path)
#### Script...
    export PATH=$PATH:/action
#### SYPNOPSIS

#### OPTION
## [If the path be beautiful, let us not ask where it leads](./3-paths)
#### Script...
    echo "$PATH:/" | grep -o ":/" | wc -l
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### OPTION
    $PATH:/ 
    
    A colon-separated list of directories where the system searches for executable binaries

#### Special Characters
    |
    
    Pipe " | " - Sends the output from one command to the input of another command. This is a method of chaining commands together
#### SYPNOPSIS
    grep [OPTION]... PATTERNS [FILE]
#### OPTION
    -o, --only-matching
    
    Print only the matched (non-empty) parts of a matching line, with each such part on a separate output line.
#### SYPNOPSIS
    wc [OPTION]... [FILE]...
#### OPTION
    -l, --lines
    
    print the newline counts
## [Global variables](./4-global_variables)
#### Script...
    printenv
#### SYPNOPSIS
    printenv [OPTION] [VARIABLE]...
#### POSSIBLE OPTION
    -0, --null
    
    end each output line with NUL, not newline
## [Local variables](./5-local_variables)
#### Script...
    set
#### SYPNOPSIS
    set -- [argument...]

#### DESCRIPTION
    If no options or arguments are specified, set shall write the names and values of all shell variables in the collation sequence of the current locale. Each name shall start on a separate line, using the format: "%s=%s\n", <name>, <value>
## [Local variable](./6-create_local_variable)
#### Script...
    BEST=School
#### CREATING VARIABLE
    NAME="value"

    Variables are case sensitive and capitalized by default. Giving local variables a lowercase name is a convention which is sometimes applied. However, you are free to use the names you want or to mix cases. Variables can also contain digits, but a name starting with a digit is not allowed
#### EXAMPLES
    MYVAR1="2"
    first_name="Franky"
    full_name="Franky M. Singh"
## [Global varible](./7-create_global_variable)
#### Script...
    export BEST=School
#### SYPNOPSIS
    export name[=word]...
#### DESCRIPTION
    The shell shall give the export attribute to the variables corresponding to the specified names, which shall cause them to be in the environment of subsequently executed commands. If the name of a variable is followed by =word, then the value of that variable shall be set to word.
## [Every addition to tru knowledge is an addition to human power](./8-true_knowledge)
#### Script...
    echo $(($TRUEKNOWLEDGE + 128))
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### ARTHMETIC EXPANSION

## [Divide and rule](./9-divide_and_rule)
#### Script...
    echo "$(($POWER / $DIVIDE))"
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### ARTHMETIC EXPANSION

## [Love is anterior to life, posterior to death, initial of creation, and the exponent of breath](./10-love_exponent_breath)
#### Script...
    echo $((BREATH ** LOVE))
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### ARTHMETIC EXPANSION
## [There are 10 types of people in the world - Those who understand binary, and those who don't](./11-binary_to_decimal)
#### Script...
    echo $((2#$BINARY))
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### ARTHMETIC EXPANSION
## [Combination](./12-combinations)
#### Script...
    echo {a..z}{a..z} | tr ' ' '\n' | grep -v oo
#### SYPNOPSIS
    echo [SHORT-OPTION]... [STRING]...
#### BRACE EXPANSION
    {a..z} or {1..9} or {Z..A} or {A{1,},B{3,4}}

    We can create multiple text strings from a pattern. Patterns to be brace expanded may contain a leading portion called a preamble and a trailing portion called a postscript. The brace expression itself may contain either a comma-separated list of strings, or a range of integers or single characters. The pattern may not contain embedded whitespace.

    The most common application is to make lists of files or directories to be created.
    

#### EXAMPLE
    
    
    If we were a photographer and had a large collection of images we wanted to organize into years and months, the first thing we might do is create a series of directories named in numeric “Year-Month” format. This way, the directory names will sort in chronological order. We could type out a complete list of directories, but that's a lot of work and it's error-prone too. 
####        
    $ mkdir {2017..2019}-{01..12}
    
    $ ls
    2017-01 2017-07 2018-01 2018-07 2019-01 2019-07
    2017-02 2017-08 2018-02 2018-08 2019-02 2019-08
    2017-03 2017-09 2018-03 2018-09 2019-03 2019-09
    2017-04 2017-10 2018-04 2018-10 2019-04 2019-10
    2017-05 2017-11 2018-05 2018-11 2019-05 2019-11
    2017-06 2017-12 2018-06 2018-12 2019-06 2019-12

## [Floats](./13-print_float)
#### Script...
    printf "%.2f\n" $NUM

## [Decimal to Hexadecimal](./14-decimal_to_hexadecimal)
#### Script...
    printf "%X\n" $DECIMAL

