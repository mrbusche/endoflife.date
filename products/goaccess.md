---
title: GoAccess
addedAt: 2024-03-11
category: app
permalink: /goaccess
versionCommand: goaccess --version
releasePolicyLink: https://github.com/allinurl/goaccess/blob/master/SECURITY.md
changelogTemplate: "https://goaccess.io/release-notes#release-__LATEST__"


auto:
  methods:
  -   git: https://github.com/allinurl/goaccess

identifiers:
-   repology: goaccess
-   purl: pkg:docker/allinurl/goaccess
# eol(x) = releaseDate(x+1)
releases:

-   releaseCycle: "1"
    releaseDate: 2016-06-09
    eol: false
    latest: "1.9.4"
    latestReleaseDate: 2025-03-31

---

> [GoAccess](https://goaccess.io/) is an open source web analytics application for Unix-like
> operating systems that runs in a terminal or through a browser.

Based on the release history, only the latest version is supported and actively maintained.
