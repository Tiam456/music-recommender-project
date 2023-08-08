## Project proposal form

Please provide the information requested in the following form. Try provide concise and informative answers.

**1. What is your project title?**  
Spotify Playlist Music Recommendation System

**2. What is the problem that you want to solve?**  
Build a recommender system and song prediction system based on Spotify playlist data. 

**3. What distributed computing for big data methodologies and systems do you plan to use in your project?**  
1) Firstly, we define 2-3 baseline models such as the matrix completion model (tentatively, Bayesian personalised ranking matrix factorization) and the LSA model. 
2) We will compare these baseline models to those slightly advanced and more personalised models we define later. 
3) Of the slightly more advanced models, the first model that we are interested in is the latent factor model (mentioned in McFee et. al. (2012). )
4) The second model of our interest is the clustering approach. This is an unsupervised approach to categorise playlists into multiple classes based on the audio features of the tracks in the playlists. Then, we can build a recommender to suggest new music from another playlist within the same class. (tentatively, we are interested in trying K-means).  
5) (where possible) Notice that we can make the problem into a supervised learning problem. We were thinking to split each playlist into 80/20 and use the rolling window approach to learn the prediction ability. A more advanced model - neural network could be deployed. (a deep fully connected neural network or a hybrid CRNN based model is worth a try).  
6) The above are models we plan to build but are not restricted to. We might make some slight adjustments in terms of the model selection after EDA. 

**4. What dataset will you use? Provide information about the dataset, and a url for the dataset if available. Briefly discuss suitability of the dataset for distributed computing for big data.**  
1) [Spotify Million Playlist Dataset](https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge)
2) [Spotify Audio Features](https://www.kaggle.com/datasets/tomigelo/spotify-audio-features)
4) The size of the dataset is roughly 5gb and is stored in json file format. Due to the cost of uploading 5gb of data onto GCP, we aim to reduce the size of the original data by at least 50% depending on the computation time during our experimentation. Tentatively, this would be done through random sampling. 
Spotify audio features dataset consists of information about the features of each track, the features are acorsticness, danceability, energy, instrumentalness, liveness, duration of the track and number of keys. 
5) We believe the dataset is suitable for the context of distributed computing for big data as the dataset is big and complicated. In particular, every playlist has different length of tracks and for each track in the playlist we have its audio attributes and there are a million of such playlist(if we are going to analyse all of them).   

**5. List key references (e.g. research papers) that your project will be based on?** (please cite them properly and provide URLs)  
1) Brian McFee, Thierry Bertin-Mahieux, Daniel P.W. Ellis, and Gert R.G. Lanckriet. 2012. The million song dataset challenge. In Proceedings of the 21st International Conference on World Wide Web (WWW '12 Companion). Association for Computing Machinery, New York, NY, USA, 909–916. https://doi.org/10.1145/2187980.2188222
2) Ching-Wei Chen, Paul Lamere, Markus Schedl, and Hamed Zamani. 2018. Recsys challenge 2018: automatic music playlist continuation. In Proceedings of the 12th ACM Conference on Recommender Systems (RecSys '18). Association for Computing Machinery, New York, NY, USA, 527–528. https://doi.org/10.1145/3240323.3240342
3) Xiangnan He, Lizi Liao, Hanwang Zhang, Liqiang Nie, Xia Hu, and Tat-Seng Chua. 2017. Neural Collaborative Filtering. In Proceedings of the 26th International Conference on World Wide Web (WWW '17). International World Wide Web Conferences Steering Committee, Republic and Canton of Geneva, CHE, 173–182. https://doi.org/10.1145/3038912.3052569
4) Kowald, Dominik & Müllner, Peter & Zangerle, Eva & Bauer, Christine & Schedl, Markus & Lex, Elisabeth. (2021). Support the underground: characteristics of beyond-mainstream music listeners. EPJ Data Science. 10. 10.1140/epjds/s13688-021-00268-9. https://epjdatascience.springeropen.com/articles/10.1140/epjds/s13688-021-00268-9
5) https://medium.com/@david.de.hernandez/modeling-data-for-a-spotify-recommender-system-3056997a0fc5  
**Please indicate whether your project proposal is ready for review (Yes/No):**  
Yes

## Feedback (to be provided by the lecturer)

[MV 31st March 2023] Project topic approved. The general problem of music recommender system design sounds interesting. It is good to see that you have identified several references, some publishied in WWW and RecSys conference proceedings which are relevant publication venues. When testing different methods you may indeed use a sample of data. For final results, you may want to try using as much data as you can. A raw data size of 5GB is relatively not large -- compared to a RAM size of a modern laptop. You may want to focus on a few recommender system methods for which you would be able to demonstrate your knowledge in distributed computing topics covered in the course. For the choice of recommender system methods, you may focus on some state of the art methods, e.g. some can be found here https://github.com/microsoft/recommenders, and have a focus on a few methods. You want want to demonstrate computation time performance benefits when running your computations on clusters with different number of worker nodes. 
