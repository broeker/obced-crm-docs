---
title: OBCED CRM | Technology Empowerment Center Build Plan
date: 2020-11-13T00:00:00.000Z
permalink: /
eleventyNavigation:
  key: Home
  order: 0
---

# CRM Build plan
Electric Citizen | November 2020

This minisite contains documentation and wireframes to outline the final build plan for the OBCED Technology Empowerment Center CRM. Please review and reply with any potential concerns or questions about this plan. Once approved we will commence development.

* This plan is adaptable to small changes (e.g. different search filters, or prioritized fields in views)
* There are still open questions, as documented in the wireframe dev notes; many of these can be answered as we go 
* The application will follow Drupal standards/user interface elements; the wireframes are only a general representation of overall functionality
* Any significant changes or new features not documented in this build plan will require additional budget and time to complete

## Project overview

We are recreating an existing FileMaker CRM developed by OBCED that is used internally to track clients, donors, donations, inventory, classes, class registrations, and computer repair incidents. The CRM will be integrated into the existing admin area of the OBCED Drupal 8 website hosted on the UMN enterprise platform. Where possible, we have tried to improve upon and simplify the existing FileMaker tool while maintaining its core functionality. 

## Key requirements

The system is for internal use only, and will be managed by OBCED CRM managers to complete the following tasks:

* Add and manage clients 
* Add and manage client repair tickets
* Add and manage client class registrations
* Manage client "requirements" and eligibility status
* Manage "donations" of equipment to clients
* Add and manage donors
* Manage computer equipment inventory (gifts or donations from donor)
* Manage a list of classes so that class requirements can be added and tracked per client
* Provide reporting capabilities (CSV/Excel exports)

## Other notes

* OBCED will enter new data manually into the CRM
* Several fields currently call for an "other" option (e.g. yes/no/other) -- there is a Drupal module available that should help us offer this functionality, but we have not used it so the ultimate functionality will be determined by how well this module works in its current state.
* All relevant data in the system will be available for csv/Excel exports for advanced reports
* The number of "custom" reports built into the system for phase one will be limited
* See dev notes on the "Reporting" wireframe 
* More advanced built-in reports can be added in a future phase

## Definitions and vocabulary

**Client:** A user of OBCED's services. Clients can be added manually by OBCED staff or via a public form that allows them to create a client node (to be approved by OBCED staff.) 

**Donor:** A donor is an outside organization who donates equipment to OBCED

**Inventory:** Inventory is a database of all equipment donated to OBCED by its donors. When somebody gives to OBCED, the equipment is entered into inventory by OBCED staff and available to eligible clients.

**Donation:** A "donation" is the act of granting a piece of inventory to a specific client. When this happens, a "donation" node is created to keep track of the donation. The "inventory" remains in the inventory database, but its stock is set to 0 to indicate it is no longer available.

**Class:** A class is a manually maintained list of classes that a client can take in order to become eligible. 

**Class registration:** A class registration node is created whenever OBCED staff adds a new class to a client. 

**Computer repairs:** A computer repair node is created each time OBCED opens a repair ticket for a client.

**Note:** Under this model, "donations" are exclusively used in the context of OBCED gifting/donation equipment to a "client." Equipment provided or gifted to OBCED is referred to and tracked directly as "inventory." The inventory database is meant to be a historical record of ALL equipment coming into OBCED from its donors. When a piece of inventory is donated to a client, it will be marked as 0 inventory and no longer available for future donations. However, it will remain available in the inventory database for historical and reporting purposes.

## Client responsibilities

* Client will manually move/recreate data from their current system
* Client will provide the "terms" for each of the numerous taxonomies used in the system
* e.g. gender options, inventory quality options, income level options, skill level options, etc. (see data model for all vocabularies)
* Some of these categories are obvious and already defined, but some should be refined and/or provide by client
