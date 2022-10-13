# Social-network-analysis-on-Disney-films

The aim of this capstone project was to analyse the character network in Walt Disney films in the context of gender inequality. Datasets used are film transcript data of 26 Disney Princess and Pixar films. In social network analysis approach, three different methods were used. First, network plots of the character network in each film are shown to understand the networks, focusing on the gender of each character from each film. Second, three different centrality metrics are computed to identify important characters. Finally, `ergm` models are used to determine whether gender plays a role in the number of words spoken. 

## 1. Datasets 
|  No   |  Film     |  Release Year |  
| :---: |    :---:    |    :----:   |
|  1    | Snow White and the Seven Dwarfs      |  1937   |
|  2    | Cinderella   | 1950    |  
|  3    | Sleeping Beauty     |  1959    | 
|  4    | Little Mermaid   | 1989   |   
|  5    | Beauty and the Beast      |  1991 |  
|  6    | Aladdin   | 1992   | 
|  7    | Pocahontas   | 1995     | 
|  8    | Toy Story 1   | 1995     | 
|  9    | Mulan   | 1998   | 
|  10    | Toy Story 2   | 1999     | 
|  11    | Little Mermaid 2   | 2000   | 
|  12    | Finding Nemo   | 2003  | 
|  13    | Incredibles   |   2004   | 
|  14    | The Princess and the Frog   |   2009   | 
|  15    | Toy Story 3 |   2010   | 
|  16    | Tangled   |   2010   | 
|  17    | Brave   |   2012   | 
|  18    | Frozen   |   2013   | 
|  19    |  Inside Out  |   2015   | 
|  20    | Moana   |   2016  | 
|  21    | Beauty and the Beast (Live-action)   |   2017   | 
|  22    | Incredibles 2   |   2018   | 
|  23    | Aladdin (Live-action)   |   2019   | 
|  24    | Frozen 2   |   2019  | 
|  25    | Toy Story 4   |   2019   | 
|  26    | Raya and the Last Dragon   |   2021   | 


## 2. Methods
The final directed dialogue dataset had four columns: `from`, `text`, `directed`, and `to`. 

* `from` : the character who is speaking the dialogue
* `to` : the character who the dialogue is spoken to, but only if the dialogue is directed. 
  * If it was the same character with different voice actors (e.g., when a character was young and then becomes an adult), or the same character who looks differently (e.g., when the Beast turns into a human), they were still seen as one unique character. 
* `textt : the line of dialogue
* `directed` : a binary variable of whether or not the dialogue is directed to a specific character

For exploratory data analysis, this project used network plots that showed how each character interacts with one another based on dialogue relationships. The gender of the character was color coded and the extent of each dialogue relationsihp between two characters were weighted by edge width. Next, three centrality metrics were computed: in- and out-degree, betweenness, and closeness centrality. These measures are typically used in social network analysis to identify influential nodes. The aggregated and average values of each centrality were grouped by each gender for each film. Finally, exponential random graph models (ERGM) were fitted to determine whether gender plays a role in having a dialogue relationshup or not. 
