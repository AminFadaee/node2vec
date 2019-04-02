# node2vec (python 3)
This is a simple fork of [node2vec](https://github.com/aditya-grover/node2vec) - implemetation of the paper *node2vec: Scalable Feature Learning for Networks. A. Grover, J. Leskovec. ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD), 2016* that is working in python 3.6.

### Basic Usage

#### Example
To run *node2vec* on Zachary's karate club network, execute the following command from the project home directory:<br/>
	``python src/main.py --input graph/karate.edgelist --output emb/karate.emd``

#### Options
You can check out the other options available to use with *node2vec* using:<br/>
	``python src/main.py --help``

#### Input
The supported input format is an edgelist:

	node1_id_int node2_id_int <weight_float, optional>
		
The graph is assumed to be undirected and unweighted by default. These options can be changed by setting the appropriate flags.

#### Output
The output file has *n+1* lines for a graph with *n* vertices. 
The first line has the following format:

	num_of_nodes dim_of_representation

The next *n* lines are as follows:
	
	node_id dim1 dim2 ... dimd

where dim1, ... , dimd is the *d*-dimensional representation learned by *node2vec*.
