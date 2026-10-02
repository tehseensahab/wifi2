---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
date: {{ .Date }}
draft: true
description: ""
authors: [""]        # e.g. ["Dana Okafor"]. Links to the author page
topics: []
summary: ""              # the price, whether it's a real low, who should buy
imageAlt: ""
dealPrice: 0
listPrice: 0             # optional. Only the real pre-sale price
retailer: ""
priceChecked: {{ dateFormat "2006-01-02" .Date }}
expires: ""              # optional
dealUrl: ""              # affiliate link, rel=sponsored is added for you
---
Say whether this is a real low and for whom.

## Price history
