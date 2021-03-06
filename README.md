
PanicKit is a collection of tools for letting panic trigger and panic receiver
apps safely and easily connect to each other. The trigger apps are the part
that the user will actual engage when in a panic situation. The receiver apps
receive the trigger signal from the trigger apps when the user has initiated
the panic response. The connections between trigger and receiver can be
strictly enforced based on `packageName` and APK signing key.

https://dev.guardianproject.info/projects/panic/wiki


License
-------

This library is licensed under the LGPLv2.1.  We believe this is compatible
with all reasonable uses, including proprietary software, but let us know if
it provides difficulties for you.  For more info on how that works with Java,
see:

https://www.gnu.org/licenses/lgpl-java.en.html


Reproducible Build
------------------

To build your own jars from source and recreate the exact same files,
bit-for-bit, as the official releases, `strip-nondeterminism` is
required to set the timestamps in the ZIP headers to match the
timestamp in the git release tag (e.g. 0.2).

To install it on Debian/jessie, Ubuntu/vivid/15.04 or newer, just do:

    sudo apt-get install dh-strip-nondeterminism

For Ubuntu/trusty/14.04, add our PPA:

    curl 'https://pgp.mit.edu/pks/lookup?op=get&search=0x6B80A84207B30AC9DEE235FEF50EADDD2234F563' | sudo apt-key add -
    sudo add-apt-repository ppa:guardianproject/ppa
    sudo apt-get update
    sudo apt-get install dh-strip-nondeterminism

