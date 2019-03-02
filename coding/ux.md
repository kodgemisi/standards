---
title: User experience 
description: Rules and conventions for creating intuitive user
---

This document outlines the standards for writing projects in Java.

* When user clicks on the logo, s/he goes to the homepage.
* When user request a page but redirected to login, s/he is redirected to the original page s/he requested before login.
* For notification/information emails;
  - The title must be natural and descirptive
  - All event data (in accordence with authorization rules) is present in email.
  - Users should only have to click on links for actions not information.
* When there is a list\*, it is pageable.
* When there is a list\*, it is filterable by (preferably all) essential fields.
* Unless the business logic requires otherwise, all lists are ordered by event time or creation time in descending order (most recent first).
  - Lists consisting of timeless items are ordered alphabetically.
* All searches are case insensitive.
* All saerches are tolerable to Turkish characters. E.g. searching "ask" results in "aşk" as well. (optional)
* Form validation errors appear under or near to the related fields and are in different color.
  - Errors spanning more than one field appear on the top or the bottom of the form.
    - If the form is long, make sure the user sees the error without any scrolling.
* Action names, resource names and page names are consistent accross pages.

\* Valid only for lists that are expected to have more than 10 elements.