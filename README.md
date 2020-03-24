pmu
===

_percol made useful_
![](https://i.imgur.com/36a11KE.png)



> **/pmu/** :
>
>
>    1. *noun.* a place where one can bet on horse races, usually a café or tabac
>    2. *acronym.* Percol Made Useful

# Description

`pmu` brings actions on top of unix commands<sup id="a1">[1](#f1)</sup> using [`percol`](https://github.com/mooz/percol)
_interactive filtering_ concept.

I love `percol` but thought it was lacking from a practical standpoint,
forcing me to manipulate `xargs` and `awk` to pipe it with others commands.  
An alternative would be to use aliases and bash functions but I prefer having
a single script for maintainability.

# Usage

~~~
USAGE: mokapot [OPTIONS] git_br|git_co|git_st|pg|ps
Trigger actions on top of unix commands using percol interactive selection

MODE
    git_br      delete local branches that have been merged
    git_sh      apply action (add, stash, restore) to locally modified files
    git_co      apply action (add, stash, restore) to locally modified files
    pg          drop postgres databases
    ps          kill processes

OPTIONS
    The options are passed to the underlying binary (eg 'git' for 'moka git')
~~~

# Contributing

My use of percol is based on my daily tools hence differs from your needs.
`pmu` should be considered as the place where to store your custom percol one-liners rather than a one-size-fits-all utility.  

You're encouraged to fork it, PR won't be merged unless they deal with a generic use case.


---
<i id="f1">1</i> `git`, `pg` and `psql` at time of writing
