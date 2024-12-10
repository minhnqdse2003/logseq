# Problem
	- Unreliable network
	  logseq.order-list-type:: number
	- Computers prone to failure
	  logseq.order-list-type:: number
	- Availability
	  logseq.order-list-type:: number
	- How to avoid involving people when things fail.
	  logseq.order-list-type:: number
- # Effective Consensus Algorithms
	- Consistency between participant state machines
	  logseq.order-list-type:: number
	- Tolerant of failure of 1 or more participant.
	  logseq.order-list-type:: number
	- Tolerant of unreliable networks and network partition
	  logseq.order-list-type:: number
- # Features of Consensus Algorithms
	- Agreement 
	  logseq.order-list-type:: number
	- Validity
	  logseq.order-list-type:: number
	- Termination
	  logseq.order-list-type:: number
- # Terms
	- Leader
	  logseq.order-list-type:: number
	- Follower
	  logseq.order-list-type:: number
	- Client
	  logseq.order-list-type:: number
	- Log
	  logseq.order-list-type:: number
	- Leader accept data from the client -> Leader send data to it followers -> And in each participant the log store it act as the state machine and it aim to have the logs match.
- Election and Log Propagation
	- Asynchronous -> No bounds on message response and received.
	  logseq.order-list-type:: number
	- Leader server until it die and trigger a new Election phrase.
	  logseq.order-list-type:: number
	- Cluster do not accept data during the Election phrase.
	  logseq.order-list-type:: number
	- ![2024-12-10-223904_839x269_scrot.png](../assets/2024-12-10-223904_839x269_scrot_1733845166420_0.png)
	  logseq.order-list-type:: number
- # How raft consensus perform
	- **`Prerequisite`**
		- **Term increase circumstances**
		  logseq.order-list-type:: number
			- *`Election Timeout:`* When a follower's election timeout expires, and it transitions to the candidate state, it immediately increments its current term number. This new, higher term number is included in the RequestVote RPCs it sends to other nodes to solicit votes.
			  logseq.order-list-type:: number
			- *`Receiving a Higher Term:`*If a node (whether a follower, candidate, or leader) receives a message from another node with a term number *higher* than its own, it immediately updates its current term to match the higher term. This ensures that all nodes eventually converge on the same term number, which is essential for maintaining consistency. This can happen when:
			  logseq.order-list-type:: number
				- A follower receives a RequestVote RPC with a higher term.
				- A candidate receives a RequestVote response or an AppendEntries RPC with a higher term.
				- A leader receives an Append Entries response with a higher term
		- **Raft specific criteria on voting**
		  logseq.order-list-type:: number
			- *`Term Number:`* Candidate's term number >= Voter's current term.
			  logseq.order-list-type:: number
			- *`Log Completeness (Up-to-date logs):`* The voter checks if the candidate's log is at least as up-to-date as its own. Raft uses a simple mechanism to determine log completeness:
			  logseq.order-list-type:: number
				- The voter compares the index and term of the last entry in its log with the corresponding values in the candidate's log.
				- If the candidate's log has a later term number in its last entry, it's considered more up-to-date.
				- If the term numbers are the same, the longer log is considered more up-to-date.
				  If the candidate's log is not at least as complete, the vote is rejected. This ensures that more complete logs are prioritized.
			- *`Prior Vote in Term:`* The voter must not have already voted for another candidate in the current term. If it has, it rejects the vote request. This prevents a node from voting for multiple candidates in the same term, which could lead to a split vote.
			  logseq.order-list-type:: number
	- Start as followers
	  logseq.order-list-type:: number
	  collapsed:: true
		- ![2024-12-10-224243_921x600_scrot.png](../assets/2024-12-10-224243_921x600_scrot_1733845367482_0.png)
	- Start Election phrase
	  logseq.order-list-type:: number
		- Each follower will have a random election timeout. And when followers do not receive any heartbeat from leader node within its election of time, it transitions to the candidate state, Increase it current term number, vote for itself. Sends `RequestVote` RPCs to all order node in a cluster.
		- And if Candidate receives vote from majority of the cluster. It become a new leader. Otherwise, it will remain candidate and continue to election process.
		- ![2024-12-10-233608_899x562_scrot.png](../assets/2024-12-10-233608_899x562_scrot_1733848585545_0.png)
- # Problem with even number of node in consensus
	- **Leader Loses Connection:** If the leader (node 1) loses connection with *only* node 2, the leader *remains* part of the cluster. It still has a connection to nodes 3 and 4. A majority of the cluster (3 out of 4 nodes) can still communicate. Node 1 will continue to function as the leader, albeit with reduced redundancy. Nodes 3 and 4 will continue to receive heartbeats from node 1 and consider it the leader.
	- **Leader Isolated:** If the leader (node 1) loses connection with *both* nodes 2 *and* 3 (or 2 *and* 4), then it becomes isolated. The remaining nodes (2, 3, and 4, or 2, 4, and 3) constitute a majority and will hold a new election.
	- **New Election:** The followers (2, 3, and 4 in the isolation scenario) will time out because they are no longer receiving heartbeats from node 1. They will transition to candidates, increment their term numbers, and request votes. One of them will win the election (assuming no split votes) and become the new leader.
	- **Old Leader Recovers:** When node 1 recovers and rejoins the cluster, it will notice that the other nodes have a higher term number than itself. This immediately indicates that it is no longer the leader. Node 1 will revert to a follower state, update its term number to match the cluster, and begin receiving log entries and heartbeats from the new leader.
	  
	  **Key Points:**
	- **Majority Matters:** Raft operates based on majorities. As long as the leader can communicate with a majority of the cluster, it remains the leader. The loss of a single follower doesn't trigger a new election unless it isolates the leader from a majority.
	- **Term Numbers:** Term numbers are essential for Raft's operation. They provide a mechanism to identify stale information and ensure that only one leader is active at a time. A node with a lower term number always defers to a node with a higher term number.
	- ```
	  # Majority means more than a half of the voting nodes in cluster
	  # A candidate must receive votes from a majority of the cluster's voting members to become the leader.
	  If the leader retains a majority, it remains the leader. If it loses its majority, a new election is triggered.
	  ```