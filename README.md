# Designing-Data-Intensive-Applications
Designing Data-Intensive Applications Reading Notes
```Try to read and understand as much as possible in one hour per day and keep straignt to 14 das. ```
As usual, there are reading notes (Aaron think it's important, because ABC). 
System Design is all about handle trade-off (Same as our day to day life). Feel free to share you thoughts or experiences.
## Contents 

## I. Foundations of Data Systems.
### 1. Reliable, Scalable, and Maintainable Applications
- [ ] Thinking About Data Systems
- [ ] Reliability
    * Hardware Faults
    * Software Errors
    * Human Errors
    * How Important Is Reliability?
- [ ] Scalability
    *
- [ ] Maintainability
- [ ] Summary
### 2. Data Models and Query Languages
- [ ] Relation Model Versus Document Model
    * The Birth of NoSQL
    * The Object-Relational Mismatch
    * Many-to-One and Many-to-Many Relationships
    * Are Document Databases Repeating History?
    * Relational Versus Document Databases Today
- [ ] Query Languages for Data
    * Declarative Queries on the Web
    * MapReduce Querying
- [ ] Graph-Like Data Models
    * Property Graphs
    * The Cypher Query Language
    * Graph Queries in SQL
    * Triple-Stores and SPARQL
    * The Foundation: Datalog
- [ ] Summary
### 3. Storage and Retrieval
- [ ] Data Structures That Power Your Database
    * Hash Indexes
    * SSTables and LSM-Trees
    * B-Trees
    * Comparing B-Tress and LSM-Trees
    * Other Indexing Structures
- [ ] Transaction Processing or Analytics?
    * Data Warehousing
    * Stars and Snowflakes: Schemas for Analytics
- [ ] Column-Oriented Storage
    * Column Compression
    * Sort Order in Column Storage
    * Writing to Column-Oriented Storage
    * Aggregation: Data Cubes and Materialized Views 
- [ ] Summary
### 4. Encoding and Evolution 
- [ ] Formats for Encoding Data
    * Language-Specific Formats
    * JSON, XML, and Binary Variants
    * Thrift and Protocol Buffers
    * Avro
    * The Merits of Schemas
- [ ] Modes of Dataflow
    * Dataflow Through Databases
    * Dataflow Through Services: REST and RPC
    * Message-Passing Dataflow
- [ ] Summary
## II. Distributed Data
### 5. Replication
- [ ] Leaders and Followers
    * Synchronous Versus Asynchronous Replication
    * Setting Up New Followers
    * Handling Node Outages
    * Implementation of Replication Logs
- [ ] Problems with Replication Lag
    * Reading Your Own Writes
    * Monotonic Reads
    * Consistent Prefix Reads
    * Solutions for Replication Lag
- [ ] Multi-Leader Replication
    * Use Cases for Multi-Leader Replication
    * Handling Write Conflicts 
    * Multi-Leader Replication Topologies
- [ ] Leaderless Replication
    * Writing to the Database When a Node Is Down
    * Limitations of Quorum Consistency
    * Sloppy Quorums and Hinted Handoff
    * Detecting Concurrent Writes
- [ ] Summary
### 6. Partitioning
- [ ] Partitioning and Replication
- [ ] Partitioning of Key-Value Data
    * Partitioning by Key Range
    * Partitioning by Hash of Key
    * Skewed Workloads and Relieving Hot Spots
- [ ] Partitioning and Secondary Indexes
    * Partitioning Secondary Indexes by Document
    * Partitioning Secondary Indexes by Term
- [ ] Summary
### 7. Transactions
- [ ] The Slippery Concept of a Transaction
    * The Meaning of ACID
    * Single-Object and Multi-Object Operations
- [ ] Weak Isolation Levels
    * Read Committed
    * Snapshot Isolation and Repeatable Read
    * Preventing Lost Updates
    * Write Skew
- [ ] Summary 
### 8. The Trouble with Distributed Systems
- [ ] Faults and Partial Failures
    * Cloud Computing and Supercomputing
- [ ] Unreliable Networks
    * Network Faults in Practice
    * Detecting Faults
    * Timeouts and Unbounded Delays
    * Synchronous Versus Asynchronous Networks
- [ ] Unreliable Clocks
    * Monotonic Versus Time-of-Day Clocks
    * Clock Synchronization and Accuracy
    * Relying on Synchronized Clocks
    * Process Pauses
- [ ] Knowledge, Truth, and Lies
    * The Truth Is Defined by the Majority
    * Byzantine Faults
    * System Model and Reality
- [ ] Summary
### 9. Consistency and Consensus
- [ ]
    *
    *
    *
- [ ]
    *
    *
    *
- [ ] Summary
## III. Derived Data
### 10. Batch Processing with Unix Tools
- [ ]
    *
    *
    *
- [ ]
    *
    *
    *
- [ ] Summary
### 11. Stream Processing
- [ ]
    *
    *
    *
- [ ]
    *
    *
    *
- [ ] Summary
### 12. The Future of Data System
- [ ]
    *
    *
    *
- [ ]
    *
    *
    *    
- [ ] Summary

