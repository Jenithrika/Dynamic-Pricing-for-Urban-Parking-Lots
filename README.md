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

