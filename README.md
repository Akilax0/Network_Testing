# Network_Testing
These are a collection of scripts and steps used to evaluate congested scenarios at PeraCom

## Situation 
The DCE building has two subnetworks running, 10.40.18.* and 10.40.19.* 

All student Lab computers and servers are running on the 18 network while a lecturer offices are on 19.

We observed a drop in network connectivity during a video lecture on 21st April 2025. The session was done by a lecturer connected to the 19 network while one of the projectors connected to a computer on the 19 network where both observed a network drop. However the students were either on the 18 network (lab machines) or WIFI. Upon further observation we figured that both the networks were going through the same set of switches. 

- One assumption is that a large stream of 18 network traffic would flood the network resulting in delays for 19 network traffic reslution.
- Another is that the department DNS server (that is unmaintained but is configured for all student machines) is causing the issue of directing the traffic within the network rather than sending them out of the network through the L3 switch (where all traffic leads to)


## Possible Solutions
