---
title: Change log 
metaDescription: This is a sample meta description. If one is not present in
  your page/post's front matter, the default metadata.desciption will be used
  instead.
date: 2017-01-01T00:00:00.000Z
permalink: /changelog/index.html
eleventyNavigation:
  key: Changelog 
  order: 4
---

This page includes documented changes or other notable project changes that have occurred since the original creation of these pages.  

## Request form (12/01)

---

> Sem: we also talked about room reservations, Aundrea said that a form can be built on the website for this purpose, which I agree. Once we receive the reservation email from our customers. can we have a portal on the database to add these records?  Perhaps we can have "Reservations" as a tool in the entry point

We have agreed to build a simple, public form and a content type to handle room reservations. This is not documented in the current data model. Here are the relevant notes from [Basecamp](https://basecamp.com/1970294/projects/17482249/messages/94017171):


> EC: Since this will be a public facing form with no login, we won't know ahead of time "who" the room reservation is for, or whether the person who submits the form is even a client. We also won't know ahead of time whether the room they reserve is available at the time they request. Because we do not have a budget for a full-blown registration/tracking system, we would propose:

* A simple "request form" that lets the use select the room they desire, and their desired time
* This would create a new node in your CRM called "reservation requests" 
* As new requests come in, your team would manually review and "approve" or "deny" the request
* It would be up to you to make sure you are not double booking, and to manually notify the the user if their request was accepted or denied

Does this sound workable to you? I think it is a reasonable approach that should fit in budget as long as you do not have a high volume of requests to track and manage. 

* Client has agreed to this overall approach
* We'll need to solicit further details for the content type -- I presume it will also involve one or more taxonomies (rooms, equipment)
* This task should be left until the end to see how much budget is remaining -- **if necessary, this can be handled in a Webform with no CRM integration.**

## Other client comments (12/1)

---

The following are responses from Sem regarding some of the questions posed throughout these documenation pages:

> Sem I am satisfied with the work so far, I think it will respond to what we want for our Unit.  I try to answer some of the questions on the dev. notes. 

* Sort by "most recently added" (?)  Yes
* Should we add "date created" field to view?  Yes
* What are the most important fields for the initial view+filters? ( first name and last name, gender , ethnicity, address, and eligibility)
* Are these the most important fields for views display? these are good enough
* Are these appropriate filters?  Yes
* Should "Status" be a term ref (e.g. open, closed, pending) or a boolean?  it should be a term ref ( open, closed, pending)
* In the "Repair" dashboard, can we  add  a field  for price, paid , and pick up option? 
* Also it would be nice to have a "technician note" where a technician would write what was done as a repair trail.

During development use these as guidance, best judgment in other cases, and go to Sem for clarity when necessary.

## Reporting Comments (12/1)

---

> Sem: For the reports, besides of what you mention,  can we have a report option for the classes.  perhaps, number the classes that are taught at a given time  (like quarterly ?,  types of classes, number of students that attended  ...)

EC Response: As noted with the other reports, we will do our best to either provide a useful report within the system and/or a way to export the Excel data needed to create one that suits your needs.
