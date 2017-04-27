## MemSQL Pipeline, Apache Kafka

```
memsql> select * from samples order by bytes desc lmit 20;
+----------------+-----------------+-----------------+--------+--------+-------+---------+---------+----------+--------+---------------------+
| device         | src             | dst             | srcASN | dstASN | proto | srcPort | dstPort | tcpFlags | bytes  | datetime            |
+----------------+-----------------+-----------------+--------+--------+-------+---------+---------+----------+--------+---------------------+
| 192.129.230.0  | 87.11.81.121    | 61.231.215.18   | 131780 |  21773 |     6 |      80 |   64670 | 0x10     | 342000 | 2017-04-27 22:05:55 |
| 52.20.79.116   | 87.11.81.100    | 216.38.140.154  |  41171 |   7994 |     6 |     443 |   26798 | 0x18     | 283364 | 2017-04-27 22:06:00 |
| 52.20.79.116   | 192.229.211.70  | 50.240.197.150  |  41171 |  33651 |     6 |      80 |   23397 | 0x10     | 216000 | 2017-04-27 22:05:55 |
| 108.161.249.16 | 152.125.33.113  | 74.121.78.10    |  13768 |   9551 |     6 |      80 |   49217 | 0x18     | 196500 | 2017-04-27 22:05:59 |
| 192.229.130.0  | 87.21.81.254    | 94.56.54.135    | 132780 |  21773 |     6 |      80 |   52853 | 0x18     | 165000 | 2017-04-27 22:05:55 |
| 108.161.229.96 | 93.184.215.169  | 152.157.32.200  |  12768 |  11430 |     6 |     443 |   50488 | 0x18     |  86400 | 2017-04-27 22:06:01 |
| 52.22.49.106   | 122.229.210.189 | 99.31.208.183   |  22171 |   8018 |     6 |     443 |   33059 | 0x18     |  73500 | 2017-04-27 22:05:55 |
| 52.22.49.126   | 81.21.81.131    | 66.215.169.120  |  22171 |  20115 |     6 |      80 |   57468 | 0x10     |  66000 | 2017-04-27 22:05:59 |
| 108.160.149.96 | 94.184.215.151  | 123.90.233.120  |  16768 |  14476 |     6 |      80 |   63905 | 0x18     |  65540 | 2017-04-27 22:05:57 |
| 52.22.79.116   | 162.129.210.181 | 60.180.253.156  |  21271 |  31651 |     6 |     443 |   59652 | 0x18     |  64805 | 2017-04-27 22:06:00 |
| 108.161.149.90 | 93.184.215.169  | 80.96.58.146    |  13868 |  22394 |     6 |     443 |    1151 | 0x18     |  59976 | 2017-04-27 22:05:54 |
| 102.232.179.20 | 111.18.232.131  | 121.62.44.149   |  24658 |   4771 |     6 |      80 |   61076 | 0x10     |  59532 | 2017-04-27 22:05:54 |
| 102.232.179.20 | 192.129.145.6   | 110.49.221.232  |  24658 |   4804 |     6 |     443 |   50002 | 0x10     |  58500 | 2017-04-27 22:05:55 |
| 102.232.179.20 | 192.129.232.112 | 124.132.217.101 |  24658 |  43124 |     6 |     443 |   37686 | 0x10     |  57000 | 2017-04-27 22:06:00 |
| 192.229.230.0  | 87.11.81.253    | 219.147.144.22  | 132380 |   2900 |     6 |      80 |   25202 | 0x18     |  56120 | 2017-04-27 22:05:58 |
| 192.129.130.0  | 87.21.11.200    | 180.239.187.151 | 132380 |   8151 |     6 |     443 |   55062 | 0x18     |  52220 | 2017-04-27 22:05:59 |
| 52.12.79.126   | 87.21.11.254    | 64.30.125.221   |  21071 |  14051 |     6 |      80 |   57072 | 0x10     |  51000 | 2017-04-27 22:05:54 |
| 192.229.110.1  | 150.195.33.40   | 98.171.170.51   | 132980 |  28773 |     6 |      80 |   53270 | 0x18     |  51000 | 2017-04-27 22:05:57 |
| 192.229.110.1  | 87.21.81.254    | 68.96.162.21    | 132980 |  28773 |     6 |      80 |   46727 | 0x18     |  49500 | 2017-04-27 22:06:01 |
| 52.22.59.110   | 192.129.210.181 | 151.203.130.228 |  21271 |  12452 |     6 |      80 |   43720 | 0x18     |  49500 | 2017-04-27 22:05:55 |
+----------------+-----------------+-----------------+--------+--------+-------+---------+---------+----------+--------+---------------------+
20 rows in set (0.06 sec)
```