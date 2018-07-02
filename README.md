Kala Core integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/robinsage-dev/kala.svg?branch=master)](https://travis-ci.org/robinsage-dev/kala)

https://kalatoken.io

What is Kala?
----------------

Kala is a fork of Bitcoin created exclusively for the Symatri ecosystem. It introduces
a few functional changes including different magic message, ports, and address prefixes.
It also introduces economic changes including block time, block reward, a premine, and
maximum coin supply.

For more information on Bitcoin, see https://bitcoin.org/en/download, or read the
[original whitepaper](https://bitcoincore.org/bitcoin.pdf).

License
-------

Kala Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/robinsage-dev/kala/tags) are created
regularly to indicate new official, stable release versions of Kala Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://www.transifex.com/projects/p/bitcoin/).

Translations are periodically converted to Kala.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Translators should also subscribe to the Bitcoin [mailing list](https://groups.google.com/forum/#!forum/bitcoin-translators).
