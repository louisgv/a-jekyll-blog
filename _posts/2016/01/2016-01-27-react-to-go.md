---
layout: post
title: React to go
date: '2016-01-27 01:46'
---

# Setup
- A MCfly app that implement flux.
- With Material UI on top
- And some cool stuffs like data binding

Future:
- Have people be criticized for stuffs they are likely to have done. Even worse, stuff that should have been forgotten.
- Since there are people who keeps data...ls

A walk in the park...

# Micro-tourism
Building a technology that reinforce Yelp, Expedia and TravelOwl
- Input:
  - Current location (Need UI to confirm the location. Preferably with a water waving effect)
  - What are they up to (Shopping, Jogging, or Eating-out)
  - Duration of their travel.

  > How long would you like to walk? (`t`) How many places would you like to visit? (`p`) Average length of each visit? (`n`) How much would you like to spend? (`m`)

Require either `t` or `p`. `n` and `m` are optional.
- Output:
  - 3 list of `p` locations aligned such that they are a round trip, determined base on their lat-lng coordinate. (Need to research more on this)
  - Each destination has its own estimated time of visit. (`etv[i]`)
  - Total estimated time (`tet`) = (trip length) / (avg walking speed) + sum(etv)
  - A route map for all three possibilities

# User Story
- Go for a tech conference, have an hour to spare, want a nice tour.
- Go for a business, and would like to go on your own tour.
- Adventurous people who want to come up with their tour.
- New to town, would like to have a shopping sprint.

1 hour - 1.5 miles - 3 locations - 3 choices

avg walking speed: 3mph

# Algorithm flow

+ Implement a graph from all the location with cost being the time to travel and stay.
+ Using DFS to get the best one with lowest time cost.
+ Get a random solution using Reservoir Sampling.

* How to acquire a list of place that align into a round-trip?
