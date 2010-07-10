twitter-lists-cli
=================
A command-line client for manipulating large Twitter lists in the shell, shell scripts, etc.

Currently supports
------------------
- OAuth authentication (twitter-auth)
- Showing a users's followers/following
- Following and unfollowing users
- Showing, adding, and removing a members from a list

Commands included:
------------------
### twitter-auth
    usage: twitter-auth
    Get OAuth credentials.

    Global Options:
            --auth FILE                  Read authentication data from the specified FILE

### twitter-follow
    usage: twitter-follow [-l LISTNAME] [--only | -d] [USER...]
    Follow or unfollow users.

        -l, --list LISTNAME              act on the specified LISTNAME instead of the logged-in user
        -d, --unfollow                   unfollow the specified users

    If no USERs are specified on the command line, they will be read from stdin.

    Global Options:
            --auth FILE                  Read authentication data from the specified FILE

### twitter-following
    usage: twitter-following [-r] [-u USER] [-l LISTNAME]
    Show who is being followed by a user or a list.

        -u, --user USER                  specify a username (default is the logged-in user)
        -l, --list LISTNAME              show members of the user's LISTNAME instead of the user's followers
        -r, --reverse                    show followers instead of who is following

    Global options:
            --auth FILE                  Read authentication data from the specified FILE

### twitter-lists
    usage: twitter-lists [-s] [-u USER] [-c LISTNAME... | -C LISTNAME... | -d LISTNAME...]
    Show, create, or delete lists.
        -u, --user USER                  specify a username (default is the logged-in user)
        -c, --create                     create the specified list(s)
        -C, --create-private             create private list(s)
        -d, --delete                     delete the specified list(s)
        -s, --slugs                      Use slugs instead of (possibly non-unique) names

    If no LISTNAMEs are specified on the command line, they will be read from stdin.

    Global options:
            --auth FILE                  Read authentication data from the specified FILE

License
-------
Copyright (c) 2010 Dwayne Litzenberger

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
