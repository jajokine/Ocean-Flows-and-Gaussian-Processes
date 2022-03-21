# Ocean-Flows-and-Gaussian-Processes
MITx - MicroMasters Program on Statistics and Data Science - Data Analysis: Statistical Modeling and Computation in Applications - Fifth Project

The aim of the project was to model flow-based environmental data, namely ocean flows measured in the Philippine Archipelago, with multivariate Gaussian random variables, and generate dynamic simulations based on Gaussian Processes.

Compared to linear or logistic regression, where we try to find parameters that match a certain function f(x), the Gaussian Process (GP), is a non-parametric approach based on probabilities where we try to find a probability distribution over the possible functions f(x) that are consistent with the observed data points. This is the Bayesian approach or Bayes' Rule, based on conditional probabilities, where our knowledge of knowing something becomes more certain as we gather more data.

The GP begins with a prior distribution that is based on domain specific knowledge about the analyzed topic and which is then updated as each data points are observed, producing eventually the posterior distribution or the probability that the data points come from a certain distribution with a specific mean and variance. The expected values of the distribution of f(x) are defined with the mean function that tells us the mean at any point of the input space, and the covariance matrix, which can be generated from a covariance function - the kernel function - making the computations of the covariance between points more managable and efficient to produce. 

What makes the covariance matrix important is that it tells us about the relationship of the observed data points, and in particular their dependencies, whether they are correlated or not to each other. This correlation that helps in making predictions, can be measured in time (e.g. with temporal patterns such as seasons) or with spatial correlations that measure linear dependencies or relations between variables measured at close-by, or even longe-range locations (e.g. temperature). In this project, the dependencies are measured through the velocity of the ocean flow that can change in time and space, and therefore the flows are measured as vectors that form a vector field, which are then modelled as multivariate Gaussian random variables.

The dataset, which due to big size cannot be downloaded unfortunately here, consists of water flow data in the form of horizontal and vertical velocity vector components around the Philippines that measure the direction and the magnitude of the flow (i.e. displacement in time). The information was measured in a number of discrete locations in 2009 by the MSEAS research group at MIT (http://mseas.mit.edu) which then constructed the data by using a data-assimilative multiresolution simulation.

## Access and Requirements

The file [project5.ipynb](https://github.com/jajokine/Ocean-Flows-and-Gaussian-Processes/blob/main/project5.ipynb) is the Jupyter Notebook that contains all the code, visualizations and analysis of the project.

The dependencies and requirements can be seen from requirements.txt that can be installed in shell with the command:

      pip install -r requirements.txt


