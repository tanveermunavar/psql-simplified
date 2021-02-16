# psqlSimplified

Description : script to run from a psql session

script deployment location `touch ~/.psqlrc`

usage : `postgres=> :vacuum_queries`

hint : ": + double tab will list all the custom scripts alias"

```
postgres=> :con_statn
         now
---------------------
 2021-02-16 17:06:19
(1 row)

Time: 1.489 ms
 state  | count
--------+-------
 idle   |     9
 [null] |     4
 active |     2
(3 rows)

Time: 5.719 ms
    datname    | client_addr |    usename    | state  | count
---------------+-------------+---------------+--------+-------
 demodb        | 10.19.2.10  | dwh           | idle   |     6
 [null]        | [null]      | [null]        | [null] |     4
 rdsadmin      | 127.0.0.1   | rdsadmin      | idle   |     3
 postgres      | 10.60.2.131 | tanveerm      | active |     1
 dwh_db        | 10.19.2.10  | dwh           | idle   |     1
(5 rows)

Time: 3.862 ms
    datname    |    usename    | wait_event_type |    wait_event    | count
---------------+---------------+-----------------+------------------+-------
 demodb        | dwh           | Client          | ClientRead       |     6
 rdsadmin      | rdsadmin      | Client          | ClientRead       |     3
 [null]        | [null]        | Activity        | RecoveryWalAll   |     1
 postgres      | tanveerm      | [null]          | [null]           |     1
 [null]        | [null]        | Activity        | WalReceiverMain  |     1
 [null]        | [null]        | Activity        | CheckpointerMain |     1
 dwh_db        | dwh           | Client          | ClientRead       |     1
 [null]        | [null]        | Activity        | BgWriterMain     |     1
(8 rows)

Time: 1.581 ms
 time | datname | usename | client_addr | xact_time | state_time | state | wait_event_type | wait_event | pid | query
------+---------+---------+-------------+-----------+------------+-------+-----------------+------------+-----+-------
(0 rows)

Time: 2.645 ms
postgres=>
```
