hail(1) -- Extract lines from a file
=============================================

## SYNOPSIS

`hail` <FIRST>-<LAST> ...

## DESCRIPTION

  Hail gets its name from a contraction of `head` and `tail`, the common
  alternative to this program. It extracts lines from a file, taken on stdin,
  and prints them on stdout. It's so simple that the *NIX wizards of old never
  bothered. But I'm lazy and prone to procrastination.

## SYNTAX

  Hail takes any number of `x`-`y` pairings as arguments. These pairs are
  integral numbers, corresponding to the first and last lines to print. The
  final number may be excluded to indicate that the remainder of the file
  should be printed

## EXAMPLES

  # prints 1 through 10, i.e. does nothing

  seq 1 10 | hail 1-


  # prints 1 through 3, i.e. equivalent to `head -n 3`

  seq 1 10 | hail 1-3

  # prints 3 through 5, i.e. equivalent to `head -n 5 | tail -n 3`

  seq 1 10 | hail 3-5

  # prints 5 through 10, i.e. equivalent to `tail -n 6`

  seq 1 10 | hail 5-

  # prints 2, 3, 5 and 7, which is where I'll give up on my comparisons to
  # head and tail

  seq 1 10 | hail 2-3 5-5 7-7


## AUTHOR

  Kevin Murray (daube) <spam@kdmurray.id.au>

## COPYRIGHT

  Copyright 2015 Kevin Murray <spam@kdmurray.id.au>

  Licensed under the GNU General Public License, version 3 or (at your option)
  any later version.