**Project group 16: Spotify Playlist Music Recommendation System**

**Candidate numbers: 48119, 52240, 55974**

In the report “Spotify Playlist Music Recommendation System” a method based on computing similarity scores and a neural collaborative filtering method is considered for making recommendations in the context of Spotify music items.

The introduction could have better formulated the problem. First a method for computing similarity scores is discussed and then some neural collaborative filtering method. For the former method, it is based on the method in [10] and the goal is clear. For the latter method, the goal is clearly described.

The methodology is described in Section 3, Methodology. The DIMSUM algorithm is described in Section 3.1. Specifically, the algorithm is defined by map and reduce functions shown in Algorithm 1 and Algorithm 2, respectively. The neural collaborative filtering algorithm is described in Section 3.2, which involves describing a neural network architecture.

The code is available in several Jupyter notebooks. The code uses both PySpark and TensorFlow. DIMSUM model.ipynb contains some errors and warnings output messages.

The dataset is described in Section 1.1. The dataset contains information about 50,000 playlists and is of total size of 1.6GB. The dataset is of moderate size.

The numerical results are presented in Section 4. For the neural collaborative filtering evaluation, computations were performed on a cluster with one master and two worker nodes, while for DIMSUM a cluster with one master node and four worker nodes was used. For the neural collaborative filtering, training loss versus number of epochs is shown for different latent dimensions and different MLP layers in Figure 5. Some other evaluation metrics are considered as well such as NDCG. Some non monotonicity in performance with respect to the number of worker nodes is observed in Figure 10 which is puzzling.

The conclusion section summarises what methods are considered in the report. Some points made in the discussion of limitations of the study, e.g. referring to some “models in the industry that outperform traditional algorithm” without saying what are these methods.

The presentation has some good elements, e.g. in terms of providing pseudo-code, and data visualisations. However, there are some shortcomings. Figures miss captions. The report uses captions and footnotes for mathematical displays which is not standard.

Overall this report studies two methods in the context of recommender systems, one for computing similarity scores and a collaborative filtering method. Consideration of these two methods appear disconnected. It would have been more coherent if the report was focused on one method or use of different methods in combination. There is some focus on evaluating performance benefits of distributed computing, more for similarity scores than for collaborative filtering.

**Total mark: 62**
