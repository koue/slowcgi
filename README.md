#### FreeBSD port of OpenBSD slowcgi ####

slowcgi is a server which implements the FastCGI Protocol to execute CGI
scripts. FastCGI was designed to overcome the CGI protocol's scalability
and resource sharing limitations. While CGI scripts need to be forked for
every request, FastCGI scripts can be kept running and handle many HTTP
requests.

slowcgi is a simple server that translates FastCGI requests to the CGI
protocol. It executes the requested CGI script and translates its output
back to the FastCGI protocol.

http://cvsweb.openbsd.org/cgi-bin/cvsweb/src/usr.sbin/slowcgi/
