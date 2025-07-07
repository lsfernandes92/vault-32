2025-07-07 18:30

Status: #child 

Tags: [[dev]] [[system-design]]

# how does CDNs work?

CDN fetches assets for the original server

every CDN server has it own local cache

after CDN **cache hit** it will store a cache version of the site and serve it to the client

## strategies
##### pull cdn

it lazily fetches
fetches automatically when a new version is up

it usually takes 1 day to stale

are the most common strategy




##### push cdn

the engineers must push the updated file to the CDN in order to porpagate it to all CDNs server caches

the first client request will be faster than pull CDN bc the CDN server already has the fetched version




# References

- [[what are CDNs?]]
