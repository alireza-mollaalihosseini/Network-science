# Twitter Word Networks – Måneskin and Eurovision 2021

Course project for *Network Science* (M.Sc. Physics of Data, University of Padova, 2021). Tweets about
the band Måneskin, winners of the Eurovision Song Contest on 22 May 2021, are turned into word
co-occurrence networks, to see how the conversation changed before, during and after the contest.

## Notebooks

| Notebook | Contents |
|---|---|
| `Tweet_API(2).ipynb` | Course lab notebook for collecting tweets with the Twitter API v2 search endpoint (bearer token from an environment variable), converting them to DataFrames and saving them as CSV, pickle or parquet |
| `Tweets.ipynb` | The analysis below |

## Analysis (`Tweets.ipynb`)

1. **Periods:** tweets (with LIWC scores) split into four weekly windows: before 17 May, the Eurovision
   week, the week after the final, and after 31 May 2021.
2. **Cleaning:** mentions, hashtags and links removed, English stop words dropped, lemmatisation with
   WordNet and part-of-speech tags (NLTK).
3. **Networks:** word frequencies and weighted co-occurrence networks per period (networkx), exported as
   Gephi edge and node lists.
4. **Network metrics** (python-igraph): order, size, density, connected components, diameter, average
   path length, global and local clustering, and cliques.

The tweet data (`maneskin_liwc.csv`) is not included.
