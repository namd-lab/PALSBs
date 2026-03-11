# Graph response network construction and transformer training code.
This codebase includes the complete set of initial DFT calculations, graph reaction network construction code, and machine learning training code.

# Install the necessary dependency libraries
numpy         1.26.4
pandas        2.2.2
seaborn       0.13.2
torch         2.1.1+cu118
networkx      3.2.1
py2neo        2021.2.4
shap          0.47.0

# Structure_Energy
Optimized geometric structure. "structure_energy.csv" refers to the total energy obtained for each structure through DFT calculation.

# DFT_to_Graph_Database
The node_edge.csv file maps the reactants to products for the annotated elementary reactions. The Graph_database.csv file is constructed by running the DFT_to_Graph_Database/DFT_to_Graph_database.ipynb code and provides a comprehensive set of total energy data computed via DFT for all adsorption systems.

# Graph_Response_Retwork_Construction
Executing the S8_Li2S pathway.ipynb code generates the complete reaction network, which can be visualized as an interactive graph in the Neo4j interface. The resulting Energy_barrier.csv file is used for training deep learning models on classification and regression tasks. Furthermore, df_Li2S4_Li2S.csv contains all the short-chain reaction pathways, while the S8_Li2S_16e-_batteries.csv file can be directly used to plot the free energy steps for all 407 pathways.

# DL_Regression
Executing the deep_learning_Regression.ipynb code evaluates the training performance of the regression model. In this model, reaction pathways are first converted into word vectors via a Bag-of-Words model as input, with the total uphill free energy change serving as the training target.

# DL_Classification
Executing the deep_learning_class.ipynb code evaluates the training performance for the three-class classification task. The model uses features derived from the MoS2@Li2S2, MoS2@Li2S3, and MoS2@LiS3 reaction pathways processed by a Bag-of-Words model as its input.


# cite literature
The manuscript titled "Photo-Electrocatalytic Chemical Pathways in Photo-Assisted Lithium-Sulfur Batteries via a Multiscale Graph-Based Machine Learning Framework" has been accepted by the Journal of the American Chemical Society.
