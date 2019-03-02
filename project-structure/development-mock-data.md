---
title: Development Mock data
description: The minimal information level of development mock data
---

Development mock data should be database agnostic. Hence, avoid using database specific functions and keywords.

Mock data should (at least) have

* A different user per available role in the app.
* At least 2 pages of item (with default paging options) for each listable resource.
* Profile pictures, company logos and other uploadable images, if applicable.

Note that values of multiselect lists (e.g. provinces and districts etc.) or status (e.g. available, blocked etc.) or states (e.g. applied, approved etc.) are part of the application itself and should not be considered as development or test data.

There are two filename conventions in Spring for automatically execute SQL on boot time. `import.sql` and `schema.sql`, see <a href="https://docs.spring.io/spring-boot/docs/current/reference/html/howto-database-initialization.html#howto-initialize-a-database-using-hibernate" target="_blank">Initialize a Database Using Hibernate</a>

Only `schema.sql` supports suffixes for different database platforms. You can optionally exploit this feature to only import data for h2 database. So that you have an effective configuration to import development mock data only in database.