---
title: Federated machine learning across RedCap databases
---

REDCap is a popular database tool for research and survey applications with over 1.3 millions users [[1]](https://www.project-redcap.org). It is primarily used in healthcare research to collect and store survey data. One of the goals of the LEAP system is to allow multiple data sources to contribute to data analysis in a privacy focused, federated manner. REDCap is a critical data source for LEAP, so the goal of this project is to connect REDCap to LEAP and to implement federated ML algorithms across multiple REDCap instances via LEAP. 

{% include figure image_path="/assets/diagrams/LEAP-REDCap.png" alt="Leap cache" caption="Leap Cache Diagram." %}

## This project has two primary objectives:
1. Build a LEAP connector module for REDCap. This will be an external module [[2]](https://github.com/vanderbilt/redcap-external-modules) that can be installed on any REDCap instance, and will provide LEAP with API-based access to the database in REDCap.
2. Implement federated statistical and machine learning algorithms that will allow computations to be mapped to the sites and the results to be aggregated in the cloud. The focus of this objective is to optimize the federated ML pipeline to work with REDCap.

### References:
1. Project REDCap: [https://www.project-redcap.org](https://www.project-redcap.org)
2. REDCap External Modules: [https://github.com/vanderbilt/redcap-external-modules](https://github.com/vanderbilt/redcap-external-modules)
