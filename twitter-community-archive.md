# Twitter Community Archive

This is a project to (1) collect twitter archives from volunteers to study ourselves (2) build open source tools for collection & analysis so that other communities can reproduce this work on their own data. 

I started this project in July 2024 with [Xiq](https://x.com/exgenesis). It currently has 4 million tweets from 187 accounts.

- Project homepage: https://www.community-archive.org/
- GitHub: https://github.com/TheExGenesis/community-archive

<img width="550" alt="image" src="https://github.com/user-attachments/assets/256ed998-669b-412a-998d-cce57dd59ab4" />

### Visualizing the evolution of language over time

App link: https://labs-community-archive.streamlit.app/

This is a "ngram viewer" over the corpus of the collected tweets. It's very useful to see how language unique to a specific community has evolved over time. For example, most of the people in the archive belong to a community called "tpot". But it wasn't always called that. At some point it was called "ingroup", and/or "postrat" (short for post rationalist).

With this kind of tool we could see (1) exactly at what point this name emerged (2) how long it took for it to settle as the official name (3) who was the first person to coin it? 

<img width="450" alt="image" src="https://github.com/user-attachments/assets/0648d909-cfe4-450c-a21c-e07d112e8bf1" />

It would be interesting to recreate the timeline of how it spread. Did a few specific users cause an inflection point in its usage? Can we visualize the first occurrence of it in _each_ user's lexicon? Can we do this with other words in the community's dictionary to identify if there are "thought leaders" who consistently adopt & spread new terms ahead of the curve? Or is this always a diffuse process with no specific leader?

Another interesting example are the words **egregore** and **psychofauna**. They mean the same thing, but `@visakanv` coined the latter [Nov 5 2022](https://x.com/i/web/status/1588796630287147009) as an attempt to create an easier to remember term: 

<img width="450" alt="image" src="https://github.com/user-attachments/assets/36a54ae1-619d-47bb-a8c3-126f98147caf" />

### Lexicon analysis

I created this simple Jupyter notebook as a template: https://colab.research.google.com/drive/109XOgTWj-sajpAYhDCNPfts5zvdkpi_s

I generated the 10 most common bigrams for each user, and asked people on twitter to guess who was who (these are bigrams for users `@eshear, @NathanpmYoung, and @nosilverv`: 

<img width="450" alt="image" src="https://github.com/user-attachments/assets/2f985dbf-0888-4e00-8aba-cfb70714a830" />

It was interesting to see "don't know" appear in almost everyone's top 10 bigrams. My current theory is that this is because this particular community cares a lot about truth & epistemology, and this comes out in the language used, but we'll need a control group to verify this. 

### Personal semantic search

Source code: https://github.com/DefenderOfBasic/twitter-semantic-search

I built a basic semantic search which is very useful for finding tweets & threads by meaning, or that are related to a general topic. Here the query is a paraphrase of a tweet I made & system can find it even if the keywords aren't in the search query:

<img width="350" alt="image" src="https://github.com/user-attachments/assets/b3bc8b01-0e61-44a9-b41c-e56c2a1a2d21" />

This can be the basis of a lot of future work, like automatically finding topics of overlap between two or more users. It can also be used to cluster tweets together and graph them over time, to see how the ideas & themes in each person's writing have evolved over time:

<img width="550" alt="image" src="https://github.com/user-attachments/assets/ef58b1e2-bda8-4105-9438-1dc2bc15b378" />

### Future work

The general areas of focus are (1) coordination and (2) sense making. When new discourse flares up, I want to know the history of it & how we got here. When I meet someone new, I want to know how much our beliefs & values overlap. Tools that make my writing legible & searchable help me find others who are aligned with my work.

Some specific ideas:

- A chrome extension that scrapes tweets as I view them and adds them to the open database, will give us a "twitter firehose" of data comparable to the Blue Sky firehose (focused on a specific community)
- An app similar to the "ngram viewer" but with semantic search. Would allow us to trace the evolution & timeline not just of specific words but of ideas & meaning
