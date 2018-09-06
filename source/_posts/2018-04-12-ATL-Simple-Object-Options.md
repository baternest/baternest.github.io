---
title: ATL Simple Object Options
date: 2018-04-12 15:18:41
categories:
tags:
---
# Options

## Aggregation

Yes: (NONE)
No: DECLARE_NOT_AGGREGATABLE()
Only: DECLARE_ONLY_AGGREGATABLE()

## Interface (IDL Attributes)

Dual: dual
Custom: (NONE)
Custom with Automation compatible: (oleautomation)

[IDL Attributes](https://msdn.microsoft.com/en-us/library/8tesw2eh.aspx)

## Threading model

CComSingleThreadModel
Single: (NONE)
Apartment: val ThreadingModel = s 'Apartment'

CComMultiThreadModel
Both: val ThreadingModel = s 'Both'
    Free-threaded marshaler: CoCreateFreeThreadedMarshaler()
Free: val ThreadingModel = s 'Free'
Neutral: val ThreadingModel = s 'Neutral'
