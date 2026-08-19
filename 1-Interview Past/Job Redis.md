Redis
Advantage
Redis vs Other Key Value Stores
Redis Support Data Types 

String  String : SET GET
HashMap    Hashes : HMSET HGETALL
List  List lpush/ lrange
Set  RedisSet sadd / smemebers
Ordered Set  SortedSet zadd ZRANGEBYSCORE
Max Element 2^32-1

Is it case sensitive ?
Does it support Atomic Operation

| Topic               | Command       |
| ------------------- | ------------- |
| Cache expiry        | EXPIRE / TTL  |
| Batch operation     | MSET / MGET   |
| Atomic counter      | INCR          |
| Distributed lock    | SET NX EX     |
| Queue               | LPUSH / RPUSH |
| Leaderboard         | ZADD          |
| Production scanning | SCAN          |
| Performance         | PIPELINE      |
