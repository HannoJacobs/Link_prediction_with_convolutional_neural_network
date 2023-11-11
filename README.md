## The problem statement
### Project 1: Link prediction model
The goal of this project is to propose effective and efficient solutions for the link prediction task. Specifically, given an input graph G, some of G's edges have been removed, and the resulting graph is called G'. Given some pairs of nodes from G', we must determine whether there is an edge between the node pairs in the original graph G. The dataset used in the competition is taken from Wikipedia, where graph nodes are annotated with text.
Link prediction is an important task in networks. Given a pair of nodes (u, v), we must predict whether or not the edge between u and v will be present. Link prediction is closely related to recommendations, network reconstruction, and network evolution. This competition focuses on the link prediction task as it applies to Wikipedia articles. In particular, given a sparsified subgraph of the Wikipedia network, we must predict whether a link exists between two Wikipedia pages, u and v.
You are given a ground-truth file that contains pairs of nodes corresponding to positive and negative samples. For example, if an edge exists between two nodes, the corresponding label is set to 1. Otherwise, the label is 0.
20% of the information from the original file has been removed. This includes both positive and negative pairs (where the edge is present) and negative pairs (where the edge does not exist). Your mission is to correctly identify the positive and negative pairs.
Please keep in mind that just because a pair of nodes is not reported in the file does not mean that there is no edge between them. In other words, if a pair of nodes ( u, v ) does not appear in the file, no conclusion can be drawn about their direct connection. Please keep in mind that the test dataset has been split to 50% and Macro F1 score can be used in the evaluation process.
### Dataset
There are three available datasets. The most important ones are train.csv and nodes.zip. The file train.csv contains pairs of nodes and an indication of whether there is an edge between them or not. More specifically, train.csv contains four columns: id, id1, id2, and label, where id is the identifier of the pair, id1 and id2 are the node ids, and label (either 0 or 1) declares the edge. The file nodes.zip is a compressed version of nodes.tsv, which contains information for each node. This file is composed of two columns, id and text, where id is the node identifier and text is a textual description of the node. In addition, a demo submission file is also given (sample_submission.csv). This file contains only two columns: the id of the pair and the corresponding label (either 0 or 1). Your submission file should also contain these two columns, i.e., id and label. You need to provide a prediction for all test elements listed in test.csv   
[Dataset google drive link](https://shorturl.at/beLT0)

### Reference:
1. Bhowmik R, de Melo G. Explainable link prediction for emerging entities in knowledge graphs. InThe Semantic Web–ISWC 2020: 19th International Semantic Web Conference, Athens, Greece, November 2–6, 2020, Proceedings, Part I 19 2020 (pp. 39-55). Springer International Publishing.