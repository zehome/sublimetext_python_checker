# Python PEP-8 and PyFlakes checker for SublimeText 2 editor

This project is a plugin for [SublimeText 2](http://www.sublimetext.com/2) text editor.

# Original project
This is a fork of https://github.com/vorushin/sublimetext_python_checker

Please see his project too!

## Installation

Go to your Packages dir (Sublime Text 2 -> Preferences -> Browse Packages). Clone this repository into Packages subdirectory:

    git clone git://github.com/zehome/sublimetext_python_checker.git

Go to sublimetext_python_checker/ and create file local_settings.py with list of your preferred checkers:

<pre>
    CHECKERS = [('/usr/bin/pep8', []),
                ('/usr/bin/pyflakes', [])]
</pre>

First parameter is path to command, second - optional list of arguments. If you want to disable line length checking in pep8, set second parameter to ['--ignore=E501,E221'].

You can also set syntax checkers using sublimetext settings (per file, global,
per project, ...):
<pre>
    "settings":
    {
        "python_syntax_checkers":
        [
            ["/usr/bin/pep8", ["--ignore=E501,E128,E221"] ]
        ]
    }
</pre>
Both "CHECKERS local_settings" and sublime text settings will be used,
but sublime text settings are prefered. (using syntax checker binary name)


Restart SublimeText 2 and open some *.py file to see check results. You can see additional information in python console of your editor (go View -> Show Console).
