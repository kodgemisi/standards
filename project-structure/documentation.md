---
title: Documentation standards
---

Minimum standards for writing documentation for projects:

* Every project should include metadata about the project, team and license in standard config files.<br>
  `pom.xml` for Java, `package.json` for Javascript etc.
  - Repository link (optional for internal projects)
  - Issue tracker link
  - Author(s) (optional)
  - Company and its link (optional)
  - License
* Every project should have  a `README.md` file in the root of the project folder.
* Server specific configuration or deployment instructions should be kept in a wiki page.
  - `README.md` doc should have a link to this document if and only if the project is an internal project.
* Document development database credentials (if any), connection url (if any) and any other information that may help other developers.

### `README.md` file contents

Every `README.md` file must contain **at least** following information (in that order):

* Project name
* Short project description (preferably more than a sentence less than 500 words).
* Screenshots (This is optional but strongly recommended for public projects)
* Prerequisites for building the project.
  - Command to build the project.
* Prerequisites for running the project.
  - Command to run the project.
  - Home page/Start page link of the application (remember we are going "development first", links are in localhost domain)
  - Login credentials
  	- If there are multiple roles in the project provide credentials of at least one user of each role
* Usage examples (if its a library)
* Link to documentation (if any)
* Link to issue tracking
* License