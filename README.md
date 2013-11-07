This is a repository of [Valgrind suppression files](http://valgrind.org/docs/manual/manual-core.html#manual-core.suppress) intended to be used to detect memory leaks in GNOME software using Valgrind.

## Getting started

You will need Valgrind, GNU Make, and `sed`.

 1. Open a terminal and `cd` into `GNOME.supp`.

 2. `make`

GNU Make will generate suppression (SUPP) files in the project root.
To use them with Valgrind, pass a [`--suppressions=<filename>`](http://valgrind.org/docs/manual/manual-core.html#opt.suppressions) option for each suppression file that you would like to use. For example, to use the suppressions in `glib.supp`, you would pass `--suppressions=/path/to/GNOME.supp/glib.supp` to Valgrind.

A `all.supp` file is created including all suppressions.

You can also add suppression lines to a ~/.valgrindrc file to automatically use them every time.

See the [Valgrind page on GNOME Live!](http://live.gnome.org/Valgrind) for tips on using Valgrind to detect memory leaks in GNOME software.
