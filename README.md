pmu
===

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
USAGE: pmu git_br|git_co|git_st|pg|ps
Trigger actions on top of unix commands using percol interactive selection

MODE
    git_br      delete local branches that have been merged
    git_sh      apply action (add, stash, restore) to locally modified files
    git_co      apply action (add, stash, restore) to locally modified files
    psql        drop postgres databases
    pgrep       kill processes
~~~

# Config

You can define `co` and `st` git aliases in your `~/.gitconfig` as replacements for `checkout` and `status` commands :

~~~
[alias]
    # pmu must be present in $PATH
    st = "!f() { pmu git_st; }; f"
    co = "!f() { pmu git_co $1; }; f"
    trim = "!f() { pmu git_br $1; }; f"
~~~


# Contributing

My use of percol is based on my daily tools hence differs from your needs.
`pmu` should be considered as the place where to store your custom percol one-liners rather than a one-size-fits-all utility.  

You're encouraged to fork it, PR won't be merged unless they deal with a generic use case.


---
<i id="f1">1</i> `git`, `pg` and `psql` at time of writing
