---
title: "What is SELECT FOR UPDATE in SQL (with examples)?"
url: "https://cockroachlabs.com/blog/select-for-update"
date: "Mon, 27 Jun 2022 00:00:00 GMT"
author: "Charlie Custer"
feed_url: "https://www.cockroachlabs.com/rss.xml"
---
Relational databases are great for transactional workloads. But things can get messy when multiple transactions start trying to access the same data at the same time. Luckily, in many SQL databases there’s a solution for that: SELECT FOR UPDATE.
