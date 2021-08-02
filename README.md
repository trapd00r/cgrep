## cgrep - grep with colors without the grep

![cgrep](/assets/cgrep.png)

## USAGE

    cgrep <regex>

## DESCRIPTION

grep is great and I use it all the time. At times I want to hilight
output data like grep can do with $GREP\_COLORS, but without actually
**filtering** the results. This program does just that.

## OPTIONS

TODO

## ENVIRONMENT

There's two environment variables that can be read and processes by cgrep:

    CGREP_MATCH
    CGREP_NONMATCH

The first one defines the colors and attributes given to a match, the
second one decides how what **not** matched should look like.

cgrep makes use of Term::ExtendedColor, and can therefore use a
range of color/attribute definitions:

    export    CGREP_MATCH=red
    export CGREP_NONMATCH=white

    export    CGREP_MATCH=38;5;196;1 # bold red (color index 196)
    export CGREP_NONMATCH=38;5;88;3  # italic darker red

## EXAMPLES

    # match one or more digits that's not preceeded by mp|MP, as in MP3.
    beet ls artist:laleh | cgrep '(?<!(?i:mp))\d+'

## REPORTING BUGS

Report bugs and/or feature requests on rt.cpan.org, the repository issue tracker
or directly to [m@japh.se](https://metacpan.org/pod/m%40japh.se)

## AUTHOR

    Magnus Woldrich
    CPAN ID: WOLDRICH
    m@japh.se
    japh@irc.libera.chat #perl
    L<~/|http://japh.se>
    L<git|http://github.com/trapd00r>

## CONTRIBUTORS

None required yet.

## COPYRIGHT

Copyright 2021- **THIS APPLICATION**s ["AUTHOR"](#author) and ["CONTRIBUTORS"](#contributors) as listed
above.

## LICENSE

This program is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

## SEE ALSO

[~/](http://japh.se)
