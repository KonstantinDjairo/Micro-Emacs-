mg
==
This is a portable version of the Mg editor from OpenBSD.

Mg is intended to be a small, fast, and portable editor for people who
can't (or don't want to) run emacs for one reason or another, or are not
familiar with the vi editor. It is compatible with emacs because there
shouldn't be any reason to learn more editor types than emacs or vi.

This repository aggressively tracks upstream.

Compiling
---------
`mg` has a simple configure script that generates a `POSIX` `Makefile`.
```
$ ./configure
$ make
$ sudo make install
```

Dependencies
------------
By default, you need the ncurses library.

NetBSD users will use the in-base NetBSD curses library.

If you do not have the ncurses library, you can call `configure` with the
`--with-builtin-curses` flag to compile with a simplified version of the
NetBSD curses library. In this setup, there are no dependencies other than
the system's libc.

Single-user mode
----------------
When configured with `--enable-static` and `--with-builtin-curses`, the
resulting `mg` binary can use used in single-user mode if placed in `/`
or `/bin` or some other directory accessible in single-user mode.

`mg` can be invoked in single-user mode similar to:
```
$ TERM=vt100 mg
```

Testing
-------
Tested on recent versions of Arch, Alpine, Cygwin, Debian, DragonFly BSD,
FreeBSD, Mac OS X (10.4 or later), NetBSD, Slackware, and Ubuntu.

Licensing
---------
Files originating from `mg` are Public Domain. Files needed for portability
have their own individual license headers.
All licenses are ISC or BSD.

Commonly asked questions
------------------------
`mg` does not yet support UTF-8. If you would like to work on this, please
reach out to the tech@ mailing list on OpenBSD.

Get a tarball
-------------
See the Releases tab on GitHub.
The latest version is mg-7.0.
