# nyc_subway_gtfs
----use NYC SUBWAY GTFS to get schedule and build up network

#### 0clean_up_nodes_and_transfer_time: </br>
which stations have which lines going through

#### 1subway_line_sequence_and_schedule.ipynb:</br>
gets sequence of all the stations along each line, and get travel time between every next station</br>

#### 2Set_up_network.ipynb</br>
##### Node
is defined as platform at each station.For example, 42 St Time-sq will have 4 nodes, (1)N Q R W train;(2) 1 2 3 train;(3) S train; (4) 7train </br>
##### Edge- weighted, directed, multi-edged</br>
Three types of edge:</br>
1) connections between stops by train</br>
2) connections between stops by transfer(walking), eg.from 42 St Bryant Park to 5 Av</br>
3) connections within stops by transfer(walking), eg. from N train platfrom in 42 St Time-sq to 7 train platform in 42 St Time-sq</br>

##### Weighted
- the edge are weighted by time cost from nodes to nodes</br>
##### Directed
- A-->B is different from B-->A, because Aqueduct Racetrack(A train) has only north bound train, and Aqueduct North Conduit Av has only south bound train. Also, the time cost of A-->B and B-->A is not always the same </br>
##### Multi-edged
- if node_A is connected to node_B by both 1 train and 2 train, then there will be two edges.
