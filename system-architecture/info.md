* `CAP theorem` - it is impossible for a distributed data store to simultaneously provide more than two guarantees (C or A): 
    * `Consistency`: Every read receives the most recent write or an error
    * `Availability`: Every request receives a (non-error) response, without the guarantee that it contains the most recent write
    * `Partition tolerance`: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes
* `PACELC theorem` - in case of network partitioning (P) one has to choose between availability (A) and consistency (C) (as per the CAP theorem), 
but else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C).

