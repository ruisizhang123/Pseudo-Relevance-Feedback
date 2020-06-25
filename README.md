#### Feature

Ranking documents of a query using BM25 Score in **Document Ranking Phase** and Rocchio Algorithm in **Query Expansion Phase**.

![](https://github.com/ruisizhang123/EE448/blob/master/archi.png)


#### Usage

1. Create a folder name `data` and put query txt and doc txt in `./data` folder

2. Run ``EE448.ipynb`` to visual output 

3. The output ranked documents is in `./data/bm25_score.txt`

#### Dependencies

Python >= 3.0

#### Dataset Overview

1. `./data/query.txt`: `query_id \t query_text`

2. `./data/doc.txt`: `document_id \t document_text`

#### To Get Better Ranking Results...

1. Set expansion words in `util.py/findNewQuery/loopRange` to different value. If the documents is short, set loopRange to a smaller value.

2. Set `k2` in `score.py/bm25` to larger value.

3. Set `GAMMA` to 0.15 or 0 to enable positive feedback and negative feedback

4. You may try different Score Function like TF-IDF to rank documents in `score.py`

#### Reference

https://github.com/preethiA30/Search-Engine
