---
title: Data model 
metaDescription: This is a sample meta description. If one is not present in
  your page/post's front matter, the default metadata.desciption will be used
  instead.
date: 2017-01-01T00:00:00.000Z
permalink: /data-model/index.html
eleventyNavigation:
  key: Data model
  order: 2
---
This page demonstrates the Drupal content architecture and data model that will be used to drive the CRM. There may be small changes to this model as development progresses but we will generally follow this structure.

* Blue = Content type
* Green = Vocabulary (categories)
* Yellow = User reference to internal admin user
* Pink = Additional client fields
Note: We will need a final list of "terms" for each of the 12 identified vocabularies (green).
----------

![](../static/img/OBCED2.png)

----------

## Dev notes

* Errata: in the above diagram there should be a one-to-one mapping from Donors to Inventory.
* These are not final field names; use sensible field names in all cases. 
* Some fields may need further adjusting as needed. 
* Fields in bold may require extra discussion.
* Does it make sense to combine "categories" and "type" into a single hierarchical vocabulary? 
