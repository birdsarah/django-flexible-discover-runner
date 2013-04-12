django-flexible-discover-runner
===============================

A test suite runner combining default django behavior with the smart test discovery of djano-discover-runner.

With snippets taken from https://gist.github.com/carljm/1450104 and
https://github.com/jezdez/django-discover-runner

Installation
============
Add test_runner.py to your project's home directory

In settings.py add TEST_RUNNER = 'test_runner.DiscoveryRunner'

(Or put test_runner module wherever you feel like it and point TEST_RUNNER 
setting to the module's DiscoveryRunner class)

Usage
=====
Running './manage.py test' will run all tests including those "smart found"
in applications (default django behavior plus default django-test-runner
behavior).

Using './manage.py test projectapps' will run all the tests in your source
folder but not all installed apps (the default behavior of
django-discover-runner)

Specifying an app name like './manage.py app', will just run the tests
"smart found" for that app.
** You cannot specify multiple apps to run tests from (just one or all). **

Or you can supply a series of test files / test names with dotted names
e.g. ./manage.py app1.tests.test_file app2.tests.file.TestClass.test_method

License
=======
Copyright (c) 2013, Sarah Bird
Copyright (c) 2011-2013, The django-discover-runner authors (Carl J. Meyer, 
Jannis Leidel, Omer Katz, Russ Ferriday, Rafal Stozek)
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are
met:

    * Redistributions of source code must retain the above copyright
      notice, this list of conditions and the following disclaimer.
    * Redistributions in binary form must reproduce the above
      copyright notice, this list of conditions and the following
      disclaimer in the documentation and/or other materials provided
      with the distribution.
    * None of the authors names may be used to endorse or promote products
      derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
