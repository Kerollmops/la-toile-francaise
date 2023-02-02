# Let's Build a Search Engine for the French Web

Wouldn't it be cool to build our very own search engine?

I propose the challenge of building a Web Search Engine à la Google, Yahoo, or DuckDuckGo. We can learn a lot about data processing, ways to optimize the code, and trade-offs to make. I define a bunch of rules in advance to ensure the project keeps being small and accessible.

This challenge is open to anyone interested. Rules can change in the future. It is non-mandatory, and people must only work on it in their free time. It is a collaborative project; therefore, a different version of a specific part of the system can be plugged together with different programming languages with different algorithms.

I initially thought about this project when reading [AWS Abusing Search Engine Gets Abused](https://boyter.org/posts/aws-abusing-search-engine-gets-abused/), in which Boyter talks about a search engine only indexing Australian websites. However, I would prefer that we use french services and increase France's [Network sovereignty](https://en.wikipedia.org/wiki/Network_sovereignty).

## Rules and Constraints

Contributors can modify these rules in the future, but most recent contributors must agree to accept the changes. Developers must strictly follow these rules for a contribution to be accepted.

### User Experience and Interface

There must be a web page with a text input called a "search bar" for the user query results. The matching result is a list of links of the best matching pages where the visible text is the webpage title. The system only shows the first forty (40) best results on one page.

The system must return this list of results in less than a second. We must do our best to answer the best results we can compute for any given user query in this amount of time. Sometimes it will be hard, and some queries will see altered results. We can inform the user about that.

The project must maintain a ["one nine" (90%) availability](https://en.wikipedia.org/wiki/High_availability) to keep a good enough quality of service without having to wake up at night at any time.

I define best-matching results as web pages relevant in time: non-outdated results, and appropriate according to the query. However, many results can degrade the search experience, like phishing and cheating websites, and we must hide them as much as we can.

### Cost of the Project

The project must be relatively inexpensive. We must spend less than 200€/month. We must find the most efficient way to compute, store, and retrieve the data we gather. One or multiple machines, a storage service, or anything that can reduce costs is allowed. However, no abuse of free trial offers is accepted. This project must be viable and sustainable over time without hurting other companies.

The web is a tough place to live. DDoS attacks are current, and our project can suffer from that. We must find a cost-efficient way to keep the service available to genuine users without increasing maintenance costs too much. We do not accept donations for the project as of now.

### Search Set

This project aims to expose a good web search engine that returns the best results for french websites. I define a french website as any webpage that is mainly composed of french text, but as of now, it could be easier to restrict on [the french TLD (.fr)](https://en.wikipedia.org/wiki/List_of_Internet_top-level_domains).

### Technology-Wise

As this project must reduce the cost, we can start by relying on other technologies like [Common-crawl to gather the websites](https://commoncrawl.org/). However, this project also aims to deliver the best results; therefore, we will surely need to design our own tools in the future.

This project is more an educational project than a money-wise sustainable company, which means that we are here to learn and design our system. Contributors should create the essential bricks from the ground up. We can use other technologies, but we must architecture those bricks ourselves.

We must keep a simple design and simple tools to achieve our goals. Avoid complex instruments and hard-to-maintain and understand configurations of them. Keep the codebase modules and behaviors well documented for external and internal contributors to dive into it quickly.

### Gathering Statistics

As the project must be sustainable, gathering statistics is crucial and must be done from the start. Understanding the way our users search and find the results interesting is essential. It would be great to have a bunch of graphs showing the indexing time, search time, web-crawling status, errors, and our system logs.

### License

The project must use an open-source license, e.g., MIT, APACHE-2.0. However, a lot of the software and hardware are not open source. We allow running our project on non-open source services. However, suppose we have the choice between different equivalent technologies. In that case, a contributor must choose the open-source one rather than the other if a developer _can easily contribute the possibly missing features to the open-source project_.
