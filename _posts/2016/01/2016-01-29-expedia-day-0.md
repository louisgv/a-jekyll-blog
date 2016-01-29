---
layout: post
title: 'Expedia : Day 0'
date: '2016-01-29 15:23'
---

# Expedia API
## GeoID extracting
Take user input such as "New York" etc and resolve it to a valid geographical region

```
  http://terminal2.expedia.com/x/suggestions/regions?query=New%20York&apikey={INSERT_KEY_HERE}
```

This will return a response that includes the following:

```
{ . . .
  "f":"New York (and vicinity), New York, United States of America",
  "id": "178293",
  . . .
}
```

## Get Point of Interests
  Supply latitude, longitude, and radius and get back travel attractions and/or point of interests using the Geography Search API

  Within 5km:

```
   http://terminal2.expedia.com/x/geo/features?within=5km&lng=-122.453269&lat=37.777363&type=point_of_interest&apikey={INSERT_KEY_HERE}
```

  Find all features (hotels, regions and points of interest) within 5 minutes walk of a given feature

```
    http://terminal2.expedia.com/x/geo/features/319476466226038470/features?mode=walking&within=5min&verbose=2&apikey={INSERT_KEY_HERE}
```

## Search Using Natural Language
- q = ""

  ```
  http://terminal2.expedia.com/x/nlp/results?q=my%20wife%20and%20i%20need%20a%20deal%20in%20las%20vegas%20this%20weekend&apikey={INSERT_KEY_HERE}
  ```

- return:

## Feature Types:

```
{
  "default": [
    "city",
    "continent",
    "country",
    "custom_large",
    "custom_medium",
    "custom_small",
    "high_level_region",
    "metro_station",
    "multi_city_vicinity",
    "multi_region_within_a_country",
    "neighborhood",
    "point_of_interest",
    "province_state",
    "train_station"
  ],
    "aoi": [
      "city",
      "continent",
      "country",
      "custom_large",
      "custom_medium",
      "custom_small",
      "metro_station",
      "multi_city_vicinity",
      "multi_region_within_a_country",
      "neighborhood",
      "point_of_interest",
      "province_state",
      "train_station"
    ],
    "region": [
      "airport_metro_code",
      "city",
      "continent",
      "country",
      "custom_large",
      "custom_medium",
      "custom_small",
      "neighborhood",
      "province_state"
    ],
    "destination": [
      "city",
      "multi_city_vicinity"
    ],
    "touristic_neighborhood": [
      "neighborhood"
    ]
  }
}
```


# Extracting user's Current Location

+ Using Chrome API
