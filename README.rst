sphinx-libretto
###############

An experiment with a Libretto in Sphinx.

This is a very early stage, and ideally it will become a real
plug-in. Right now, however, it's a functional pair of themes.

It requires the addition of at least one new role, ``action``,
so that we can mark stage direction, etc. It supports either
creating an explicit ``actor`` role, or using the Sphinx
defaults. So, basically::

    .. role:: actor
    .. role:: action

    .. default-role:: actor

The ``action`` needs to be used with a ``container``, so that
references to actors within it will be formatted properly.
So, basically::

    .. container:: action

       `Billy` screams and falls down.

Since this is designed for musical librettos, we also need
to deal with sung parts. When one person sings, it is easy::

    ..  

            `Billy`

            | How I want this nightmare to end.
            | They've eaten my dearest friend.

Dealing with multiple parts gets treatment with a table for
HTML, but also needs special-casing for ePUB output.

See: http://yam655.com/experiments/libretto

