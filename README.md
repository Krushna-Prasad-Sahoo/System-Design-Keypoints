# System-Design-Keypoints

Definition: Systems design is the process of defining elements of a system like modules, architecture, components and their interfaces and data for a system based on the specified requirements.

System Design Concepts & Components :-

1. Scaling
Large enterprises have large amounts of data. With increasing amounts of data the system should also grow to manage it effectively. This process of growing or shrinking of the system to handle data is called scaling.

Scaling of any system can be achieved by two ways.

Vertical Scaling : Vertical scaling means upgrading the hardware/software of the existing system. Adding more power to it more RAM, CPU’s and HDD. But with vertical scaling there is always a limit a max beyond which it cannot go higher.
Horizontal Scaling : Horizontal scaling means adding multiple additional systems to improve the performance. Typically we might use several low end commodity hardware to save the cost.
These are some differences between them.
Horizontal Scaling


2. Load Balancing
Load balancer helps distribute incoming traffic across servers or databases. There are 2 types of load balancers hardware and software. Hardware load balancers are generally expensive but very effective. 

You can use multiple load balancers to avoid single point of failure. They can be in active-active mode or active-passive mode.

Following algorithms are largely used for load balancing purpose.

Round Robin 
Least Loaded
Session Based
Hashing

3. Caching
Caching is a concept where data is stored in fast memory for quick access. The cache is generally a temporary storage like RAM since it is faster than reading the data from HDD or a database.

There is a famous 80:20 rule which states that 20% of the data is accessed almost 80% of the time. So generally we try to keep that 20% data in the cache.

Cache Invalidation 

-Write-through cache: Data is written in cache and database at the same time.
-Write-around cache: Data is written in database only. Cache is marked as invalid. It is written later in cache.
-Write-back cache: Data is written in cache only. It is written later in db.


4. Consistent Hashing
Consistent hashing is one of the techniques used to bake in scalability into the storage architecture of your system. 

In a distributed system, consistent hashing helps in solving following scenarios:

To Provide elastic scaling (a term used to describe synamic adding/removing of servers based on usage load) for cache servers.
Scale out a set of storage nodes like NoSQL databases.


5. Storage
Object Store

Object store or object-based storage is a storage architecture which manages data as objects unlike your regular hard disks which manages it as files in a file hierarchy system.

RAID

Redundant array of independent disks (RAID) is a way of storing the same data on multiple hard disks or solid state drives to protect it in case of failures. There is a RAID controller which handles all the operations and is responsible for improving performance while writing and protecting the data on multiple devices.

RAID Levels

RAID levels are nothing but different configurations. There are 6 standard levels of RAID from RAID 0 to RAID 5, then there are several combined RAID levels like RAID 10 and many non standard RAID levels which companies have developed for their own use. For the purpose of this section we will go through RAID 0 to RAID 5 and a combination RAID 10. These are good to know topics for design interview. You can ignore the other RAID levels safely.

RAID 0 – Striping
RAID 1 – Mirroring
RAID 2 – Bit-level striping with dedicated Hamming-code parity 
RAID 3 – Byte-level striping with a single parity disk
RAID 4 – Block-level striping with a single parity disk 
RAID 5 – Striping with distributed parity
RAID 6 – Striping with double parity
RAID 10 – Combining striping and mirroring




