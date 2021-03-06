# Log::Syslog::Native

Provide access to the Native syslog facility on Unix-like systems for Perl 6

## Description

This provides a simple, perhaps naive,interface to the POSIX syslog facility
found on most Unix-like systems.

It should be enough to get you started with simple logging to your system's
log files, though exactly what files those might be and how they are logged
is a function of the system configuration and the exact logging software
that is being used.

This does not provide logging to a remote syslog server, nor does it provide
syslog style logging to platforms that do not provide a ''syslog()'' function
in their standard runtime library.

## Installation

Currently there is no dedicated test to determine whether your platform is
supported, the unit tests will simply fail horribly.

Assuming you have a working perl6 installation you should be able to
install this with *ufo* :

    ufo
    make test
    make install

*ufo* can be installed with *panda* for rakudo:

    panda install ufo

Or you can install directly with "panda":

    # From the source directory
   
    panda install .

    # Remove installation

    panda install Log::Syslog::Native

Other install mechanisms may be become available in the future.

## Support

This should be considered experimental software until such time that
Perl 6 reaches an official release.  However suggestions/patches are
welcomed via github at

   https://github.com/jonathanstowe/Log-Syslog-Native

I'm not able to test on a wide variety of platforms so any help there would be 
appreciated.

Things that I know don't work as of the current release are:

    * The built in sprintf is emulated because no varargs in NativeCall yet 

Help with these is explicitly invited.

## Licence

Please see the LICENCE file in the distribution

(C) Jonathan Stowe 2015
