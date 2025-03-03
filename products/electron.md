---
title: Electron
layout: post
category: framework
changelogTemplate: |
  https://www.electronjs.org/releases/stable?version={{"__LATEST__" | split:'.' | first}}#__LATEST__
iconSlug: electron
permalink: /electron
link: https://www.electronjs.org/docs/latest/tutorial/support
eolColumn: Supported
activeSupportColumn: false
command: npm show electron version
releaseDateColumn: true
sortReleasesBy: releaseCycle
releases:
  # The approximate EoL going forward will be 8 months for every release
  # but this varies a lot currently due to the cadence change.
  - releaseCycle: "16"
    eol: false
    release: 2021-11-16
    latest: "16.0.5"
  - releaseCycle: "15"
    eol: false
    release: 2021-09-22
    latest: "15.3.4"
  - releaseCycle: "14"
    eol: false
    release: 2021-08-31
    latest: "14.2.3"
  - releaseCycle: "13"
    eol: false
    release: 2021-05-25
    latest: "13.6.3"
  - releaseCycle: "12"
    eol: true
    release: 2021-03-02
    latest: "12.2.3"
  - releaseCycle: "11"
    eol: true
    release: 2020-11-17
    latest: "11.5.0"
  - releaseCycle: "10"
    eol: true
    release: 2020-08-25
    latest: "10.4.7"
  - releaseCycle: "9"
    eol: true
    release: 2020-05-19
    latest: "9.4.4"
  - releaseCycle: "8"
    eol: true
    release: 2020-02-04
    latest: "8.5.5"
  - releaseCycle: "7"
    eol: true
    release: 2019-10-22
    latest: "7.3.3"
  - releaseCycle: "6"
    eol: true
    release: 2019-07-30
    latest: "6.1.12"
  - releaseCycle: "5"
    eol: true
    release: 2019-04-24
    latest: "5.0.13"
---
> [Electron](https://www.electronjs.org/) is a framework for building desktop applications using JavaScript, HTML, and CSS. By embedding Chromium and Node.js into its binary, Electron allows you to maintain one JavaScript codebase and create cross-platform apps that work on Windows, macOS, and Linux.

The latest _four_ stable major versions are currently supported (till May 2022, after which only [3 major versions will be supported](https://www.electronjs.org/blog/8-week-cadence)). Only the latest minor release in each major version is supported. A new major stable version is released every 8 weeks.

All supported release get fixes backported that were previously merged to main, though this may be on a case-by-case basis for some older supported releases. When an API is changed or removed in a way that breaks existing functionality, the previous functionality will be supported for a minimum of two major versions when possible before being removed.

The Chromium version of Electron is usually bumped within one or two weeks after a new stable Chromium version gets released. This estimate is not guaranteed and depends on the amount of work involved with upgrading. Only the stable channel of Chromium is used. If an important fix is in Chromium's beta or dev channel, it is back-ported.

## End-of-life

When a release branch reaches the end of its support cycle, the series will be deprecated in NPM and a final end-of-support release will be made. This release will add a warning to inform that an unsupported version of Electron is in use.

## Other Links

- A list of [officially supported platforms][platforms]
- [Best Practices for building secure Electron applications](https://www.electronjs.org/docs/latest/)
- [Versioning Policy](https://www.electronjs.org/docs/latest/tutorial/electron-versioning)
- [Release Timelines](https://www.electronjs.org/docs/latest/tutorial/electron-timelines)
- List of [Breaking Changes](https://www.electronjs.org/docs/latest/breaking-changes)

[platforms]: https://www.electronjs.org/docs/latest/tutorial/support#supported-platforms
