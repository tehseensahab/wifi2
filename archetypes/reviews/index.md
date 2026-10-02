---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
date: {{ .Date }}
# lastmod: {{ .Date }}   # set when you retest or update. Shown as "Last updated"
draft: true
description: ""          # one line for cards, search, and meta description
author: ""
topics: []               # first topic is the card label. Slugs in data/topics.yaml
tags: []
summary: ""              # 2-3 sentences, answer first: verdict, who it is for, the catch
imageAlt: ""             # describe the real photo in cover.jpg
# imageCredit: "Photo: [Name](https://unsplash.com/...) / Unsplash"

# Review fields
brand: ""
product: ""
price: 0                 # USD, street price on the test date
score: 0.0               # 0-10
bestFor: ""              # shown on the card as "Best for ___"
testedOn: {{ dateFormat "2006-01-02" .Date }}
pros:
  - ""
cons:
  - ""
specs:                   # renders the Key specs table
  - {k: "Wi-Fi standard", v: ""}
  - {k: "Bands", v: ""}
  - {k: "Ports", v: ""}
  - {k: "Coverage", v: ""}
  - {k: "Street price", v: ""}
faq:
  - q: ""
    a: ""
  - q: ""
    a: ""
sources:
  - title: ""
    publisher: ""
    url: ""
---

Start with the verdict in one paragraph. Use `##` headings so the table of contents works.

## How we tested

## What we liked

## What we didn't

## Who should buy it

## Verdict
