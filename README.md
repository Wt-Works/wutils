WUtils {#mainpage}
======

WUtils is a set of cross-platform C++11 utility classes for the [Wt] C++ web framework.

This library is developed following modern practices:

* Test Driven Development; comes with a full UT suite.
* Continuous Integration; each commit is built and tested on: Mac OS X 10.9, Linux XXX, FreeBSD YYY, [Travis CI].

Contents
--------

* WU::UrlRouter: A regex-based URL router/dispatcher for Wt inspired by the smart [Django URLconf].
* `test` directory: extensive Unit Tests.

Requirements
------------

Any platform with a decent C++11 compiler.

* g++: at least g++ 4.9 (unfortunately g++ 4.8 has a [non-working std::regex][g++ broken regex])
* clang++: 3.4

Build
-----

For the time being it is an include-only library, no need to compile. Just include `urlrouter.hpp` in your project.

Testing
-------

For running the UT, you need Google Mock, Google Test, Wt built with the UT library and Boost.

Under the directory `scripts` there are script to fetch and build Google Mock and Wt.

Known issues
------------

* This is innocuous and has been fixed in wt after the release.

    test-urlrouter.cpp:85:16: warning: deleting object of polymorphic class type Wt::Test::WTestEnvironment which has non-virtual destructor might cause undefined behaviour [-Wdelete-non-virtual-dtor]

License
-------

WUtils is released under the the BSD 2-clause license (see file LICENSE.txt).

Pull requests appreciated.

[Wt]: http://www.webtoolkit.eu/wt
[Django URLconf]: https://docs.djangoproject.com/en/dev/topics/http/urls
[Travis CI]: https://travis-ci.org/marco-m/wutils
[g++ broken regex]: http://gcc.gnu.org/bugzilla/show_bug.cgi?id=53631
