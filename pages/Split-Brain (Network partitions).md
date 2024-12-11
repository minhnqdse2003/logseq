# Problem context
	- You have two cluster that connect to the other one, one of them will be the master cluster and the other one is followers. In the scenario of the connection break between them, if we use even number of manager nodes. We will have two group of managers, one have the leader (old one) and group for the other two nodes of followers (this will choose the new leader based on which is  the new one). And now we will have two group that perform the same action on the same data centralize store.
- # Solution
	- Using odd number of managers, because Docker swarm using [[Consensus Algorithms]] to prevent it.
-