## Explaining differential privacy

1. State problem that people have.

 * Who has this problem?
 * How big is the problem?
 * What are current approaches to solving this or similar problems?

2. Discuss approach to handle problem.

 * We will build a tool, called xDP.
 * Explain why a tool is the right approach.

3. Describe xDP tool:

xDP is a tool to aid in explaining differential privacy in a visual and interactive format. The project has two components. The first component is explaining the concepts of differential privacy to stakeholders in medical research (i.e., patients, researchers, ethics board members, privacy assessment office, data stewards) that influence the decision making process in medical data usage. The second component is guiding researchers and data stewards in selecting an appropriate epsilon that satisfies the privacy concerns of patients as well as the accuracy requirements of researchers.

### Explaining Differential Privacy

Using our tool, users will gain an intuition for differential privacy through active learning. As there are various stakeholders ranging from patients to data stewards, each with different backgrounds and preferences for how much they would like to know, we are building the tool to have multiple layers.

All stakeholders can start by understanding the high level concepts behind differential privacy. Stakeholders who wish to learn more can continue to modules that explain the more complex aspects of differential privacy. We are also experimenting with dynamic and animated visualizations to better visualize the uncertainty aspect of differential privacy.

### Selecting Epsilon

The tool will also guide users in estimating properties of the privacy risk such as the cost and prior probabilities of adverse events, as well as the cost of inaccurate analysis. These insights will be used to help users select an optimal epsilon that satisfies both privacy and accuracy requirements.

