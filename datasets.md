---
layout: archive
title: datasets
permalink: /datasets/
---
## Dataset
---

### Attribution Graphs

| Name  | Type      | #nodes    | #edges | #attributes  | #labels | URL       | 
|-------  |---------  |---------  |---------|-----------  |---------  |---------  |
|Cora | directed|2,708|5,429|1,433| 7| [[raw]](https://linqs.soe.ucsc.edu/data)|
|Citeseer| directed|3,327|4,732|3,703| 6| [[raw]](https://linqs.soe.ucsc.edu/data)|
|Pubmed| directed|19,717|44,338|500| 3| [[raw]](https://linqs.soe.ucsc.edu/data) |
|BlogCatalog| undirected|5,196|343,486| 8,189| 6| [[raw]](https://github.com/mengzaiqiao/CAN/tree/master/data) |
|PPI| undirected|56,944|81,8716|50| 121| [[raw]](https://snap.stanford.edu/graphsage/) |
|Flickr| undirected|7,575|47,9476|12,047| 9| [[raw]](https://github.com/mengzaiqiao/CAN/tree/master/data) |
|Reddit| undirected|  232,965 |  11,606,919 | 602 | 41 | [[raw]](https://drive.google.com/drive/folders/1zycmmDES39zVlbVCYs88JTJ1Wm5FbfLz) |
|Ogbn-ArXiv| undirected| 169,343 | 1,157,799 | 128 | 40 | [[raw]](https://drive.google.com/drive/folders/1zycmmDES39zVlbVCYs88JTJ1Wm5FbfLz) |

<!--
|Facebook| undirected|4039|88234|1283| 193| [[raw]](https://snap.stanford.edu/data/ego-Facebook.html) |
|Yelp| undirected|  716847 | 6,977,410 | 300 | 100 | [[raw]](https://drive.google.com/drive/folders/1zycmmDES39zVlbVCYs88JTJ1Wm5FbfLz)|
|Twitter| directed|81306|1768149|216839| 4065| [[raw]](https://snap.stanford.edu/data/ego-Twitter.html)|
|Amazon2M| undirected| 2449029 | 61859140 | 100 | 47 | [[raw]](https://github.com/google-research/google-research/tree/master/cluster_gcn) [[raw]](https://ogb.stanford.edu/docs/nodeprop/#ogbn-products) |
|Google+| directed|107614|13673453|15907| 468| [[raw]](https://snap.stanford.edu/data/ego-Gplus.html) |
|TWeibo| directed| 2320895| 50655143| 1657| 8| [[raw]](https://www.kaggle.com/c/kddcup2012-track1) |
|MAG| directed| 59249719| 978147253| 2000| 100| [[raw]](http://ma-graph.org/rdf-dumps/) |
|MAG-SC| directed|10541560| 265219994 |2784240 | 8 | [[raw]](https://figshare.com/articles/dataset/mag_scholar/12696653)|
|Wiki |directed|2405|17981|4973| 19| [[raw]](https://github.com/thunlp/TADW/tree/master/wiki)|
!-->

These datasets are also available in [Pytorch-Geometric](https://pytorch-geometric.readthedocs.io/en/latest/modules/datasets.html#torch_geometric.datasets.AttributedGraphDataset). Node attributes can be loaded as a sparse matrix using the following code
```python
from scipy import sparse
features = sparse.load_npz("attrs.npz")
```



### Simple Graphs 

| Name    | #nodes    | #edges    | #labels | Type        | URL       | 
|-------  |---------  |---------  |---------|-----------  |---------  |
| com-Amazon |  334,863 |  925,872  |   151,037    | undirected  | [[raw]](https://snap.stanford.edu/data/com-Amazon.html) | 
| com-DBLP | 317,080  |  1,049,866  |   13,477    | undirected  | [[raw]](https://snap.stanford.edu/data/com-DBLP.html) | 
| com-Youtube | 1,134,890   | 2,987,624   | 8,385      | undirected  | [[raw]](https://snap.stanford.edu/data/com-Youtube.html) | 
|com-LiveJournal  | 3,997,962 | 34,681,189 |  287,512   |  undirected  |  [[raw]](https://snap.stanford.edu/data/com-LiveJournal.html)         | 
| com-Orkut   | 3,072,441   | 117,185,083 | 6,288,363    | undirected  | [[raw]](https://snap.stanford.edu/data/com-Orkut.html) |
|com-Friendster | 65,608,366  | 1,806,067,135 |   957,154  |  undirected  | [[raw]](https://snap.stanford.edu/data/com-Friendster.html)|
|com-Friendster-small | 7,944,949  | 447,219,610 |  100  |  undirected  | [[raw]](https://snap.stanford.edu/data/com-Friendster.html) [[raw]](https://graphvite.io/docs/latest/api/dataset.html)  |
|Pokec    | 1,632,803 | 30,622,564|    -    |   directed  |  [[raw]](https://snap.stanford.edu/data/soc-Pokec.html)        | 
|Twitter  | 41,652,230  | 1,468,365,182|    -    | directed    | [[raw]](http://law.di.unimi.it/webdata/twitter-2010/) |
|LiveJournal  | 4,847,571 | 68,475,391 |  -    |  directed  |  [[raw]](https://snap.stanford.edu/data/soc-LiveJournal1.html)          | 


<!--
| PPI |  3,890  |   76,584 | 50  | undirected  | [[raw]](https://github.com/xptree/LightNE) [[raw]](http://snap.stanford.edu/node2vec/) | 
| Blogcatalog3 |  10,312  |  333,983   | 39  | undirected  | [[raw]](https://github.com/xptree/LightNE) [[raw]](http://leitang.net/code/social-dimension/data/blogcatalog.mat) | 
| Flickr |  80,513 |  5,899,882  |   195    | undirected  | [[raw]](https://github.com/xptree/LightNE) [[raw]](http://leitang.net/code/social-dimension/data/flickr.mat) | 
| TWeibo  | 2,320,895   | 50,655,143  | 100     | directed    | [[raw]](https://www.kaggle.com/c/kddcup2012-track1) |
|In-2004  | 1,382,908 | 16,539,643|    -    |   directed  |  [[raw]](http://law.di.unimi.it/webdata/in-2004/)   | 
|DBLP     | 5,425,963 | 17,298,032|    -    |   undirected|  [[raw]](http://konect.uni-koblenz.de/networks/dblp-author)         | 
|IT-2004  | 41,291,594  | 1,135,718,909  |   -      |  directed  |  [[raw]](http://law.di.unimi.it/webdata/it-2004/) | 
|OAG | 67,768,244  | 895,368,962 |   19  |  undirected  | [[raw]](https://github.com/xptree/LightNE)  |
|UK-2007 | 105,896,555 | 3,738,733,648|    -    |   directed  |  [[raw]](http://law.di.unimi.it/webdata/uk-2007-05/)    | 
|UK-union | 133,633,040 | 5,475,109,924|    -    |   directed  |  [[raw]](http://law.di.unimi.it/webdata/uk-union-2006-06-2007-05/)     | 
|ClueWeb12| 978,408,098 | 42,574,107,469 | - | directed | [[raw]](http://law.di.unimi.it/webdata/clueweb12/) |
|ClueWeb09| 1,684,868,322| 7,939,635,651|    -    |  directed  |   [[raw]](http://www.lemurproject.org/clueweb09.php/)       | 
!-->



<!--

### Bipartite Graphs (http://konect.cc/)


| Name    |     \|U\|   |    \|V\|    |   \|E\|   | URL       | 
|-------  |---------  |---------  |---------|---------  |
|  Avito  |  27736    |  16589    | 67029   |[[raw]](https://www.kaggle.com/c/avito-context-ad-clicks/data)  |
|  AOL    |   4811647 |  1632788  | 10741954|[[raw]](http://www.ccc.ipt.pt/~ricardo/experiments/AOL_DS.html)  |
|  DBLP   |  6001     |  1524     |  29257  |[[raw]](https://github.com/clhchtcjj/BiNE/tree/master/data/dblp) |
|  Movielens-1M  |   6040        |   3706        |  1000210 |[[raw]](https://grouplens.org/datasets/movielens/) |
|  KDDCup2012  |  255170  | 1848114  | 2766394 |[[raw]](https://www.kaggle.com/c/kddcup2012-track2) |
|  Last.fm     | 359349  |  160168  | 17559531 |[[raw]](http://ocelma.net/MusicRecommendationDataset/lastfm-360K.html)  |
|  Amazon-games | 826767  |  50210 | 1324754 |[[raw]](http://deepyeti.ucsd.edu/jianmo/amazon/)  |
|  DBLP    | 6,001  | 1,308 | 29,256  | [[raw]](https://github.com/clhchtcjj/BiNE/tree/master/data/dblp) |
| Wikipedia     | 15,000  |  3,214 | 64,095  | [[raw]](https://github.com/clhchtcjj/BiNE/tree/master/data/wiki)  |
|   Pinterest   | 55,187  | 9,916  | 1,500,809  | [[raw]](https://github.com/hexiangnan/neural_collaborative_filtering/tree/master/Data) |
|   Yelp   |  31,668 | 38,048  | 1,561,406  | [[raw]](https://github.com/kuandeng/LightGCN/tree/master/Data/yelp2018) |
|  MovieLens-10M    |  69,878 | 10,677  |  10,000,054 | [[raw]](https://grouplens.org/datasets/movielens/)  |
|  Last.fm    | 359,349  | 160,168  | 17,559,530 | [[raw]](http://ocelma.net/MusicRecommendationDataset/lastfm-360K.html) |
|   MIND   | 876,956  | 97,509  | 18,149,915  | [[raw]](https://msnews.github.io/)  |
|  Netflix    | 480,189  | 17,770  | 100,480,507  | [[raw]](https://academictorrents.com/details/9b13183dc4d60676b773c9e2cd6de5e5542cee9a)|
|   Orkut   | 2,783,196  | 8,730,857  | 327,037,487  | [[raw]](https://networkrepository.com/aff-orkut-user2groups.php) |
|  MAG    | 10,541,560  | 2,784,240  |  1,095,315,106 | [[raw]](https://figshare.com/articles/dataset/mag_scholar/12696653) |





### Temporal Graphs
http://konect.cc/

http://www.sociopatterns.org/

https://snap.stanford.edu/

!-->



## Dataset Repositories

| Name                                                                                       | Type                                   | Collected by             |
|--------------------------------------------------------------------------------------------|----------------------------------------|--------------------------|
|[SNAP](http://snap.stanford.edu/data/index.html)                                            |Graphs & Networks                       | Stanford                 |
|[KONECT](http://konect.cc/networks/)                                                        |Graphs & Networks                       | Jérôme Kunegis           |
|[Aminer](https://www.aminer.cn/data/) [Aminer](https://www.aminer.cn/data_cn)               |Academic Networks                       | AMiner                   |


<!--
|[LAW](http://law.di.unimi.it/datasets.php)                                                  |Graphs & Networks                       | UNIMI                    |
|[BioSNAP](http://snap.stanford.edu/biodata/index.html)                                      |Biomedical Networks                     | Stanford                 |


|[UCI Network Data Repository](https://networkdata.ics.uci.edu/)                             |Graphs & Networks                       | UCI Datalab               |
|[Network Repository](https://networkrepository.com)                                         |Graphs & Networks                       | -                         |
|[Open Academic Graph](https://www.microsoft.com/en-us/research/project/open-academic-graph/)|Academic Networks                       | Microsoft                |
|[Open Graph Benchmark](https://ogb.stanford.edu/)                                           |Graphs & Networks                       | Stanford                 |
|[TuDatasets](https://chrsmrrs.github.io/datasets/)                                          |Graphs & Networks                       | Christopher Morris, etc. |
|[StreamingGraphs](https://eecs.wsu.edu/~yyao/StreamingGraphs.html)                          |Streaming Graphs                        | Yibo Yao                 |
|[ARB](https://www.cs.cornell.edu/~arb/data/)                                                |Graphs & Networks                       | Austin R. Benson         |
|[SuiteSparse Matrix Collection](https://sparse.tamu.edu/)                                   |Matrix/Graphs                           | TAMU                     |
|[Web Data Commons](http://webdatacommons.org/)                                              |Hyperlink Graphs/Web Tables/RDFa        | University of Mannheim   |
|[Yahoo Webscope Datasets](https://webscope.sandbox.yahoo.com/#datasets)                     |Graphs/Ratings/Languages/Advertising    | Yahoo                    |
|[UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets.php)              |Multivariate/Text/Time-Series           | UCI                      |
|[Yelp Open Dataset](https://www.yelp.com/dataset)                                           |businesses/reviews/user data            | Yelp                     |
|[Recommender Systems Datasets](https://cseweb.ucsd.edu/~jmcauley/datasets.html)             |graphs/interactions/reviews/ratings     | UCSD                     |
|[MIcrosoft News Dataset](https://msnews.github.io/)                                         |user behavior logs                      | Microsoft                |
|[Search Query Logs](https://jeffhuang.com/search_query_logs/)                               |query logs                              | Jeff Huang               |
|[AOL DS](http://www.ccc.ipt.pt/~ricardo/experiments/AOL_DS.html)                            |query logs                              | Ricardo Campos           |
|[AWS](https://registry.opendata.aws/)                            |-                             | Amazon           |
|[Kaggle Datasets](https://www.kaggle.com/datasets)                            |-                             | Kaggle           |
|[OpenML](https://www.openml.org/search?type=data&sort=runs&status=active) | - | OpenML |
|[Datasets](https://courses.cs.washington.edu/courses/cse547/19sp/data.html) | - | - |
|[Netzschleuder](https://networks.skewed.de/) | - | - |

!-->
