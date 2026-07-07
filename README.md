This repository contains 13 networks.
In each folder, there are two files:
- out_graph.txt contains an edgelist.

- out_community.txt contains the attributes:  
Attributes are reported as node_id - attribute couples  
Attributes are either 0 or 1, and 1 is the mathematical minority

escorts folder contains the information only for the giant component of the network.  

A more detailed description of the datasets is reported below.

## [BLOGS](https://dl.acm.org/doi/10.1145/1134271.1134277)
This is a directed network of hyperlinks between weblogs on US politics during the 2004 election.
The directed link among two nodes is added if one blog references another.
Weblogs are labelled as liberal or conservative both by self-reported membership and by the Democratic and Republican parties' notice of the established position of blogs in political discourse.
The adjusted nominal assortativity coefficient denotes that the two communities are extremely segregated.

## [DBLP SPYROS & DBLP COURSE](https://github.com/SotirisTsioutsiouliklis/FairLaR)

Both these networks are subsamples of the DBLP AMINER dataset, hence the detailed description will be discussed further (see Section: DBLP AMINER).

## [SEXUAL CONTACTS](https://www.pnas.org/doi/full/10.1073/pnas.0914080107)

The network is reconstructed from an online Brazilian forum for the sale of sexual services.
The forum is oriented toward heterosexual males, for this reason, nodes are divided into female sex sellers and male sex buyers.
This also implies that this network is completely disassortative, as shown by the $r^*$ in Table 1, hence the graph is bipartite.
This is also the only disconnected graph, divided into 418 components.
Below are reported the main characteristics of the whole network and of its giant component. 

| | $N$ | $L$ | $\langle k \rangle$ | $P_m^*$ | $r^*$ | $r_{deg}$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Network | 16730 | 39044 | 4.668 | 0.39 | -1.0 | -0.11 |
| Giant component | 15810 | 38540 | 4.875 | 0.39 | -1.0 | -0.12 |


## [TWITTER](https://ojs.aaai.org/index.php/ICWSM/article/view/14126)

This is a retweet network where nodes represent users' tweets from the six weeks leading up to the 2010 U.S congressional midterm elections.
A directed link is added among users $i$ and $j$ if $j$ retweets content originally broadcast by $i$. The label assigned divides between left- and right-leaning users.
Communities were created via label propagation.
Then two annotators assigned the political left/right attribute to 1000 random users.
The attributes were highly correlated with the community labels and thus all community members were assigned the same left/right attribute.
The adjusted nominal assortativity coefficient suggests a high level of segregation between the two communities (see Table 1).

## [BRAZIL](https://link.springer.com/article/10.1140/epjds/s13688-019-0213-9)

This is a mention network about the impeachment of Dilma Roussef (tweets were collected from March 5th to December 31st 2016).
A directed link from node $i$ to node $j$ exists if user $i$ sends a tweet mentioning user $j$.
For each link, a classification is provided based on the sentiment regarding the impeachment (pro-, anti-impeachment or neutral).
To binary classify the users, we established that a node belongs to a category if more than half of its outgoing links belong to that category.
In this process, we dropped the nodes for which the outgoing links pro- and anti-impeachment are in the same number.
Such nodes consist of the 0.0393% of the users, so the change in network structure is negligible.
The adjusted nominal assortativity coefficient indicates significant separation between the two groups.

## [PHYSICS](https://dl.acm.org/doi/10.1145/980972.980992)

This is a citation network built on the Arxiv high-energy physics phenomenology.
If a paper $i$ cites paper $j$, the graph contains a directed edge from $i$ to $j$.
If a paper cites, or is cited by, a paper outside the dataset, the graph does not contain any information about this.
The data covers papers in the period from January 1993 to April 2003 (124 months).
The node labels are provided by [Tsioutsiouliklis et al.](https://dl.acm.org/doi/10.1145/3442381.3450065).

## [DBLP AMINER](https://arxiv.org/abs/1704.05801)

This is an author collaboration network constructed by the Arnetminer academic search system using publication data from [dblp](https://dblp.org/).
Two authors are connected if they have co-authored an article.

## ABORTION, ELECTION, VP_DEBATE, SECOND_DEBATE, GUN_CONTROL
Descriptions of these networks can be found in [Hohmann et al.](https://www.science.org/doi/full/10.1126/sciadv.abq2044).
