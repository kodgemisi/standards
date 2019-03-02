---
title: General coding standards
description: Common principles when writing any piece of code
---

This document outlines the common principles for writing any piece of code in any language.

When developing software wheter it is a project or a small script we comply with best practices and and a minimal documentation of usage of it.

## Technology selection

* All apps use HTTP/2 and https by default, http redirects to https.
  - Use Let's Encrypt for certificates.
  - Use scheduled auto reneval scripts for sertificates.
* Use Spring Boot with Java or Groovy language.
  - You can use other languages and frameworks only in following conditions:
    - To be decided (TODO)

## Password selection

* Password selection for DB/email/server/app admin: at least 15 char alpha numeric, use https://strongpasswordgenerator.com (without punctuation)
  - Follow this standards even for development and test environments.

## Email usage in apps

* Use a dedicated email address for every application.
* Use a different email address for an applications different environments.
* Don't use an email address from `kodgemisi.com` domain for any environment bu prod.
* E.g. prod: acme<i class="at-sign"></i>kodgemisi.com, test: acme-test@yandex.com, dev: acme-dev@yandex.com

## Coding style

* Use <a href="https://semver.org/" target="_blank">semantic versioning</a>.
  - Start a new project with `0.1.0`. Only upgrade it to `1.x.x` when it's started to be used in prod.
* Don't invent new styles, learn and use related community's de-facto standard styles.

### Ongoing or in-maintanence project

* If there is any established coding standards in the project (even it is not in complience with best practices) you should comply to it. This is required for consistency.
* If there is an IDE style file (for the project) you can import you have to import it, it is not optional.

### New project

* You should comply with the standards given by Kod Gemisi. 
* If there is no standards set by Kod Gemisi for the language/framework you are working in then it is **your responsibility** to learn official coding style of the language/framework and use it.
* If there is an IDE style file you can import for the language/framework provided by Kod Gemisi you have to import it, it is not optional.

## Source Control

* Use Git.
* Learn to use Git from command line. (remember that this is not optional)
* Use git from command line. (Optional)
* Don't put any code on a live system unless it has a repository. Create a Git repository or a Gist/Snippet under source control for the code.

