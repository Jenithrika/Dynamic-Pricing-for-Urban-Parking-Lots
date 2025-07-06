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

#  Project Architecture and Workflow
The project simulates a dynamic pricing system for urban parking using real-time demand signals, competitive positioning, and pricing rules. Here's how the entire pipeline flows:

## 1. Data Ingestion and Preprocessing
Input Source: Live or simulated real-time data stream from Pathway (model2_window).

Features: Includes SystemCodeNumber, price, occupancy, capacity, timestamp, latitude, longitude, and derived norm_demand.

Preprocessing:

Timestamps are parsed.

Dates are extracted.

Static location data is merged.

Unique sorted dates are used to build a map of previous dates (for lagged logic).

## 2. Model 1 – Linear Pricing
A simple benchmark model using a linear pricing formula.

Prices are computed based on fixed multipliers on demand.

## 3. Model 2 – Demand-Based Pricing
Incorporates real-time occupancy-to-capacity ratio and norm_demand.

Prices increase with high demand and decrease when demand is low.

Enforces a price floor and cap to keep prices realistic.

## 4. Model 3 – Competitive Pricing Model
Location intelligence is used to determine nearby competitors (within 1 km radius).

Uses previous day's competitor prices as a proxy for market rates.

Adjusts pricing using clear business rules:

If the lot is full and competitors are cheaper → reduce price slightly.

If demand is high and competitors are expensive → raise price moderately.

In low-demand zones, avoid overpricing.

Neutral price band prevents overreaction to small fluctuations.

## 5. Price Adjustment Logic
Final prices are adjusted in Adjusted_Price based on:

Occupancy conditions

Competitive undercut/overpricing scenarios

Market responsiveness

A safeguard ensures prices stay between ₹10 and ₹20

## 6. Evaluation
All models are compared based on:

Total Revenue generation

% of time the model undercut competitors

% of time the model was overpriced

Smart pricing opportunities captured

Model 3 performs nearly as well as Model 2 in terms of revenue but offers better business realism and market adaptiveness.

## 7. Visualization
Visualisations created using Bokeh:

Time-series plots of adjusted prices across lots

Comparative price trendlines for all models

All plots are saved as a PDF document and added to the repo.

