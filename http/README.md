# HTTP

## Headers max size

The HTTP RFC does not specify a maximum header length, but in reality most servers and many firewalls support a limited length. In some instances this depends on the header itself but in many cases there's a check against the length of all header values, so one must make sure not to pass too many informations via headers.

> And in practice the 8000 bytes limit is usually found on headers also.

[source](https://security.stackexchange.com/a/113365/155108)

A server that receives an exceedingly large header will reject the request issuing a 400.

## HTTP requests

### Preflight requests

Preflight requests enable the browser to ask for the server’s permission before making requests with certain HTTP methods and headers. This permissions model puts the server in charge of how cross-origin requests behave. [source](https://livebook.manning.com/book/cors-in-action/chapter-5/7)
