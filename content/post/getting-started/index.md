---
title: Application of Graph Neural Network in Vulnerability Mining
subtitle: 

# Summary for listings and search engines
summary: Vulnerability mining based on graph neural network is one of the current research hotspots. Representing source code as a graph structure (abstract syntax tree, data flow graph, control flow graph, code property graph, etc.) can better represent the syntax in the code , semantics, structure and other information, this article shares several GNN-based vulnerability mining articles, aiming to summarize the methods, learn the research ideas, and explore the existing problems.

# Link this post with a project
projects: []

# Date published
date: "2022-04-13T00:00:00Z"

# Date updated
lastmod: "2022-04-24T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
#   focal_point: ""
#   placement: 2
#   preview_only: false

authors:
- admin

tags:
- Code Representation
- Vulnerability Analysis
- Graph Neural Network

categories:
- Posts
---

## Overview


**Abstract**: Vulnerability mining based on graph neural network is one of the current research hotspots. Representing source code as a graph structure (abstract syntax tree, data flow graph, control flow graph, code property graph, etc.) can better represent the syntax in the code , semantics, structure and other information, this article shares several GNN-based vulnerability mining articles, aiming to summarize the methods, learn the research ideas, and explore the existing problems.


**Existing Issues**:
- Vulnerability detection is a task that attempts to discover software vulnerabilities by auditing the software code or analyzing the software's execution. It requires understanding and reasoning about program semantics. Therefore, the methods used to detect bugs cannot be directly used for vulnerability detection.
- Rule-based and vulnerability mining: Experts are required to manually add vulnerability rules, it is impossible to list all vulnerability rules, and the time and labor costs are too high.
- Traditional deep learning methods, such as GRU, LSTM, BiLSTM, etc., treat the source code as a text sequence for learning, ignoring the structural information of the code.
- Existing approaches work by converting the code into input for graph structures during preprocessing and learning the semantic, structural, and other information in them directly through graph neural networks (GNNs). However, most GNN-based approaches only allow message delivery in the 𝑘-hop neighborhood (where k is usually a decimal number), thus capturing only local neighborhood information and ignoring global interactions between nodes.

## BGNN4VD: Constructing Bidirectional Graph Neural-Network for Vulnerability Detection
*Journal*: Information and Software Technology
### Methodology

![截屏2021-08-08 下午6.40.21.png](https://i.loli.net/2021/08/08/N7ruSPsWfymiokQ.png)

The syntactic and semantic information in the source code is extracted by AST, CFG, DFG, and then vectorized as the input of BGNN to learn the different features between fragile and non-fragile codes by introducing edges based on the traditional graph neural network (GNN), and further extracting features and detecting vulnerabilities by classifier using convolutional neural network (CNN).

- Phase 1: Syntactic information is represented by AST and semantic information can be represented by CFG and DFG. A code composite graph (CCG) is constructed by combining AST, CFG and DFG. CCG consists of a set of AST nodes and different types of edges. The statement and predicate nodes are connected by CFG and DFG. Thus, the types of edges reflect the syntactic and semantic relationships between different nodes.
- Phase 2: The text features of each node are represented as vectors using Word2Vev. To further reflect the abstract semantic relationships between words, the type of each node is considered and added to the transformed vector to calculate the state of the initial node. For example, the code result = num1 result and num1 are both identifiers Identifier, so the type of the chicken eh single (identifier, function, etc.) and the textual features of the node are represented as vectors and then spliced as the new features of the node.
- Phase 3: After obtaining an initial node representation that can be used as input to the deep learning model, BGNN is used to train the detection model to learn aggregated information as it is suitable for non-sequential output and semantic learning. **Because source code is more logical and structured than natural language, fragments of vulnerability code are usually related to their contexts**. Therefore the model needs to be able to process sequences back and forth to obtain a deeper representation and to obtain better robustness. The paper constructs a Bidirectional Graph Neural Network (BGNN) . The final representation of the nodes is finally output through the BGNN.
- Phase 4: Train the classifier for vulnerability classification using the node representation from the previous step.

## A Unified Framework to Learn Program Semantics with Graph Neural Networks
*conference*: ASE-2020
### Methodology

 ![截屏2021-08-08 下午10.17.33.png](https://i.loli.net/2021/08/08/86nI5PBgGOu47yX.png)

 The use of graph neural networks (GNNs) to represent programs has achieved state-of-the-art performance in many applications; however, a unified framework for GNNs for different applications is currently lacking; moreover, most existing GNN-based approaches ignore global relationships with nodes, limiting models to learn rich semantics.The authors propose a unified framework to construct two types of graphs to capture rich code semantics for various SE applications.



## A Hybrid Graph Neural Network Approach for Detecting PHP Vulnerabilities
*Journal*: Information and Software Technology
### Methodology

![截屏2021-08-08 下午11.41.55.png](https://i.loli.net/2021/08/08/iPjYfLhS1aZToC9.png)

DeepTiver detects SQLi, XSS and OSCI vulnerabilities at function and file level granularity in source code, and is divided into two key components: a gated recursive unit (GRU) running on a linear sequence of source code tokens, and another applying a graph convolutional network (GCN) to the control flow graph (CFG) of the source code. Each component provides a different mechanism for the model to efficiently detect multiple types of vulnerabilities, and finally combines GRU and GCN in a new hybrid architecture that is able to exploit the advantages of both techniques.

**Component**
- graph construction, encoding the source code into semantic-based and attention-based graphs.
- Semantic learning, which fuses the messages in the constructed graphs with their respective message-passing functions in order to learn the full code semantics.
- Applications that use learned code semantics for vulnerability identification, code clone detection, etc.


## Devign: Effective Vulnerability Identifification by Learning Comprehensive Program Semantics via Graph Neural Networks
*Conference*: 2019-NIPS
### Methodology

Devign a generic graph neural network based model that learns rich code semantics for graph-level classification representations. It includes a Conv module that can efficiently learn rich node representations and extract useful features from them for graph-level classification.

![截屏2021-08-10 下午11.21.26.png](https://i.loli.net/2021/08/10/MjKfHyhBGXpgYU9.png)

In the composite code representation, the different levels of program control and data dependencies are explicitly encoded into a joint graph of heterogeneous edges with ASTs as the backbone. In contrast to previous models, it helps to capture the types and patterns of vulnerabilities as widely as possible and enables better learning of node representations through graph neural networks.

![截屏2021-08-10 下午11.21.33.png](https://i.loli.net/2021/08/10/D2owRzVtsKkYCfa.png)

In program analysis, various representations of programs are used to show deeper semantics behind textual code, where classical concepts include AST, control flow and data flow graphs, which capture syntactic and semantic relationships between different tokens of the source code. A large number of vulnerabilities, such as memory leaks, are so subtle that they cannot be found without considering compound code semantics. Using ASTs alone can only find insecure parameters. By combining ASTs with control flow graphs, it is possible to cover that type of vulnerability. By further integrating the three code graphs, it is possible to describe the external information needed for most vulnerability types except the two code graphs (i.e., competing conditions and design errors that depend on runtime properties and that are difficult to model without detailing the intended design of the program), in addition to which the authors define a natural code sequence, in programming logic order. It complements the classical representation because its unique flat structure captures the relationships of code tokens in a "human readable" way.


## Ponder

- The code with vulnerabilities is often only a small part of it. The critical lines of code can be proposed by slicing techniques, and then the semantic and structural information of the code can be completed by structural complementation, which can reduce the number of irrelevant codes and improve the accuracy and efficiency of detection.
- Many of the many methods are for a single function of the vulnerability detection, can not be cross-functional or even cross-file vulnerability detection, but the reality of many vulnerabilities are associated with multiple functions.
- For large systems and applications, more than one language may be used, while the server and client are separated, if the simple analysis of one end of the easy to lead to false positives and missed reports, so the cross-language repo vulnerability mining is also a major problem at present.