gerrit-raise-patch: Gerrit Raise Patchset plugin
==================

* Author: rinrinne a.k.a. rin_ne
* Repository: http://github.com/rinrinne/gerrit-raise-patch

[![Build Status](https://travis-ci.org/rinrinne/gerrit-raise-patch.png?branch=master)](https://travis-ci.org/rinrinne/gerrit-raise-patch)

Synopsis
----------------------

This is a Gerrit plugin.

This can raise `patchset-created` event to gerrit event stream.
`Raise Event` button is added to revision view.

This plugin works on Gerrit 2.8 or later.

About Buck
---------------------

[Buck] is a build system now gerrit adopt. If you want to use Buck,
you need to setup it referring [Building with Buck] in gerrit documentation.

[Buck]: http://facebook.github.io/buck/
[Building with Buck]: https://gerrit-documentation.storage.googleapis.com/Documentation/2.8.3/dev-buck.html


Environments
---------------------

* `linux`
  * `java-1.7`
    * `gradle`
    * `buck`

Build
---------------------

* Use `gradle`

To build plugin with maven.

    ./gradlew build

* Use `buck`

To build plugin with buck

    git clone https://gerrit.googlesource.com/gerrit -b v2.8.3
    ln -s $(pwd) gerrit/plugins/raise-patch
    cd gerrit
    buck build plugins/raise-patch:raise-patch

Using another version API
--------------------------

* For `gradle`

Now avaliable for Gerrit 2.8.3 only. If you want to use it on another version of Gerrit, please try the below.

    ./gradlew build -PapiVersion=2.8

* For `buck`

After clone gerrit, you can checkout specified version.

    git checkout -b 2.8 refs/tags/v2.8

*NOTE*: If you use buck, you can build on gerrit master.


History
---------------------

* 1.1
  * Add gradle support
  * Remove maven support

* 1.0
  *  First release

License
---------------------

The Apache Software License, Version 2.0

Copyright
---------------------

Copyright (c) 2014 rinrinne a.k.a. rin_ne
