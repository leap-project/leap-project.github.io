---
title: Design and Software Stack
permalink: /architecture/software-stack/
header:
  teaser: /assets/images/architecture.png
---

LEAP is a federated and privacy preserving evaluation and analysis platform that allows users to run different types of queries, including training machine learning models on distributed data. LEAP achieves this through an infrastructure that brings the computation to the data, instead of bringing the data to the computation.

Cloud Algo: The cloud algo is written in Python and is responsible for aggregating the data from the multiple sites and post-processing them before returning an aggregate to a user. To get a response from pre-selected sites, the cloud algo uses GRPC to send a protobuf message to the coordinator, which handles all communication between the cloud and a local site.

Coordinator: The coordinator, written in the Go programming language, is responsible for managing all the sites available in the LEAP system. It is responsible for propagating the proper error messages to the cloud algo when a site is down, and for passing the computation requests issued by the cloud algo to the proper sites. When a coordinator contacts a site, it serializes the request using protobuf and uses grpc to issue a remote procedure call to each site. The coordinator has a multithreaded design in which one goroutine (Go thread) listens for cloud algo connections and another goroutine listens for site connector connections.

Site Connector: The site connector runs a grpc server written in Go that listens to requests from the coordinator. Before showing up as available, the site-connector sends a registration request to the coordinator. After this is done, the site connector can receive computation requests from the coordinator and delegates them to a node running the site algo. Communication between the site connector and the site algo also uses grpc and protobufs for serialization.

Site Algo: The site algo is a Python program responsible for retrieving the appropriate data from a database and running some sort of computation on the data. If differential privacy (DP) is turned on, the site algo is responsible for taking the appropriate measures to make the result differentially private, such as adding Laplacian noise to the result. The site algo uses the REDCap API to retrieve the data from a REDCap database or a REDCap external module that is optimized for cases where all the necessary computation can be done in a SQL query.
