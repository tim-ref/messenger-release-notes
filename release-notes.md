# Release Notes

All high-level changes for every TI-M ref release, and known bugs will be documented in this file. For more fine granular
changes, see the change logs of the individual components.

This is an initial version that will be improved with the following releases.

**Related change logs**:

- [messenger-client](https://github.com/tim-ref/messenger-client/blob/main/CHANGELOG.md)
- [messenger-org-admin](https://github.com/tim-ref/messenger-org-admin/blob/main/CHANGELOG.md)
- [messenger-proxy](https://github.com/tim-ref/messenger-proxy/blob/main/CHANGELOG.md)
- [messenger-push](https://github.com/tim-ref/messenger-push/blob/main/CHANGELOG.md)
- [messenger-rawdata-master](https://github.com/tim-ref/messenger-rawdata-master/blob/main/CHANGELOG.md)
- [messenger-registration-service](https://github.com/tim-ref/messenger-registration-service/blob/main/CHANGELOG.md)

<!--
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
-->


<!--

### Added

- A new feature.

### Changed

- A change in existing functionality.

### Deprecated

- A soon-to-be removed feature.

### Fixed

- A bug fix

### Security

- A vulnerability.

-->

## 0.28.0 (published on 2025-06-03)

### Added

- Support for insurance group users
- Support for gematik TI-Messenger-Testsuite 2.2.3.

### Fixed

- Fixed classic tim-variant org-admin-testdriver HBA cleanup

### Changed

- Improved Messenger-Service expire management in Registration Service 


## 0.27.0 (published on 2025-04-29)

### Added

- Support for up to 100mb large attachments
- Support for gematik TI-Messenger-Testsuite 2.2.1.

### Fixed

- Fixed test driver memory leak

## 0.26.0 (published on 2025-04-22)

### Fixed

- Improved test driver memory leak

### Changed

- Removed HBA Cleanup from Org-Admin testdriver.

## 0.25.0 (published on 2025-04-09)
### Added

- More monitoring.
- Support for gematik TI-Messenger-Testsuite 2.1.1.

### Changed

- Optimized caching of federation list.
- Stabilized certain messenger test driver interactions.

### Fixed

- An error that circumvented one stage of the federation list cache.
- Added missing Matrix media routes for thumbnails.
- The client will not use the deprecated Matrix media endpoints anymore, if the server supports the new endpoints.
- An issue with user presence.

##  0.24.0 (published on 2025-03-25)

### Added

- Support for testsuite 2.1.0
- For unknown methods, a response with HTTP status 405 is returned.
- A new message type "m.location" has been introduced.

### Changed

- The Org-Admin password can no longer be changed.
- The deprecated media config endpoint has been removed.

### Fixed
- The Org-Admin Client "Classic (ref_1)" is now provided.
- Creating a room, including inviting a user from outside the federation, is now correctly rejected.

## Known issues
The following restrictions apply when using Testsuite Version 2.2.3:
- Tests concerning dehydrates Devices are not supported yet 

## Version Compatibility Matrix
| Release | Domain Service | Raw Data Master | Registration Service | Messenger Proxy | Org-Admin Client | Org-Admin Test Driver | Messenger Client | Messenger Test Driver | Test Suite |
|:-------:|:--------------:|:---------------:|:--------------------:|:---------------:|:----------------:|:---------------------:|:----------------:|:---------------------:|:----------:|
| 0.24.0  |     1.7.2      |     0.3.14      |        0.6.0         |      0.7.2      |      0.13.0      |        0.16.0         |      1.28.0      |        0.13.0         |   2.1.0    |
| 0.25.0  |     1.8.0      |     0.3.14      |        0.6.1         |      0.8.0      |      0.13.0      |        0.16.0         |      1.28.1      |        0.13.5         |   2.1.1    |
| 0.26.0  |     1.8.1      |     0.3.14      |        0.6.1         |      0.8.0      |      0.13.0      |        0.17.0         |      1.28.1      |        0.13.6         |   2.1.1    |
| 0.27.0  |     1.8.2      |     0.3.14      |        0.6.1         |      0.8.1      |      0.13.0      |        0.18.0         |      1.28.1      |        0.13.8         |   2.2.1    |
| 0.28.0  |     1.8.3      |     0.3.14      |        0.6.2         |      0.8.2      |      0.13.0      |        0.18.0         |      1.28.1      |        0.14.2         |   2.2.3    |
