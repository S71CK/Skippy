# Skippy

# Version: 0.9
#
# - Current SSL/TLS tests: 
#   Currently Validates: Heartbleed, Logjam, CRIME,POODLE, DROWN, Weak Cipher Suites enabled, NULL ciphers, MD5 signed certificates, 
#   secure renegotiation checks, and self-signed certificate checks.
#
# Requires: 
# - sslscan, SSLv2 enablement to test for stuff like DROWN, etc. SSLv2 is disabled on most decent
#            modern operating systems, so make sure it's enabled to get the most out of this script.
#
# Known Issues Being Worked On: 56 bit detection.

# This script runs sslcan once, stores the results to a log file and
# analyzes that file for all the different tests. Afterwards, it removes the log file.
# Feel free to modify comment out the "rm $LOGFILE" if you need  to observe the log file.
# An error file is also created and stored in the home directory if anything goes wrong.

