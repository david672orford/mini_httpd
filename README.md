This is a very simple HTTP server. It has the following features:

* Serves static files
* Serves CGI scripts (identified by .cgi extension)
* Infers MIME type from extension
* If a directory is requested, looks for index.html or index.cgi
* Does not automatically create directory listings
* Does not support authentication
* Does not support persistent connections

In /etc/inetd.conf:

http stream tcp nowait nobody /usr/local/sbin/mini_httpd mini_httpd /var/www

