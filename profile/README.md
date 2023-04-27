## Hi there 👋

实验室主要从事“以人为中心的计算”的跨学科前沿研究，主要包含协同信息与系统和智能人机交互两大方向。采用计算机科学与社会科学互动融合的方法，将信息技术从机器回归聚焦于人（用户）本身，整合“芯片敏捷设计-区块链网络-群智社区-通用智能服务”，旨在打造以人为中心的智能服务。


# 1. Human-Centered Recommender Systems

## 1.1 Candidate Item Matching

### Collaborative Filtering

1. **Personalized Graph Signal Processing for Collaborative Filtering.  WWW 2023. [[paper](https://arxiv.org/abs/2210.08189)], [[code](https://github.com/FudanCISL/FreeGEM)].**

   The collaborative filtering (CF) problem with only user-item interaction information can be solved by graph signal processing (GSP), which uses low-pass filters to smooth the observed interaction signals on the similarity graph to obtain the prediction signals. However, the interaction signal may not be sufficient to accurately characterize user interests and the low-pass filters may ignore the useful information contained in the high-frequency component of the observed signals, resulting in suboptimal accuracy. To this end, we propose a personalized graph signal processing (PGSP) method for collaborative filtering. Firstly, we design the personalized graph signal containing richer user information and construct an augmented similarity graph containing more graph topology information, to more effectively characterize user interests. Secondly, we devise a mixed-frequency graph filter to introduce useful information in the high-frequency components of the observed signals by combining an ideal low-pass filter that smooths signals globally and a linear low-pass filter that smooths signals locally. Finally, we combine the personalized graph signal, the augmented similarity graph and the mixed-frequency graph filter by proposing a pipeline consisting of three key steps: pre-processing, graph convolution and post-processing. Extensive experiments show that PGSP can achieve superior accuracy compared with state-of-the-art CF methods and, as a nonparametric method, PGSP has very high training efficiency.

### Dynamic Graph

1. **FIRE: Fast Incremental Recommendation with Graph Signal Processing. WWW 2022. [[code](https://github.com/FudanCISL/FIRE)].**

   Recommender systems are incremental in nature. Recent progresses in incremental recommendation rely on capturing the temporal dynamics of users/items from temporal interaction graphs, so that their user/item embeddings can evolve together with the graph structures. However, these methods are faced with two key challenges: 1) model training and/or updating are time-consuming and 2) new users/items cannot be effectively handled. To this end, we propose the fast incremental recommendation (FIRE) method from a graph signal processing perspective. FIRE is non-parametric which does not suffer from the time-consuming back-propagations as in previous learning-based methods, significantly improving the efficiency of model updating. In addition, we encode user/item temporal information and side information by designing new graph filters in FIRE, which can capture the temporal dynamics of users/items and address the cold-start issue for new users/items, respectively. Experimental studies on four popular datasets demonstrate that FIRE can improve the accuracy by a large margin and improve the model updating efficiency by at least 3X compared with the state-of-the-art incremental recommendation algorithms. The Code is available at https://github.com/Yaveng/FIRE.

2. **Parameter-free Dynamic Graph Embedding for Link Prediction. NeurIPS 2022. [[paper](https://arxiv.org/abs/2210.08189)], [[code](https://github.com/FudanCISL/FreeGEM)].**

   Dynamic interaction graphs have been widely adopted to model the evolution of user-item interactions over time. There are two crucial factors when modelling user preferences for link prediction in dynamic interaction graphs: 1) collaborative relationship among users and 2) user personalized interaction patterns. Existing methods often implicitly consider these two factors together, which may lead to noisy user modelling when the two factors diverge. In addition, they usually require time-consuming parameter learning with back-propagation, which is prohibitive for real-time user preference modelling. To this end, this paper proposes FreeGEM, a parameter-free dynamic graph embedding method for link prediction. Firstly, to take advantage of the collaborative relationships, we propose an incremental graph embedding engine to obtain user/item embeddings, which is an Online-Monitor-Offline architecture consisting of an Online module to approximately embed users/items over time, a Monitor module to estimate the approximation error in real time and an Offline module to calibrate the user/item embeddings when the online approximation errors exceed a threshold. Meanwhile, we integrate attribute information into the model, which enables FreeGEM to better model users belonging to some under represented groups. Secondly, we design a personalized dynamic interaction pattern modeller, which combines dynamic time decay with attention mechanism to model user short-term interests. Experimental results on two link prediction tasks show that FreeGEM can outperform the state-of-the-art methods in accuracy while achieving over 36X improvement in efficiency. All code and datasets can be found in https://github.com/FudanCISL/FreeGEM.

3. **Triple Structural Information Modeling for Accurate, Explainable and Interactive Recommendation. SIGIR 2023. [[paper](https://arxiv.org/abs/2210.08189)], [[code](https://github.com/FudanCISL/FreeGEM)].**

   In dynamic interaction graphs, user-item interactions usually follow heterogeneous patterns, represented by different structural information, such as user-item co-occurrence, sequential information of user interactions and the transition probabilities of item pairs. However, the existing methods cannot simultaneously leverage all three structural information, resulting in suboptimal performance. To this end, we propose TriSIM4Rec, a triple structural information modeling method for accurate, explainable and interactive recommendation on dynamic interaction graphs. Specifically, TriSIM4Rec consists of 1) a dynamic ideal low-pass graph filter to dynamically mine co-occurrence information in user-item interactions, which is implemented by incremental singular value decomposition (SVD); 2) a parameter-free attention module to capture sequential information of user interactions effectively and efficiently; and 3) an item transition matrix to store the transition probabilities of item pairs. Then, we fuse the predictions from the triple structural information sources to obtain the final recommendation results. By analyzing the relationship between the SVD-based and the recently emerging graph signal processing (GSP)-based collaborative filtering methods, we find that the essence of SVD is an ideal low-pass graph filter, so that the interest vector space in TriSIM4Rec can be extended to achieve explainable and interactive recommendation, making it possible for users to actively break through the information cocoons. Experiments on six public datasets demonstrated the effectiveness of TriSIM4Rec in accuracy, explainability and interactivity.

## 1.2 CTR Prediction

1. **CL4CTR: A Contrastive Learning Framework for CTR Prediction. WSDM 2023. [[code](https://github.com/FudanCISL/CL4CTR)].**
2. **Enhancing CTR Prediction with Context-Aware Feature Representation Learning. SIGIR 2022. [[paper](https://dl.acm.org/doi/abs/10.1145/3477495.3531970)]. [[code](https://github.com/FudanCISL/FRNet)]**
3. **MMCRF: Enhancing CTR Prediction Models via Multi-Channel Feature Refinement Framework. DASFAA 2022. [[paper](https://www.researchgate.net/profile/Fangye-Wang/publication/360216390_MCRF_Enhancing_CTR_Prediction_Models_via_Multi-Channel_Feature_Refinement_Framework/links/6268d291bca601538b6bfae9/MCRF-Enhancing-CTR-Prediction-Models-via-Multi-Channel-Feature-Refinement-Framework.pdf)]**

# 2. Computer Supported Cooperative Work and Social Computing

## 2.1 Human-Centered Text Processing

### Machine Translation

1. **Building  User-oriented Machine Translator based on User-generated Textual Content. CSCW 2022. [[paper](https://dl.acm.org/doi/pdf/10.1145/3555171)].**

### Social Media Textual Content Censorship

1. **Building a Personalized Model for Social Media Textual Content Censorship. CSCW 2022. [[paper](https://dl.acm.org/doi/abs/10.1145/3555657)].**

