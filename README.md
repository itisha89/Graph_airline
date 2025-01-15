# Airline Network Analysis: Identifying the Most Important Airport for Operations

## Business Problem
A new airline is in the process of determining the most important airport to initiate its operations. The goal of this analysis is to identify the busiest and most cost-effective airport to establish operations based on the number of flights, which correlates with factors like passenger volume, destinations covered, and network connectivity.

## Dataset Overview
The dataset used for this analysis was extracted from a website and focuses on the following attributes:
- **Origin Airport**
- **Destination Airport**
- **Number of Flights**

The dataset consists of the number of flights between airports, and we consider this as a primary factor for evaluating the importance of an airport, with other factors such as passengers carried and destinations covered assumed to be proportional to the number of flights.

### Dataset Details:
- **Source**: [Kaggle Dataset](https://www.kaggle.com/code/danishmehmuda/flightnetworkanalysis/data)
- **Number of Nodes**: 931 (representing airports)
- **Number of Edges**: 12,377 (representing flights between airports)
- **Graph Type**: Directed and Weighted

## Objective
The primary objective of this analysis is to find the busiest and most cost-effective airport for setting up airline operations by calculating the **importance** of each airport. Several techniques were used to measure the importance of airports within the network.

## Techniques Used
The following centrality measures were used to evaluate the importance of each airport:
1. **Degree Centrality**
2. **Betweenness Centrality**
3. **Closeness Centrality**
4. **PageRank**

These metrics provide insights into the network structure and connectivity, helping determine which airport plays the most central role in the network.

## Results and Interpretation

### Degree Centrality
- **ATL (Atlanta International Airport)** has the highest degree centrality.
  - **Degree Centrality** = 0.363
  - **In-Degree Centrality** = 0.182
  - **Out-Degree Centrality** = 0.182
- **Interpretation**:
  - Degree centrality represents the number of direct connections (or flights) an airport has with other airports.
  - ATL has the maximum number of connections, indicating it is one of the most connected airports in the network.

### Betweenness Centrality
- **ATL** has the highest betweenness centrality score.
  - **Betweenness Centrality** = 0.0208
- **Interpretation**:
  - Betweenness centrality measures the number of shortest paths that pass through a particular airport.
  - ATL has the highest value of betweenness centrality, implying that it serves as a crucial connector in the network, with many shortest paths passing through it.

### Closeness Centrality
- **ATL** has the highest closeness centrality score.
  - **Closeness Centrality** = 0.232
- **Interpretation**:
  - Closeness centrality suggests that important nodes are closer to all other nodes.
  - ATL is located close to other important airports, facilitating efficient connections across the network.

### PageRank
- **ATL** has a PageRank score of 0.0131.
- The highest PageRank was found for an airport coded as **10397**.
  - **PageRank (10397)** = 0.0134
- **Interpretation**:
  - PageRank assigns importance based on incoming links from other airports.
  - While ATL has a strong degree centrality, the airport coded as **10397** has the highest PageRank, suggesting that incoming connections from other airports play a significant role in determining its importance.


## Conclusion
Based on the analysis, we suggest the following:
- **ATL** is the central node in the network, making it a prime candidate for the airline's base of operations.
- Setting up operations at ATL would likely be cost-effective, as it is part of a well-connected network, facilitating short-distance flights.
- Further study is recommended to understand the importance of incoming nodes to ATL, as factors such as traffic (passenger and cargo), competitiveness, and physical capacity may influence the decision.
  

