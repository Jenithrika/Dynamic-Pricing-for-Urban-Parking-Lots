# Dynamic-Pricing-for-Urban-Parking-Lots
# Overview
This project simulates dynamic pricing strategies for urban parking spaces using real-time occupancy data and competitive pricing intelligence. The goal is to optimize parking lot revenue while maintaining fairness and responsiveness in pricing.

Three models are implemented and evaluated:

Model 1: Linear Pricing — A static pricing model using fixed base logic.

Model 2: Demand-Based Pricing — Adjusts prices based on occupancy levels and estimated demand.

Model 3: Competitive Pricing — Enhances Model 2 by incorporating competitor prices and location-based competition awareness.

Performance is evaluated based on total revenue, price fairness, and responsiveness.

# Tech Stack

| **Category**                | **Technologies Used**                                                                |
| --------------------------- | ------------------------------------------------------------------------------------ |
| **Programming**             | Python                                                                               |
| **Data Handling**           | [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/)                    |
| **Streaming Engine**        | [Pathway](https://pathway.com/) for real-time data simulation and transformation     |
| **Visualization**           | [Bokeh](https://docs.bokeh.org/) for interactive time-series plotting                |
| **Geospatial Logic**        | [Geopy](https://geopy.readthedocs.io/) for calculating distance between parking lots |
| **Development Environment** | Google Colab, GitHub                                                                 |

<pre><code>```mermaid flowchart TD A[Pathway Data Stream] --> B[Base DataFrame<br/>(Prices, Timestamps, Occupancy, Location)] B --> C1[Model 1:<br/>Linear Pricing] B --> C2[Model 2:<br/>Demand-Based Pricing] B --> C3[Model 3:<br/>Competitive Pricing] subgraph Pricing Models C1 --> D1[Linear Prices] C2 --> D2[Demand-Based Prices] C3 --> D3[Competitor-Aware Prices] end B --> E[Competitor Identification<br/>(within 1 km)] E --> C3 D1 --> F[Revenue Evaluation] D2 --> F D3 --> F F --> G[Bokeh Plots & Visual Reports] ```</code></pre>
