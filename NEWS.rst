Change Log
----------

* v1.3.0
    - Fix the helper command line "setup" code to work with Python 2.4.
    - Include a ``go-setup`` script as an alternative to ``python -m go``
    - Experimental integration with `sources <https://github.com/trentm/sources>`_
    - ZSH support.
    - Support --open option on Mac OS X.
    - ``go`` now always uses the original Python executable

* v1.2.0
    -  Add support for "go FOO" falling back to changing to subdirectory
       "FOO" if there is no "FOO" shortcut. Patch from Phil Schwartz.

*  v1.1.0
    - Move to 'go-tool' Google Code project. (Couldn't use "go" because
      Google Code requires minimum 4 (or 3?) characters for a project
      name.)
    - Add automatic setup code to assist with setting up the shell
      integration drivers.

* v1.0.6
    - Redo changes to 'function go' that were made in version 1.0.4 so
      that people without my own personal Bash definitions can actually
      use it.

* v1.0.5
    - Fix bug where 'go' would fail to switch to a directory with spaces.

* v1.0.4
    - Improve Bash 'function go' to fail more gracefully if 'go' is
      not found on the PATH.

* v1.0.3
    - Correct information about the suggested Bash "go" function
      definition to avoid a user's possible "which" alias (some RedHat
      systems setup "alias which='type -p'") that can screw things up.

* v1.0.2
    - Filter out the stupid FCNTL.py deprecation warning for usage with
      Python 2.3 on Windows.

* v1.0.1
    - Ensure the installed 'go' script on non-Windows is executable.

* v1.0.0
    - Change version attributes and semantics. Before: had a _version_
      tuple. After: __version__ is a string, __version_info__ is a tuple.

* v0.9.2:
    - Fix install on Un*x: 'go' script wasn't in sdist to install

* v0.9.1:
    - Find gow.cpp again and get gow.exe into dists to fix installation and
      DQSD integration on Windows.

* v0.9.0:
    - Move hosting to trentm.com.
    - Improve starter docs a little bit.

* v0.8.2:
    - Ensure that "go SHORTCUT" switches to the correct drive on
      Windows when called in a subsystem:window environment (via the /D
      switch).
    - Drop the '-o' option added by the DQSD go.xml search. This means
      that openning the given path in the _shell_ is now the default, as
      it is for command line usage.

* v0.8.1:
    - Remove a debugging statement in 0.8.0 that caused "go SHORTCUT"
      to fail from Dave's Quick Search Deskbar.
    - Install go.py as 'go' in Linux, which executable bit set. Before
      this, getting go going was a real pain. It still is somewhat.

* v0.8.0:
    - Improve Windows integration: errors are now shown in dialogs rather
      than lost on the non-existant console.
    - Improve DQSD integration. The default action is not to open a shell
      to the stated directory. "go -o" can be used, as on the command
      line, to open a directory in Explorer.
    - Fix bug introduced in 0.7.0 whereby using go's innocuous options
      (-h, -V) could result in a directory change from the last "go"
      call.
    - Add explicit "-c" option for the default "change directories"
      action.
    - Improve shortcut listing output.

* v0.7.0:
    - Add an optional argument when listing (-l|--list) to be a pattern
      for existing shortcuts, e.g.::
      ``go -l foo  # lists all shortcuts with foo in them``
    - Add DQSD (Dave's Quick Search Deskbar) integration. After
      installation and a re-start of DQSD you should be able to jump to
      directory shortcuts via "go SHORTCUT[/SUBPATH]" in DQSD.

* v0.6.3:
    - first public release

