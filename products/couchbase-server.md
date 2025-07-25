---
title: Couchbase Server
addedAt: 2021-10-18
category: database
iconSlug: couchbase
permalink: /couchbase-server
alternate_urls:
-   /couchbase
versionCommand: cat /opt/couchbase/VERSION.txt
releasePolicyLink: https://www.couchbase.com/support-policy/enterprise-software/
changelogTemplate: https://docs.couchbase.com/server/__RELEASE_CYCLE__/release-notes/relnotes.html
eolColumn: Full Maintenance

identifiers:
-   repology: couchbase-server-community
-   purl: pkg:docker/library/couchbase
-   purl: pkg:docker/couchbase/server
-   cpe: cpe:2.3:a:couchbase:couchbase_server
-   cpe: cpe:/a:couchbase:couchbase_server

auto:
  methods:
  -   couchbase-server: https://docs.couchbase.com/server
      regex: '^Release (?P<version>\d+\.\d+(\.\d+)?) \((?P<date>.+)\)$'
  -   release_table: https://www.couchbase.com/support-policy/EOL/
      selector: "table"
      fields:
        releaseCycle:
          column: "Release"
          regex: '^Couchbase Server (?P<value>[0-9.]+)$'
        eol: "End of Full Maintenance"
  -   declare: couchbase-server
      versions:
        # Dates are not available for all versions, so they must be set manually in some cases.
        -   { name: "6.0.0", date: 2018-10-31 } # https://www.couchbase.com/blog/announcing-couchbase-6-0/
        -   { name: "6.0.1", date: 2019-02-15 } # https://web.archive.org/web/20190307191211/https://docs.couchbase.com/server/6.0/release-notes/relnotes.html
        -   { name: "6.6.0", date: 2020-08-12 } # https://www.couchbase.com/blog/whats-new-and-improved-in-couchbase-server-6-6/
        -   { name: "7.2.0", date: 2023-06-01 } # https://www.couchbase.com/blog/couchbase-capella-spring-release-72/

releases:
-   releaseCycle: "7.6"
    releaseDate: 2024-03-31
    eol: 2026-07-31
    latest: "7.6.6"
    latestReleaseDate: 2025-05-31

-   releaseCycle: "7.2"
    releaseDate: 2023-06-01
    eol: 2026-07-31
    latest: "7.2.7"
    latestReleaseDate: 2025-03-31

-   releaseCycle: "7.1"
    releaseDate: 2022-05-31
    eol: 2024-01-31
    latest: "7.1.6"
    latestReleaseDate: 2023-11-30

-   releaseCycle: "7.0"
    releaseDate: 2021-07-31
    eol: 2023-01-31
    latest: "7.0.5"
    latestReleaseDate: 2022-12-31

-   releaseCycle: "6.6"
    releaseDate: 2020-08-12
    eol: 2023-01-31
    latest: "6.6.6"
    latestReleaseDate: 2023-01-15

-   releaseCycle: "6.5"
    releaseDate: 2020-01-15
    eol: 2021-02-28
    link: https://web.archive.org/web/20230519160357/https://docs.couchbase.com/server/6.5/release-notes/relnotes.html
    latest: "6.5.2"
    latestReleaseDate: 2021-02-15

-   releaseCycle: "6.0"
    releaseDate: 2018-10-31
    eol: 2020-07-31
    link: https://web.archive.org/web/20230519162206/https://docs.couchbase.com/server/6.0/release-notes/relnotes.html
    latest: "6.0.5"
    latestReleaseDate: 2022-04-30

---

> [Couchbase Server](https://www.couchbase.com/products/server) is a modern cloud-native,
> distributed database that fuses the strengths of relational databases such as SQL and ACID
> transactions with JSON flexibility and scale that defines NoSQL. It is available as a service in
> commercial clouds and supports hybrid and private cloud deployments.

Security updates stop when a release reaches end of "Full Maintenance". Major versions are supported
for the longer period between:

1. 30 months from its General Availability Date
2. 6 months after the next Major Release version release.

Limited Support is also available after the end of Full Maintenance. But this is only best effort
support without any code fixes nor security updates, so this page does not track it.
