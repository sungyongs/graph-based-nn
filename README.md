# Graph-based Neural Networks
This page is to summarize important materials about *graph-based neural networks* and *relational networks*. If I miss some recent works or anyone wants to recommend other references, please let me know.

## Background
(You can find many materials for deep neural networks in other places. Here, I mainly cover materials about graphs.)
- [Basic Graph Theory](http://data-science-training-xb.com/) by Xavier Bresson
  - Lecture 3 and 16
- [Spectral Graph Theory](http://www.math.ucsd.edu/~fan/research/revised.html) by Fan Chung
- [Graph Signal Processing GSP](https://arxiv.org/abs/1712.00468) by Ortega et al.
  - This paper provide an overview of core ideas in GSP and their connection to conventional digital signal processing.
  - Signal processing is required to understand the convolution in the spectral domain.
- Keywords : graph theory, spectral graph theory, discrete Fourier transform (DFT)

## List of Related Works
- **Early works using graph structure**
  - [A new model for learning in graph domains](http://ieeexplore.ieee.org/document/1555942/)
    - M. Gori, G. Monfardini, F. Scarselli, IJCNN 2005 (**First attempts to generalize neural networks to graphs**)
  - [The graph neural network model](http://ieeexplore.ieee.org/document/4700287/)
    - F. Scarselli, M. Gori, A. C. Tsoi, M. Hagenbuchner, and G. Monfardini, IEEE Trans. Neural Networks 2009
  - These works optimized over the parameterized steady state of some diffusion process (or random walk) on the graph.
- **Review paper** (*highly recommend*)
  - [Geometric deep learning: going beyond Euclidean data](https://arxiv.org/abs/1611.08097)
    - Michael M. Bronstein, Joan Bruna, Yann LeCun, Arthur Szlam, Pierre Vandergheynst, IEEE Signal Processing Magazine 2017 
    - **First review paper of geometric deep learning**
  
- **Graph Convolutional Networks (GCNs)**
  - [Spectral Networks and Locally Connected Networks on Graphs](https://arxiv.org/abs/1312.6203)
    - Joan Bruna, Wojciech Zaremba, Arthur Szlam, Yann LeCun, ICLR 2014
    - **First formulation of CNNs on graphs in the spectral domain**
  - [Deep Convolutional Networks on Graph-Structured Data](https://arxiv.org/abs/1506.05163)
    - Mikael Henaff, Joan Bruna, Yann LeCun, 2015
    - **Spatial localization of smooth filters in the frequency domain**
  - [Convolutional Networks on Graphs for Learning Molecular Fingerprints](http://papers.nips.cc/paper/5954-convolutional-networks-on-graphs-for-learning-molecular-fingerprints)
    - David Duvenaud, Dougal Maclaurin, Jorge Iparraguirre, Rafael Bombarell, Timothy Hirzel, Alan Aspuru-Guzik, Ryan P. Adams, NIPS 2015
  - [Gated Graph Sequence Neural Networks](https://arxiv.org/abs/1511.05493)
    - Yujia Li, Daniel Tarlow, Marc Brockschmidt, Richard Zemel, ICLR 2016
    - **Sliding a filter on the vertices as conventional CNNs, not spectral filtering**
  - [Learning Convolutional Neural Networks for Graphs](https://arxiv.org/abs/1605.05273)
    - Mathias Niepert, Mohamed Ahmed, Konstantin Kutzkov, ICML 2016
  - [Generalizing the Convolution Operator to extend CNNs to Irregular Domains](https://arxiv.org/abs/1606.01166)
    - Jean-Charles Vialatte, Vincent Gripon, Grégoire Mercier, arXiv 2016
    - **Generalize CNNs to irregular domains using weight sharing and graph-based operators**
  - [Convolutional Neural Networks on Graphs with Fast Localized Spectral Filtering](https://arxiv.org/abs/1606.09375), [[PyTorch Code]](https://github.com/xbresson/graph_convnets_pytorch/blob/master/README.md) [[TF Code]](https://github.com/mdeff/cnn_graph)
    - Michaël Defferrard, Xavier Bresson, Pierre Vandergheynst, NIPS 2016
    - **Spectral CNN with Chebychev polynomial filters (ChebNet)**
  - [Learning Shape Correspondence with Anisotropic Convolutional Neural Networks](https://arxiv.org/abs/1605.06437)
    - Davide Boscaini, Jonathan Masci, Emanuele Rodolà, Michael M. Bronstein, NIPS 2016
    - **Anisotropic CNN framework**
  - [Semi-Supervised Classification with Graph Convolutional Networks](https://arxiv.org/abs/1609.02907), [[Code]](https://github.com/tkipf/gcn), [[Blog]](http://tkipf.github.io/graph-convolutional-networks/)
    - Thomas N. Kipf, Max Welling, ICLR 2017
    - **Graph Convolutional Networks (GCN) framework, a simplification of ChebNet**
  - [Geometric Deep Learning on Graphs and Manifolds using Mixture Model CNNs](https://arxiv.org/abs/1611.08402)
    - Federico Monti, Davide Boscaini, Jonathan Masci, Emanuele Rodolà, Jan Svoboda, Michael M. Bronstein, CVPR 2017 
    - **MoNets**
  - [Geometric Matrix Completion with Recurrent Multi-Graph Neural Networks](https://arxiv.org/abs/1704.06803), [[Code]](https://github.com/fmonti/mgcnn)
    - Federico Monti, Michael M. Bronstein, Xavier Bresson, NIPS 2017
    - **Recommendation systems**
  - [CayleyNets: Graph Convolutional Neural Networks with Complex Rational Spectral Filters](https://arxiv.org/abs/1705.07664)
    - Ron Levie, Federico Monti, Xavier Bresson, Michael M. Bronstein, arXiv 2017
    - **Spectral CNN with complex rational filters (CayleyNet)**
  - [Residual Gated Graph ConvNets](https://arxiv.org/abs/1711.07553)
    - Xavier Bresson, Thomas Laurent, arXiv 2017

- Relational Networks (RNs), Relational Reasoning
  - [Interaction networks for learning about objects, relations and physics](https://arxiv.org/abs/1612.00222)
    - Peter W. Battaglia, Razvan Pascanu, Matthew Lai, Danilo Rezende, Koray Kavukcuoglu), NIPS 2016
  - [A simple neural network module for relational reasoning](https://arxiv.org/abs/1706.01427), [[Deepmind Article]](https://deepmind.com/blog/neural-approach-relational-reasoning/), [[Code]](https://github.com/kimhc6028/relational-networks)
    - Adam Santoro, David Raposo, David G.T. Barrett, Mateusz Malinowski, Razvan Pascanu, Peter Battaglia, Timothy Lillicrap, arXiv 2017
    - **Consider all possible pairs**
  - [Neural Message Passing for Quantum Chemistry](https://arxiv.org/abs/1704.01212)
    - Justin Gilmer, Samuel S. Schoenholz, Patrick F. Riley, Oriol Vinyals, George E. Dahl, ICML 2017
  - [Pointnet: Deep learning on point sets for 3d classification and segmentation](https://arxiv.org/abs/1612.00593)
    - Charles R. Qi, Hao Su, Kaichun Mo, Leonidas J. Guibas, CVPR2017
  - [SchNet: A continuous-filter convolutional neural network for modeling quantum interactions](https://arxiv.org/abs/1706.08566)
    - Kristof T. Schütt, Pieter-Jan Kindermans, Huziel E. Sauceda, Stefan Chmiela, Alexandre Tkatchenko, Klaus-Robert Müller, NIPS 2017
  - [VAIN: Attentional Multi-agent Predictive Modeling](http://papers.nips.cc/paper/6863-vain-attentional-multi-agent-predictive-modeling)
    - Yedid Hoshen,  NIPS 2017
  - [Modeling Relational Data with Graph Convolutional Networks](https://arxiv.org/abs/1703.06103)
    - Michael Schlichtkrull, Thomas N. Kipf, Peter Bloem, Rianne van den Berg, Ivan Titov, Max Welling, arXiv 2017
  - [Graph Attention Networks](https://arxiv.org/abs/1710.10903), [[Code]](https://github.com/PetarV-/GAT)
    - Petar Veličković, Guillem Cucurull, Arantxa Casanova, Adriana Romero, Pietro Liò, Yoshua Bengio, ICLR 2018

- Graph Auto-Encoder (GAE)
  - [Variational Graph Auto-Encoders](https://arxiv.org/abs/1611.07308), [[Code]](https://github.com/tkipf/gae)
    - Thomas N. Kipf, Max Welling, NIPS Workshop on Bayesian Deep Learning 2016
    - Question: Why the adjacency matrix is reconstructed rather than the feature matrix?
  - [Modeling Relational Data with Graph Convolutional Networks](https://arxiv.org/abs/1703.06103)
    - Michael Schlichtkrull, Thomas N. Kipf, Peter Bloem, Rianne van den Berg, Ivan Titov, Max Welling, 2017
  - [Graph Convolutional Matrix Completion](https://arxiv.org/abs/1706.02263)
    - Rianne van den Berg, Thomas N. Kipf, Max Welling, 2017
    
- Other Applications using Graph-based Neural Networks
  - [Diffusion Convolutional Recurrent Neural Network: Data-Driven Traffic Forecasting
](https://arxiv.org/abs/1707.01926), [[Code]](https://github.com/liyaguang/DCRNN)
    - Yaguang Li, Rose Yu, Cyrus Shahabi, Yan Liu, ICLR 2018
  - [Automatically Inferring Data Quality for Spatiotemporal Forecasting](https://openreview.net/forum?id=ByJIWUnpW)
    - Sungyong Seo, Arash Mohegh, George Ban-Weiss, Yan Liu, ICLR 2018

## Tutorials or Workshops
- IPAM18 Workshop, [New Deep Learning Techniques](http://www.ipam.ucla.edu/programs/workshops/new-deep-learning-techniques/)
- NIPS17 Tutorial, [Geometric Deep Learning on Graphs and Manifolds](https://nips.cc/Conferences/2017/Schedule?showEvent=8735)
- CVPR17 Tutorial, [Geometric Deep Learning on Graphs](http://geometricdeeplearning.com/)

## Useful Resources
- [Kipf's blog](http://tkipf.github.io/graph-convolutional-networks/)
- [Geometric Deep Learning](http://geometricdeeplearning.com/) **highly recommended**
- [CVPR17 tutorial, Geometric and Semantic 3D Reconstruction](https://www.dropbox.com/s/4l6m32tg9yecvow/CVPR%20GDL.pdf?dl=0), 240MB
- [How do I generalize convolution of neural networks to graphs?](https://www.quora.com/How-do-I-generalize-convolution-of-neural-networks-to-graphs), Defferrard's answers in Quora
- [PointNet](http://stanford.edu/~rqi/pointnet/)


## List of Researchers
- [Thomas Kipf](http://tkipf.github.io/), University of Amsterdam
- [Joan Bruna](http://cims.nyu.edu/~bruna/), NYU
- [Michaël Defferrard](http://deff.ch/), EPFL
- [Xavier Bresson](http://www.ntu.edu.sg/home/xbresson/index.html), NTU
- [Federico Monti](https://www.ics.usi.ch/index.php/people-detail-page/268-federico-monti), Università della Svizzera Italiana
- [Michael M. Bronstein](http://www.inf.usi.ch/bronstein/), Università della Svizzera Italiana
