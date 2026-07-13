---
title: "How to implement HTTP request retry policies"
url: "https://pusher.com/blog/how-to-implement-http-request-retry-policies/"
date: "2022-10-26"
author: ""
feed_url: "https://pusher.com/blog"
---
HTTP requests are always at risk of failure. No matter how highly available both the source and destination hosts are, the request can still encounter an issue in the intermediary network that you have no control over. Given this, it makes sense to devise an HTTP request retry strategy. You want to ensure systems can handle and recover from unexpected failures when making HTTP requests.
