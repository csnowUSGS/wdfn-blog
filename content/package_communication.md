---
author: Lindsay R Carr
date: 2017-07-20
slug: package-communication
draft: True
title: GRAN Package Categories
type: post
categories: Data Science
author_github: ldecicco-usgs
author_email: <ldecicco@usgs.gov>
tags: 
  - R
description: Defining USGS R package categories for clear communication of maintenance, feature development, and user support.
keywords:
  - R
---
Clear communication about package expectations is very important. Package developers should be transparent about the maintenance, development, and user support associated with their package so that potential users are aware. To help with this communication for USGS R packages, we have created the following categories:

1.  Core
2.  Research (Active and Archive)
3.  Support
4.  Private/Exploratory
5.  Orphan

Each are described in detail below. In general, they go from most support/outreach ("Core") to least ("Orphan").

People with packages on the [USGS-R GitHub community](github.com/USGS-R) and/or [GRAN](https://owi.usgs.gov/R/gran.html) should add a startup message to their pacakge indicating the package category. See `?packageStartupMessage` to learn how.

Core
====

A package with the designation “Core” has several key features:

-   Critically important to a wide and general audience
-   Published, peer-reviewed documentation on the package function
-   Long-term support addressed publicly (could be stated in README or elsewhere)
-   Bug-fixes
-   R version upgrades
-   R package dependency changes
-   Customer support and troubleshooting
-   An active USGS employee is designated as maintainer. Development and maintenance of core packages should include a team of developers. Maintainers coordinate and lead the development team, but should not be the sole developer.
-   The package should be well tested, and the package should be tested on a continuous integration platform regularly.
-   All external functions should have clear documentation and working examples.

A user of core packages can expect prompt feedback from bug reports and general-use questions. Users can expect smooth transitions of maintainers since the package is well-tested, well-documented, and multiple developers have collaborated on the project. Enhancements should be carefully considered, “scope-creep” should be actively avoided (that is, careful thought to add new features). The general scope of the package should not change over time.

Research
========

Research packages have two distinct phases: Active and Archive.

Active Research:
----------------

A package with the designation “Active Research” has several key features:

-   The package is in active development and there is no guarantee of future behavior.
-   An official disclaimer is shown on the README and package startup message.
-   The development of the package is being driven by a research topic, and includes input from both researchers and software developers.
-   The end goal should be one or more peer-reviewed journal publications.
-   A “sunset” date should be communicated on the README and package startup message. This is an indication of how far in the future the work for this package is currently supported.
-   Emphasis should still be placed on testing key features and good documentation during development.
-   Since the goal is a published article, the expectation should be that outside users will use this package to test the reproducibility of the primary author’s data analysis, as well as reproducing the analysis on new data.
-   During development, the package version should remain below v0.0.0.

It is important to clearly communicate to any known or unknown users the risk they take with using a package that is in the active research development phase. \#\# Archive Research:

A package with the designation “Archive Research” has several key features:

-   Ideally, the development of the active research package was completed with the publishing of a scientific, peer-reviewed journal or report
-   A reproducible work-flow is included either within a vignette or via the final product (such as the journal article)
-   A message on the README indicates the archive status.
-   There are no official expectations that bug fixes and R version upgrades will happen.
-   The package maintainer should have an active email.
-   The package version should be updated to v1.0.0 once a stable version is released.

It should be clearly communicated that the package has a well-documented final product. An archived research R-package can certainly maintain development such as bug fixes and required changes to R version updates. Maintaining the package and interacting with users can be very beneficial for professional development. However, it is important to communicate the official level of support for future users.

Support
=======

A package with the designation “Infrastructure” may not have a research component, and also not intended for a wide, general audience. However, these packages may be critically important to other projects throughout the USGS. Therefore, it is important to follow best practices in the package development, as well as clearly communicate the intent and level of support for these packages.

-   An active USGS employee is designated as maintainer. Development and maintenance of core packages should include a team of developers. Maintainers coordinate and lead the development team, but should not be the sole developer.
-   The package should be well tested, and the package should be tested on a continuous integration platform regularly.
-   Key functions should have clear documentation and working examples.

Private / Exploratory
=====================

These packages should remain on personal github repositories or local computers. These packages offer value to only a small number of people for a limited time.

Orphan
======

A package with the designation “Orphan” does not have an active USGS employee designated as maintainer. The odds of a package becoming orphaned can be minimized during the package-creation phase by using a team of developers to collaborate, and emphasizing clear documentation and high test-coverage. Community efforts to troubleshoot issues and submit bug-fixes are encouraged. Orphan packages should include some communication on both the readme and package startup message that the status is “orphan” and information on who to contact to volunteer to take over maintainer duties.

Training from USGS-sponsored courses should avoid orphan packages until they have designated an active maintainer and have addressed long-term resource commitments.
