# MacOS:  Installing Utilities with Homebrew

While Mac OS is Unix-based (specifically based
on BSD), it's technically not Linux-based. 

Unix is a family of operating systems, all stemming
from the first version developed in the 1960s.
Unix, however, was commercialized and required a license.

Linux is essentially a clone of Unix written from scratch
in order to create a free Unix-like system
(in fact, the name GNU was chosen as an acronym for "GNU's Not Unix").

For standardization, for all of the commands/utilities we'll
use in class, we'll assume the GNU versions.
Due to the above whole Unix / Linux history and
because Mac is based on BSD, the default versions of some
commands/utilties on mac are slightly different.

To solve this, if you are a mac user, you'll want to install
[homebrew](https://brew.sh/), a package manager
for macOS.
Linux users don't need to worry about this -- ubuntu already
has a package manager.

## Install Homebrew

Copy `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
and paste it into the terminal, then hit enter.

## Install packages

Anytime you want to install a package, you will run
`brew install packagename`.
At a bare minimum, you will want to run:

* `brew install wget`
* `brew install gawk`
* `brew install bash`
* `brew install grep`
* `brew install gnu-sed`
* `brew install gcc`
* `brew install make`
