# redis

A Redis client for zepto.
It is stable and maintained, but not really battle-tested.

# Installation

```
zeps install hellerve/redis
```

# Usage

Most commands of redis are supported. The naming
schme follows the template of `redis:the-command-in-lower-case`.

```clojure
(load "redis/redis")

(define redis-client (redis:new)) ; defaults to a connection to 127.0.0.1:6379
; you can also open a connection to a specific IP/Port pair
(define redis-client (redis:new :ip "192.168.1.2"
                                   :port 6331))

(redis:ping redis-client) ; "PONG"
(redis:dbsize redis-client) ; some integer denoting the current db size
(redis:set redis-client "zepto" "myvalue") ; sets "zepto" to "myvalue"
(redis:get redis-client "zepto") ; "myvalue"
```

<hr/>

Have fun!
