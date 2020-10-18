# Web crawler/Google Search working/Page Rank/Indexing of huge set of documents/Hadoop/Google Big Table

## Problem Statement: Design a search engine like google at scale with latency within miliseconds

### Solution Summary: Entire solution has four stages:
         a. Web-crawler: scans all pages on web and stores their latest copies on servers. 
         b. Indexing services: Indexing services index the collected pages/content/snippets for keywords
         c. Page Ranking: Now we have keywords to page mapping but when we query, search results have to be sorted based on relevance. This is done by this service. 
            This service uses many parameters to determine position of pages on search results first page. Below are some parameters:
            i. Geolocation: Search results might have different relevance based on geolocation. For example, some search terms might be more frequent in certain geographies compared to others
            ii. Query: And or OR: if search query contains a phrase then search results containing the full phrase might be disapled first. For example, searching for code snippet or exception stack trace in search. 
            iii. Freshness of Page: Latest pages should appear in results first as compared to stale or old pages
            iv. Pages with more hits: If search term is repeated then search engine can keep track of links which are opened more frequently for particular combination of search terms, phrases. This means that those links are more relevant as compared to others and their ranking can be improved
            v. Position of search terms in document: Like document which has search term in title, image names and more appearance has more likelyhood of being related to the searched term more as compared to documents where word/term appears less. In nutshell the frequency and location of search/term phrases in documents
            vi. Search Raters: Search Raters are the users who are paid to collect feedback on relevance of search results, specially for new keywords typed in search. Google actually does that.
        d. Query Services: Query services will contexualize and cateorise the query in correct way. For example, "replace light buld", "change light buld" essentially mean the same thing. So there should be a synonym service to interprete the queries. Then to find the other aspects of query like is it question, 
        e. Search result aggregator service: Output of abov service might just be ids of documents which should be part of result and their order but search result aggregator has to fetch those document's cached pages and find in the documents where those terms appear, their positions, and summary extraction to display on the page.
  






# Important links:
1. [google: How search works](https://www.google.com/search/howsearchworks/crawling-indexing/)
2. [Wiki: Web-crawler](https://en.wikipedia.org/wiki/Web_crawler)
3. [Page Ranking algorithms](https://www.google.com/search/howsearchworks/algorithms/)
4. [Google search working in 5 mins](https://www.youtube.com/watch?v=0eKVizvYSUQ)
