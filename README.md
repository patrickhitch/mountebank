mountebank
==========

mountebank is the first open source tool to provide cross-platform, multi-protocol test doubles over the wire.
Just point your application to mountebank instead of the real dependency,
and test like you would with traditional stubs and mocks.

At the moment, the following protocols are supported:
* http
* https
* tcp (text and binary)
* smtp

mountebank supports mock verification, stubbing with advanced predicates, JavaScript injection,
and record-playback through proxying.

[![how it works](https://github.com/bbyars/mountebank/blob/master/src/public/images/overview.gif?raw=true)](https://github.com/bbyars/mountebank/blob/master/src/public/images/overview.gif?raw=true)

See [getting started](http://www.mbtest.org/docs/gettingStarted) guide for more information.

## Install and Run

[![NPM version](https://badge.fury.io/js/mountebank.png)](http://badge.fury.io/js/mountebank)

Install:

    npm install -g mountebank

The npm install requires at least node 0.10.  Billions of other install options are
[also available](http://www.mbtest.org/docs/install) with no platform dependencies.

Run:

    mb

## Learn More

After installing and running, view the docs in your browser at http://localhost:2525, or visit the
[public site](http://www.mbtest.org/).

## Goals

mountebank has the following goals:

* Trivial to get started
    * mountebank is easy to install, without any platform dependencies.  mountebank aims for fun and comprehensive
     documentation with lots of examples, and a nice UI that lets you explore the API interactively.
* A platform, not just a tool
    * mountebank aims to be fully cross-platform, with native language bindings.  Servers are extensible through scripting.
* Powerful
    * mountebank is the only open source stubbing tool that is non-modal and multi-protocol.  Commercial
    "service virtualization" solutions exist, but their licensed platforms make it hard to move the tests
    closer to development and can even require a specialized IDE.  mountebank provides service virtualization free
    of charge without any platform constraints.

Not all of mountebank's goals are currently implemented, but fear not, for he has a team of top-notch open
source developers, and they are legion.

## Support

Visit the [Google group](https://groups.google.com/forum/#!forum/mountebank-discuss)
for any support questions.  Don't be shy!

## Building

[![Coverage Status](https://coveralls.io/repos/bbyars/mountebank/badge.png?branch=master)](https://coveralls.io/r/bbyars/mountebank?branch=master)
[![Codacy Badge](https://www.codacy.com/project/badge/c030a6aebe274e21b4ce11a74e01fa12)](https://www.codacy.com/public/brandonbyars/mountebank)

|                       |Ubuntu 12.04 |CentOS 6.7 |OS X Mavericks |Windows Server 2012 |
|-----------------------|:-----------:|:---------:|:-------------:|:------------------:|
|npm (node v5.0)        | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | (not tested) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build status](https://ci.appveyor.com/api/projects/status/acfhg44px95s4pk5?svg=true)](https://ci.appveyor.com/project/bbyars/mountebank) |
|npm (node v4.2)        | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | (not tested) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build status](https://ci.appveyor.com/api/projects/status/acfhg44px95s4pk5?svg=true)](https://ci.appveyor.com/project/bbyars/mountebank) |
|npm (node v4.0)        | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | (not tested) | (not tested) | (not tested) |
|npm (node v0.12        | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | (not tested) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build status](https://ci.appveyor.com/api/projects/status/acfhg44px95s4pk5?svg=true)](https://ci.appveyor.com/project/bbyars/mountebank) |
|npm (node v0.10        | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | (not tested) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build status](https://ci.appveyor.com/api/projects/status/acfhg44px95s4pk5?svg=true)](https://ci.appveyor.com/project/bbyars/mountebank) |
|OS package             | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | N/A |
|Self-contained archive | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) | [![Build Status](https://travis-ci.org/bbyars/mountebank.png)](https://travis-ci.org/bbyars/mountebank) |

`./build` should do the trick on Mac and Linux, and `build.bat` on Windows, assuming you have at least node 0.10.
If not, yell at me.

There are some tests that require network access (`grunt airplane` ignores them in case that offends your
moral sensibilities).  A few of these tests verify the correct behavior under DNS failures.  If your ISP
is kind enough to hijack the NXDOMAIN DNS response in an attempt to allow you to conveniently peruse their
advertising page, those tests will fail.  I suggest that, under such circumstances, you talk to your ISP
and let them know that their policies are causing mountebank tests to fail.

## Contributing

Contributions are welcome!
Some tips for contributing are in the contributing link that spins up when you run mb.
I have a liberal policy accepting pull requests - I'd rather you sent them even if you can't figure out
how to get the build working, etc.  I'm also available via Skype or something similar to help you get started.
Feel free to reach me at brandon.byars@gmail.com.
