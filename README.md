# System-Design-Notes
System design topics and concepts and thieir study links
# Most important: [https://github.com/donnemartin/system-design-primer/blob/master/README.md]
Concepts:

1. Consistent Hashing

   [Cassandra Consistent Hasing with explanation of read and write opertions with replication](https://www.datastax.com/blog/2019/02/distributed-database-things-know-consistent-hashing)
   
   [Consistent Hashing explanation with advantages, high level article](https://dzone.com/articles/simple-magic-consistent)
   
   [Consistent Hashing with code example](http://michaelnielsen.org/blog/consistent-hashing/) 
   
   [Artile with most detailed notes on when nodes get added or removed](https://www.ably.io/blog/implementing-efficient-consistent-hashing/)
   
   [Consistent Hasing: Algorithimin tradeoffs, code level exlpanation](https://medium.com/@dgryski/consistent-hashing-algorithmic-tradeoffs-ef6b8e2fcae8)

2. Distributed Transactions:
   DTs using Sagas in Micro-Services architecture: https://www.youtube.com/watch?v=YPbGW3Fnmbc
   
   Idea is that first part is executed consitently and second dependent part is executed eventually. for example,  Support transfer 
   of amount from acc A to acc B. then service handling transfer will debit the amount from A and then create a message in queue for     
   crediting to B acc which will eventually get executed. 
   
   Article on intro to both approaches: https://developers.redhat.com/blog/2018/10/01/patterns-for-distributed-transactions-within-a-microservices-architecture/

3. Distributed Locks


4. Cluster management



5. Resiliency


6. CAP theorem


7. Bloom Filters
   Are probabilistic data structure which can tell for sure that item do not belong to a set (No false negatives) and tell item belong to the given set with some certainity, if item is present in the set(false positives are present but can be minimized). It is extremelly useful as it saves a lot of memory. For introduction to subject follow following link: https://www.youtube.com/watch?v=bEmBh1HtYrw .  The basic idea is to use k hash functions to generate a position to set a bit in an array of size n. where n is always > k. Then go for this video, this certainly makes things much clear after first video: https://www.youtube.com/watch?v=zYlxP7F3Z3c


8. Rate Limiting (Leaky Bucket and Token Bucket algorithms), Load Shedders, 
   [Youtube](https://www.youtube.com/watch?v=mhUQe4BKZXs)
   [Design Distributed Rate Limiter](https://www.ably.io/blog/distributed-rate-limiting-scale-your-platform/)

9. Data Replication

10. Types of data and their mapping to different kinds of databases/stores

11. Caching: Types, places where data can be cached and cache selection

12. Map-Reduce 

13. DNS Servers

14. CDNs

15. Public Subscribe Queues
