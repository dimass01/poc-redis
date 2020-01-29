Poc Redis
=========

A Symfony project created on June 20, 2017, 2:22 pm.

**About redis**

Redis is an in-memory key-value cache and data store (also referred as NoSQL database). It can persist it's state to disk which helps recover data after restart unlike memcached. Since it stores data in memory, size of data cannot exceed the total memory space on the system. Nowadays, many prefer redis over memcached and MongoDB especially for performance reasons. It can store strings, hashes, lists, sets, sorted sets and more whereas memcached only supports strings.

    - String : Simple strings.

    - List : Similar to a single dimensional array in PHP which holds ordered collection. You can push, pop, shift and unshift.

    - Hash : Used for objects.

    - Set : Similar to list but it has no order and each element appears only once.

    - Sorted Set : Similar to set but values stored in set and ordered/ranked. Each member is associated with score and used to order the set from the smallest score to the largest.


What we will do

    - Set persistent key : http://192.168.50.10:8081/app_dev.php/redis/set?key=a&value=1

    - Set non-persistent key : http://192.168.50.10:8081/app_dev.php/redis/set?key=a&value=1&ttl=10

    - Get key's value : http://192.168.50.10:8081/app_dev.php/redis/get?key=a

    - Get key's TTL : http://192.168.50.10:8081/app_dev.php/redis/ttl?key=a

    - Make key persistent : http://192.168.50.10:8081/app_dev.php/redis/persist?key=a

    - Delete key : http://192.168.50.10:8081/app_dev.php/redis/delete?key=a

    - Expire key (TTL optional) : http://192.168.50.10:8081/app_dev.php/redis/expire?key=a&ttl=10