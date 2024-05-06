# Team members
Manuel Knepper - mkne@itu.dk
Steinar Slette - stsl@itu.dk

# Mini_project_aml
Mini project for Advanced Machine Learning at ITU spring 2024
Dataset link - https://ogb.stanford.edu/docs/linkprop/#ogbl-ddi

# Goal
Our task in this project is to implement different graph neural networks to investigate link property prediction of the OGB ddi dataset that contains drug-drug interractions
and see how the different implementations affect the results when compared to a baseline model. 

# Dataset information
The ogbl-ddi dataset is a homogeneous, unweighted, undirected graph, representing the drug-drug interaction network [1]. Each node represents an FDA-approved or experimental drug. Edges represent interactions between drugs and can be interpreted as a phenomenon where the joint effect of taking the two drugs together is considerably different from the expected effect in which drugs act independently of each other.

# Central method(s) 
We have decided to work with gnn's for this implementation and we are using a predefined GCN (Graph Convolutional Network) procedure for the baseline of the model. Further we have implemented a GAN (Graph Attention Network) and a GraphSAGE method to investigate how these models compare to the baseline model. 

# Key experiments and results 
The metric we use for evaluation is Hits@30, which corresponds to ranking true drug interactions in a set of 100000 randomly-sampled negative drug interactions, and counting the ratio of positive edges ranked at 30-place or above.
![image](https://github.com/Steinar-Slette/mini_project_aml/assets/71990567/0322b0fb-d384-473f-89ab-03a12f8c7ea1)

# Discussion 

The findings that are represented in this report showcase the results gained for the different implementations of models in our project.
The model parameters are based on set values that are largely equal accross the different implementations, and although a multitude of values were tested during production in order to investigate the different impacts this would have on the models it is not a focus of this report due to the nature of our analysis and the fact that we want to investigate different implementations and not focus so heavily on parameter tuning. 

The resulting accuracies and metrics visualized accross the different models tells us that in this case, our GraphSAGE model performed the best on our given data and choice of scoring metric The Graph Attention network also performed better than our baseline model during most of the training process, although we do see some inconsistency at the end. In the case of our particular task with the given dataset, we can to some degree conclude that our chosen implementations of methods outperformed the baseline model. These results do not neccecarily generalize for all link property prediction tasks and/or other tasks involving graphs and GNN's.

# Improvements 
Possible improvements could involve a larger focus on tuning parameters in order to find optimal values for the individual implementations.
