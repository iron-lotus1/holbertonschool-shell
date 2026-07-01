# Permissions

## [My name is Betty](./0-iam_betty) 

    su [options] [-] [<user> [<argument>...]]

Change the effective user ID and group ID to that of <user>.
A mere - implies -l.  If <user> is not given, root is assumed.

Options:
 -m, -p, --preserve-environment      do not reset environment variables
 -w, --whitelist-environment <list>  don't reset specified variables

 -g, --group <group>             specify the primary group
 -G, --supp-group <group>        specify a supplemental group

 -, -l, --login                  make the shell a login shell
 -c, --command <command>         pass a single command to the shell with -c
 --session-command <command>     pass a single command to the shell with -c
                                   and do not create a new session
 -f, --fast                      pass -f to the shell (for csh or tcsh)
 -s, --shell <shell>             run <shell> if /etc/shells allows it
 -P, --pty                       create a new pseudo-terminal

 -h, --help                      display this help
 -V, --version                   display version
## [Who am I](./1-who_am_i) 
    whoami [OPTION]...
Print the user name associated with the current effective user ID.
Same as id -un.
## [Groups](./2-groups)

    groups [OPTION]... [USERNAME]...
Print group memberships for each USERNAME or, if no USERNAME is specified, for
the current process (which may differ if the groups database has changed).

## [New Owner](./3-new_owner)
    chown [OPTION]... [OWNER][:[GROUP]] FILE...
  or:
   
    chown [OPTION]... --reference=RFILE FILE...
Change the owner and/or group of each FILE to OWNER and/or GROUP.
With --reference, change the owner and group of each FILE to those of RFILE.

#### OPTION
    -c, --changes          like verbose but report only when a change is made
    -f, --silent, --quiet  suppress most error messages
    -v, --verbose          output a diagnostic for every file processed
      --dereference      affect the referent of each symbolic link (this is
                         the default), rather than the symbolic link itself
    -h, --no-dereference   affect symbolic links instead of any referenced file
                         (useful only on systems that can change the
                         ownership of a symlink)
      --from=CURRENT_OWNER:CURRENT_GROUP
                         change the owner and/or group of each file only if
                         its current owner and/or group match those specified
                         here.  Either may be omitted, in which case a match
                         is not required for the omitted attribute
      --no-preserve-root  do not treat '/' specially (the default)
      --preserve-root    fail to operate recursively on '/'
      --reference=RFILE  use RFILE's owner and group rather than specifying
                         OWNER:GROUP values.  RFILE is always dereferenced.
    -R, --recursive        operate on files and directories recursively

The following options modify how a hierarchy is traversed when the -R
option is also specified.  If more than one is specified, only the final
one takes effect.

    -H                     if a command line argument is a symbolic link
                         to a directory, traverse it
    -L                     traverse every symbolic link to a directory
                         encountered
    -P                     do not traverse any symbolic links (default)
## [Empty](./4-empty)
## [Execute]()
## [Multiple permissions]()
## [Everybody!]()
## [James Bond]()
## [John Doe]()
## [Look in the mirror]()
## [Directories]()
## [More directories]()
## [Change group]()
## [Owner and group]()
## [Symbolic links]()
## [If only]()
