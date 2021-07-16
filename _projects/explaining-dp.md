---
title: Explaining differential privacy
toc: true
toc_label: Contents
---

Differential privacy provides formal guarantees on privacy; it provides a framework that allows the sharing of summary statistics of a dataset without disclosing additional information of any individuals in the dataset. However, few medical research data are released with differential privacy at the moment, as it is yet to be introduced to the medical community at large. 

## xDP, a Tool that Explains Differential Privacy

To facilitate the much needed discussions about differential privacy in the medical research community, we are developing xDP, an interactive tool with dynamic and animated visualizations that explains various concepts about differential privacy to stakeholders in medical research, those who are involved in the decision-making process of medical data usage, such as patients, researchers, ethics board members, privacy assessment office, and data stewards. 

As there are various types of stakeholders, each with different backgrounds and preferences for different levels/types of detail about differential privacy, xDP has multiple layers, equipping each stakeholder with necessary information to reason, discuss and eventually make their conclusions about if and when to adopt differential privacy; all stakeholders can start by understanding the high level concepts behind differential privacy, and those who wish to learn more can continue to additional modules that explain the more complex aspects of differential privacy. 

## xDP, a Tool that Helps Select Epsilon
The choice of epsilon is often left as a social problem, beyond the scope of technical discussions of differential privacy. xDP will guide stakeholders to reason about the cost and prior probabilities of privacy leaks as well as the cost of inaccurate analysis. Intuitions and insights developed through xDP can in turn facilitate discussions about the ways in which epsilon should be set when differential privacy is used in data sharing and ultimately help establish guidelines in selecting optimal epsilon values that would satisfy both privacy and accuracy requirements of all stakeholders, benefiting the society at large.
