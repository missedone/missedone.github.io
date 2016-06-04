---
layout: post
title: Cassandra References
categories: [db, nosql, cassandra]
tags: [nosql, cassandra]
description: the collection of Cassandra relate articles.
---

## Getting Started

### Installation

* for Mac
  * [Installing Cassandra on Mac OS X](https://gist.github.com/hkhamm/a9a2b45dd749e5d3b3ae)
    ```bash
    ll /usr/local/Cellar/cassandra/
    ln -s /usr/local/Cellar/cassandra/3.5/homebrew.mxcl.cassandra.plist ~/Library/LaunchAgents/homebrew.mxcl.cassandra.plist
    
    # Use this command to start Cassandra:
    launchctl load ~/Library/LaunchAgents/homebrew.mxcl.cassandra.plist

    # Use this command to stop Cassandra:
    launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.cassandra.plist
    ```

## Modeling

* 2016
  * [Understanding the Guarantees, Limitations, and Tradeoffs of Cassandra and Materialized Views](http://www.datastax.com/dev/blog/understanding-materialized-views)
* 2015
  * [New in Cassandra 3.0: Materialized Views](http://www.datastax.com/dev/blog/new-in-cassandra-3-0-materialized-views)
  * [Materialized Views in Cassandra 3.0](https://cassandra-zone.com/materialized-views/)
  * [Basic Rules of Cassandra Data Modeling](http://www.datastax.com/dev/blog/basic-rules-of-cassandra-data-modeling)
  * [Cassandra Day London 2015](http://mrcalonso.com/cassandra-day-london-2015-2/)
  * [Benchmarking Cassandra Models](http://mrcalonso.com/benchmarking-cassandra-models/)
  * [Data Modelling Recommended Practices](https://support.instaclustr.com/hc/en-us/articles/207071957-Data-Modelling-Recommended-Practices)
* 2014
  * [16 Notes on Cassandra Summit Europe 2014](http://mrcalonso.com/16-notes-cassandra-summit-europe-2014/)
  * [16 Notes on Cassandra Summit Europe 2014 (Part II)](http://mrcalonso.com/16-notes-cassandra-summit-europe-2014-part-ii/)
* 2012
  * [Cassandra Data Modeling Best Practices, Part 1](http://www.ebaytechblog.com/2012/07/16/cassandra-data-modeling-best-practices-part-1/)
  * [Cassandra Data Modeling Best Practices, Part 2](http://www.ebaytechblog.com/2012/08/14/cassandra-data-modeling-best-practices-part-2/)
