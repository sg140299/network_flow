# network_flow
  Weighted Connected Directed Graph acts as a network flow where vertices are junctions and edges are pipes.
  FLOW OF THE NETWORK - Flow of the material at any point is intutively defined as the rate of the material.
  CAPACITY -Maximum amount of material that can flow through a edge.
  Flow f<=x where x is the edge weight.
  RESIDUAL CAPACITY = Total Capacity - Flow of Material
  AUGMENTED PATH - A path from source to sink such that the residual capacity on every edge is greater than 0.
  Maximum flow is equal to the minimum augmented path.
  
  =
  =========================================================================================================
  ======================================== FORD FULKERSON ALGORITHM =======================================
  =========================================================================================================
  POINTS TO KEEP IN MIND-
  1- Flow cannot be greater than the max capacity of an edge.
  2- For conservation of flow the amount of flow coming in is equal to amount of flow going out excluding source and sink.
  3- Max flow will be equal to the minimum weight of edge.
  4- Any augmented path should have non zero backward edge and a non full forward edge.
  
  ALGORITHM (dfs is used to find diff augmented paths)
  1- Set up our directed residual graph with edge capacity equal to the original graph weights.
  2- Initialize the value of maxflow equal to 0.
  3 while(there exists any augmented path from source to sink):
     i) find 'f' the minimum edge weight along the current path.
     ii) decrease the capacity of all the forward edges by f and increase the capacity of all the backward edges by f.
     iii) increase the value of max_flow by f.
 4- print max_flow
 BACKWARD EDGE COMPATIBILITY
 
