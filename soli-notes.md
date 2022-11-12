[读懂Redis源码，我总结了这7点心得](http://kaito-kidd.com/2021/09/23/read-redis-source-code/)
## redis-benchmark压测
```sh
cd /usr/local/projs/redis/src && ./redis-benchmark -h
./redis-benchmark -t set -n 1000000 -r 100000000
47496.91 requests per second
./redis-benchmark -t set -n 1000000 -r 100000000 -P 16
291290.41 requests per second
```
查看redis的快照文件dump.rdb:
rdb -c memory dump.rdb > dump_rdb.csv
其中：size_in_bytes 内存的大小，由此可以查询内存最高的key



