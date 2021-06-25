##Notes

There are two approaches to solve this problem:
   1. Operational Transformation: To achieve eventual consistency for documents, OT is supposed to possess following properties. Couple of models are developed to achieve those properties and one example is [CCI](https://en.wikipedia.org/wiki/Operational_transformation#The_CCI_model). Below we also mention which properties are possessed by CGI approach
         1. ***Convergance:*** All copies of documents must look exactly the same after execution of all operations
         2. ***Intention preservation:*** Effect of operation should be the same as expected by the user. For example, suppose user wanted to delete o at position 4 then even if other operations are executed before that, transformed operation should take that into account and delete the exact same character at adjusted plance to accomodate the intention
         3. ***Causality preservation:*** Operations must be executed accordingly to their natural cause-effect order during the process of collaboration (based on [happened before](https://en.wikipedia.org/wiki/Happened-before) relation). CCI model doesn't have this propety, other properties mentioned above it has


   2. Conflict-Free Replicated Data Types (CRDTs)





Core point in CRDTs is to make sure operations are commutative (commutative means order of operations doesn't matter). If we can ensure that and come up with some smart rules for each conflict resolution then it will work. 

`
   Example:
   
      There are two Nodes A and B. Idea is that each letter is given an incrementable ID,  for example each node starts with word "helo"
      
        Node A                            Node B
      
        h   e   l    o                     h   e    l    o
        1a  2a  3a   4a                    1b  2b   3b   4b
        
        insert l after "3a"                insert ! after "4b"

       # Each insert results in incremented id, for example in case of Node A next ID will be 5a and for B it will be 5b

        h   e   l    l    o                     h   e    l    o   !
        1a  2a  3a   **5a**   4a                1b  2b   3b   4b  5b
        
        
        
`


1. [Talk Video: Simple collaborative text editor using CRDTs](https://www.youtube.com/watch?v=jIR0Ngov7vo), 
  [Talk blog link](https://digitalfreepen.com/2017/10/06/simple-real-time-collaborative-text-editor.html)

2. [Video: System design with proper diagram: OT based](https://www.youtube.com/watch?v=g9VIh13SA1Y) 

[OT best explanation with example](https://hackernoon.com/operational-transformation-the-real-time-collaborative-editing-algorithm-bf8756683f66)

3. [Martin Klepmann video on CRDTs](https://www.youtube.com/watch?v=B5NULPSiOGw)

4. [Operational Transformation good explanation](https://medium.com/coinmonks/operational-transformations-as-an-algorithm-for-automatic-conflict-resolution-3bf8920ea447)
