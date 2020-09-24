# Part II. Distributed Data

## Quick Peak

### Chapter 5. Replication （复制）
-[ ] Leaders and Followers
    * Synchronous Versus Asynchronous Replication
    * Setting Up New Followers
    * Handling Node Outages
        * Follower Failure: Catch-up Recovery
        * Leader Failure: Failover
    * Implementation of Replication Logs
        * Statement-based replication
        * Write-ahead log (WAL) shipping here
        * Logic (ROW-BASED) Log Replication
        * Trigger-Based Replication
        
-[ ] Problems with Replication Lag -- 复制延迟问题
    * Reading Your Own Writes (读自己写的)
    * Montonic Reads (单调读)
    * Consistent Prefix Reads (一致前缀读)
    * Solutions for Replication Lag
    
-[X] Multi-Leader Replication -- 多主复制 （多主多活） 
    * Use Cases for Multi-Leader Replication
        * Multi-DataCenter Operation （运维多个数据中心）
        * Clients With Offline Operation （离线客户端操作）
        * Collaborative Editing （协同编辑）这里有个System design
    * Handling Write Conflicts （处理写入冲突，重点）
        * Synchronous vs Asynchronous Conflict Detection (同步与异步冲突检测)
        * Conflict Avoidance (避免冲突)
        * Converging Toward a Consistent State (收敛至一致的状态)
        * Custom Conflict Resolution Logic (自定义冲突解决逻辑) (题外话)
        * What is a Conflict? (什么是冲突)
    * Multi-Leader Replication Topologies (多主复制拓扑)
    
-[X] Leaderless Replication (无主复制)
    * Writing to the Database When a Node Is Down (当节点故障时写入数据库)
        * Read Repair And Anti-Entropy (读修复和反熵)
        * Quorums For Reading and Writing (读写的法定人数)
    * Limitations of Quorum Consistency (仲裁一致性的局限性)
        * Monitoring Staleness (监控陈旧度)
    * Sloppy Quorums and Hinted Handoff (松散法定人数与带提示的接力)
        * Multi-datacenter Operation (运维多个数据中心-无主复制)
    * Detecting Concurrent Writes （检测兵法写入）
        * Last Write Wins(Discarding concurrent Writes) (最后写入胜利 - 丢弃并发写入)
        * The "Happens-Before" Relationship and Concurrency
        * Capturing the Happens-Before Relationship
        * Merging Concurrently Written Values
        * Version Vectors      
-[ ] Summary

### Chapter 6. Partitioning （分区）
-[X] Partitioning and Replication (分区与复制)
-[ ] Partitioning of Key-Value Data (键值数据的分区)
    * Partitioning by Key Range (根据键的范围分区)
    * Partitioning by Hash of Key (根据键的散列分区)
    * Skewed Workloads and Relieving Hot Spots (负载倾斜与消除热点)
-[ ] Partitioning and Secondary Indexes (分片与次级索引)
    * Partitioning Secondary Indexes by Document (按文档的二级索引)
    * Partitioning Secondary Indexes By Term ()
-[ ] Rebalancing Partitions ()
    * Strategies for Rebalancing ()
        * HOW NOT TO DO IT: HASH MOD N ()
        * FIXED NUMBER OF PARTITIONS ()
        * DYNAMIC PARTITIONING 
        * PARTITIONING PROPORTIONALLY TO NODES
    * Operations: Automatic or Manual Rebalancing
-[ ] Request Routing
    * Parallel Query Execution
-[ ] Summary

### Chapter 7. Transactions （事务）
-[ ] The Slippery Concept of a Transaction (事务的棘手概念)
    * The Meaning of ACID (ACID的含义)
        ATOMICITY (原子性)
        CONSISTENCY (一致性)
        ISOLATION
        DURABILITY
    * Single-Object and Multi-Object Operations
        SINGLE-OBJECT WRITES
        THE NEED FOR MULTI-OBJECT TRANSACTIONS
        HANDLING ERRORS AND ABORTS
-[ ] Weak Isolation Levels
    * Read Committed
        NO DIRTY READS
        NO DIRTY WRITES
        IMPLEMENTING READ COMMITTED
    * Snapshot Isolation and Repeatable Read
        IMPLEMENTING SNAPSHOT ISOLATION
        VISIBILITY RULES FOR OBSERVING A CONSISTENT SNAPSHOT
        INDEXES AND SNAPSHOT ISOLATION
        REPEATABLE READ AND NAMING CONFUSION
    * Preventing Lost Updates
        ATOMIC WRITE OPERATIONS
        EXPLICIT LOCKING
        AUTOMATICALLY DETECTING LOST UPDATES
        COMPARE-AND-SET
        CONFLICT RESOLUTION AND REPLICATION
    * Write Skew and Phantoms
        CHARACTERIZING WRITE SKEW
        MORE EXAMPLES OF WRITE SKEW
        PHANTOMS CAUSING WRITE SKEW
        MATERIALIZING CONFLICTS
-[ ] Serializability
    * Actual Serial Execution
        ENCAPSULATING TRANSACTIONS IN STORED PROCEDURES
        PROS AND CONS OF STORED PROCEDURES
        PARTITIONING
        SUMMARY OF SERIAL EXECUTION
    * Two-Phase Locking (2PL)
        IMPLEMENTATION OF TWO-PHASE LOCKING
        PERFORMANCE OF TWO-PHASE LOCKING
        PREDICATE LOCKS
        INDEX-RANGE LOCKS
    * Serializable Sanpshot Isolation (SSI)
        PESSIMISTIC VERSUS OPTIMISTIC CONCURRENCY CONTROL
        DECISIONS BASED ON AN OUTDATED PREMISE
        DETECTING STALE MVCC READS
        DETECTING WRITES THAT AFFECT PRIOR READS
        PERFORMANCE OF SERIALIZABLE SNAPSHOT ISOLATION
-[ ] Summary

### Chapter 8. The Trouble with Distributed Systems （分布式系统的麻烦）

### Chapter 9. Consistency and Consensus （一致性与共识）
