# Spotify Collaboration Network Analysis

## Question
Which artists act as the key collaboration hubs in recent top-streamed Spotify tracks, and how do these hubs differ by total audience reach?

## Stakeholder
Record labels and artist managers deciding whom to target for features and cross-promotion.

## Data
- Source: Spotify "Most Streamed Songs" CSV (Kaggle).  
- Key fields: `track_name`, `artist(s)_name`, `artist_count`, `streams`, `in_spotify_playlists`, `in_spotify_charts`, release date.  
- Filtered to multi-artist tracks, cleaned streams (numeric), and standardized artist names.  

## Method
- Built a collaboration graph with **NetworkX**:
  - **Nodes** = artists  
  - **Edges** = co-credits  
- Measured **degree centrality**, **betweenness centrality**, and **total streams**.  

## Findings
- Top hubs: **Metro Boomin, Bad Bunny, Feid**.  
- They combine **many collaborators** (structural importance) with **high streams** (audience reach).  
- High-betweenness artists act as bridges between subgenres/markets.

## Outputs
- Bar chart of Top-10 central artists.  
- Network graph (full + Top-10 subgraph with node size = streams, edge thickness = collab frequency).  

## Limitations
- Only reflects **most-streamed tracks**, not full catalogs.  
- Streams influenced by playlists/virality.  
- Dataset skewed toward **recent hits**.  

## Tools
**pandas**, **networkx**, **matplotlib**, **folium/pyvis**.

---

**Author: Wuilmer Palacios**
