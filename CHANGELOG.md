# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).


<!-- Template:
## [Unreleased] - 2019-xx-xx
### Added
### Changed
### Deprecated
### Removed
### Fixed
### Security
-->

## [Unreleased]


## [0.0.10] - 2019-10-05
### BREAKING CHANGES
- **myhpi:** make Action.icon a binary png

## [0.0.9] - 2019-10-04
### BREAKING CHANGES
- **myhpi:** make InfoBit.description plain text

### Added
- **myhpi:** add InfoBit.content

## [0.0.8] - 2019-10-01
### BREAKING CHANGES
- **course:** support multiple lecturers
- **myhpi:** restructure MyHPI

## [0.0.7] - 2019-09-05
### BREAKING CHANGES
- **course, food, news:** support pagination

### Added
- **crashreporting:** add Crash Reporting definitions

### Removed
- **food:** remove MenuItem.substitution

## [0.0.6] - 2019-08-19
### Added
- **feedback:** add feedback definitions

## [0.0.5] - 2019-08-18
### BREAKING CHANGES
- **course:** make CourseSeries more strict
- **course:** make CourseDetail teletask + description optional
- **food:** add details to substitution
- **food:** support different prices for different customers
- **news:** rename Source, Category, Tag name to title
- **news:** make Article.view_count nullable
- **news:** rename remaining site occurrences to source
- **news:** make Semester.year an int32

### Added
- **common:** add Image.aspect_ratio
- **myhpi:** add Action.icon

### Documentation
- **myhpi:** document that Action.Text.content can be HTML
- **food:** remove unnecessary optional comments

## [0.0.4] - 2019-08-12
### Added
- add documentation on how to generate Dart code
- **course:** add course definitions
- **food:** add food definitions
- **myhpi:** add MyHPI definitions

### Changed
- shorten GitHub templates
- **news:** shorten proto descriptions

## [0.0.3] - 2019-08-12
### BREAKING CHANGES
- **course, myhpi:** split message definitions into multiple files

## [0.0.2] - 2019-07-05
### Changed
- Updated library `com.google.protobuf:protobuf-java` to version 3.8.0.

## 0.0.1 - 2019-07-05
Initial release with NewsService.


[Unreleased]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.10...dev
[0.0.10]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.9...0.0.10
[0.0.9]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.8...0.0.9
[0.0.8]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.7...0.0.8
[0.0.7]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.6...0.0.7
[0.0.6]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.5...0.0.6
[0.0.5]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.4...0.0.5
[0.0.4]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.3...0.0.4
[0.0.3]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.2...0.0.3
[0.0.2]: https://github.com/HPI-de/hpi-cloud-apis/compare/0.0.1...0.0.2
