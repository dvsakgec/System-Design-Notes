
## Contents:

  1. Google Docs: Collaboration () | Storage (secure storage, efficient as google gives lots of space, speedy upload and download) | Access Management
  2. DropBox: Storage (Efficient, speedy upload and download, secure storage) | Access Management (Secure 

## Google Docs:
 Core challenges: Live collaboration, Storage and Access Management
 Google docs collaboration feature can be build using either OT (Operational Transformation) or DIfferential Synchronization ( CRDTs)
 OT Links:
 
    1. [Evailauting CRDTs(Commutative Replicated Datatypes) ](https://hal.inria.fr/file/index/docid/629503/filename/doce63-ahmednacer.pdf)
    2. [Best link:Conflict-Free Replicated Data Types (CRDT) for Distributed JavaScript Apps] (https://www.youtube.com/watch?v=M8-WFTjZoA0)


Main Ideas on realtime-collaboration:

    1. There is a mandatory property for all types of algorithms support for ***concurrency*** and ***convergance*** to a single document 
    2. Synchronization can be state based (CRDTs and so on) or operation based (OTs and CRDTs)
    3. State based approaches are: Differential synchronization or three-way merges (as adopted by GIT or other source version control systems)

