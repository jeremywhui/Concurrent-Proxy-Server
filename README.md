# Concurrent Proxy Server

Makefile	- For building proxy

README.md	- This file

## Proxy source files

proxy.{c,h}	- Primary proxy code

csapp.{c,h}	- Wrapper and helper functions from the CS:APP text

The program is an upgraded version of the sequential proxy, a concurrent
proxy. The program performs the same original steps as the sequential
proxy, but now instead uses each child process to handle each connection
in the process version, or uses each thread to handle each connection
in the thread version. The proxy also now suupports HTTPS tunneling
via the connect method, and logs all entries in the file proxy.log. The
program can be run by first running `make clean`, `make`, then finally
`./proxy portNumber`, `./proxy -p portNumber`, or `./proxy --process portNumber`
for the process version, or `./proxy -t portNumber` or `./proxy --thread portNumber`
for the thread version.
