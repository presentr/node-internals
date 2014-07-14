##  The Node.js core

```
 +------------------------------------------------+
 |                     node.cc                    | <- the main node juju
 +------------------------------------------------+
 |      v8 / JS libs     |       c++ addons       |
 +------------------------------------------------+
 | libuv | c-ares | openssl | zlib | http_parser  | <- c++ dependencies
 +------------------------------------------------+
     ^ the secret sauce

```

note:
  - node.cc is the node API and it's glue
  - v8 is the JS compilers
  - c++ addons is a can of worms we'll leave alone
  - libuv is the secret sauce that handles event loops and async IO
  - All methods in the dns module use C-Ares except for dns.lookup which uses getaddrinfo(3) in a thread pool.
  