# Network Analysis - Game of Thrones (ASOIAF)

**WARNING! STATISTICAL SPOILERS AHEAD!**

Network analysis is a big topic in software and in mathematics these days. Probably the most famous network analysis project is the Google search backend. But parsing the entire internet is probably not a great goal for a one-hour project. So let's take look at something a bit smaller.

The Game of Thrones books (and TV series) is almost 5,000 pages long, with hundreds and hundreds of characters. Based on their interactions there are a huge number of connections between these characters. And based on these connections, some of these characters are a lot more important than others. Because the books are so profoundly pluralist, there is no "main character" to any of the books. BUT we can quantify which characters are more "central" to the story, by mapping out all of the connections between them and using the undamped [PageRank algorithm](https://en.wikipedia.org/wiki/PageRank) as a measure of centrality.

NOTE: At the time of this writing there were only five of the expected seven books in the series published. I happen to own electronic copies of all five books, which is where I got the text for this project. For copyright reasons, I will not sure this raw data.

## Methods

The network analysis of the characters in the Game of Thrones (A Song of Ice and Fire) series is caried out by parsing the text in all of the books.

1. The books will be stripped down to only lower case letters with no punctuation.
2. We will find all the character names in the text.
3. Any names that are `X` words apart will have a connection.
4. We will then [PageRank](https://en.wikipedia.org/wiki/PageRank) these connections to determine which characters are more central.
5. We may try several values of `X` to determine which returns more useful results.

## RESULTS

Before getting into the network analysis, we have another clue to character centrality in these books. Each chapter is told in first-person perspective. You will find a quick tally of which characters have the most POV chapters [here](character_povs.ipynb).

TODO
