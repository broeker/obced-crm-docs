---
title: Dev notes 
metaDescription: This is a sample meta description. If one is not present in
  your page/post's front matter, the default metadata.desciption will be used
  instead.
date: 2017-01-01T00:00:00.000Z
permalink: /dev-notes/index.html
eleventyNavigation:
  key: Dev notes 
  order: 3
---

This page includes overall development guidelines and principles to follow throughout the course of development 

## Overview 

* The field names, field types, views filters, and so on that appear in the wireframes are merely suggestions or best guess attempts
* Use common sense when creating, and ask client when clarification is needed
* This is an isolated tool that will have its own "dashboard" at its own admin URL within the main OBCED site
* The CRM is only available to authenticated users (site managers or other appropriate roles)
* Create a CRM Manager role and set all appropriate permissions on views and nodes
* All of the content types should be hidden/removed from the primary content editing interface
* Provide a sensible URL pattern for all content types
* For all data exports, provide a sensible set of fields that includes all of the relevant data for a given export (including fields not directly visiible in the view)
* For all primary admin views, select a sensible set of display fields and filter based loosely on the wireframes
* For all primary admin views, provide sort functionality on all relevant columns (not shown in wireframes)
* Client can provide feedback on needed filters/helpful view fields as needed
* All unnecessary content type options should be disabled and removed from the content edit forms
* All edit forms should be simplified and minimized as much as possible
* There is NO NEED for a standard "node view" -- perhaps there is an easy way to disable and/or programatically direct the use to /edit on all attempts at a node view
* We will use Field Group tabs to organize admin forms, esp. the client forms (see wireframes)
* We will use Inline Entity forms and custom Entity Browsers to allow for easy selection/creation of nodes throughout the CRM
* Entity browsers should be customized so that a user can easily search/filter (e.g when assigning a class or a donation to a client)
* Not present in wireframes, but it may make sense to introduce VBO for some of the views

## Key challenges/approaches

The overall data architecture is straight forward but relies on a few tools and techniques that go beyond vanilla Drupal:

* Heavy use of Inline Entity Forms and custom Entity browsers to manage the user interface
* Mapping tables (e.g. class registrations, donations)
* Dual data entry points -- users can add a repair ticket or a donation from multiple places. When created via the main screen, a new entity reference needs to be created programatically on the client node so that the reference show up on the client editc screen
* Inventory management -- each time an inventory item is "donated", we will need to set its inventory status to "not in stock" so that it does not appear in the available inventory list
* It may be challenging to always return the user to the "right" place after completing various actions via a destination query; we will do our best 

 
