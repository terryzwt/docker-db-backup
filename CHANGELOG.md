## 2.8.0 2021-08-27 <dave at tiredofit dot ca>

   ### Added
      - Alpine 3.14 Base

   ### Changed
      - Fix for syntax error in 2.7.0 Release (Credit the1ts@github)
      - Cleanup image and leftover cache with AWS CLI installation


## 2.7.0 2021-06-17 <dave at tiredofit dot ca>

   ### Added
      - MongoDB Authentication Database support (DB_AUTH)


## 2.6.1 2021-06-08 <jwillmer@github>

   ### Changed
      - Fix for Issue #14 - SPLIT_DB=TRUE was not working for Postgres DB server


## 2.6.0 2021-02-19 <tpansino@github>

   ### Added
      - SQLite support


## 2.5.1 2021-02-14 <dave at tiredofit dot ca>

   ### Changed
      - Fix xz backups with `PARALLEL_COMPRESION=TRUE`


## 2.5.0 2021-01-25 <dave at tiredofit dot ca>

   ### Added
      - Multi Platform Build Variants (ARMv7 AMD64 AArch64)

   ### Changed
      - Alpine 3.13 Base
      - Compile Pixz as opposed to relying on testing repository
      - MSSQL Support only available under AMD64. Container exits if any other platform detected when MSSQL set to be backed up.

## 2.4.0 2020-12-07 <dave at tiredofit dot ca>

   ### Added
      - Switch back to packges for Postgresql (now 13.1)


## 2.3.2 2020-11-14 <dave at tiredofit dot ca>

   ### Changed
      - Reapply S6-Overlay into filesystem as Postgresql build is removing S6 files due to edge containing S6 overlay


## 2.3.1 2020-11-11 <bambi73@github>

   ### Fixed
      - Multiple Influx DB's not being backed up correctly

## 2.3.0 2020-10-15 <dave at tiredofit dot ca>

   ### Added
      - Microsoft SQL Server support (experimental)

   ### Changed
      - Compiled Postgresql 13 from source to backup psql/13 hosts

## 2.2.2 2020-09-22 <tpansino@github>

   ### Fixed
      - Patch for 2.2.0 release fixing Docker Secrets Support. Was skipping password check.

## 2.2.1 2020-09-17 <alwynpan@github>

   ### Fixed
      - Ondemand/Manual backup with `backup-now` was throwing errors not being able to find a proper date

## 2.2.0 2020-09-14 <alwynpan@github>

   ### Fixed
      - Allow to use MariaDB and MongoDBs with no username and password while still allowing Docker Secrets
      - Changed source of Alpine package repositories


## 2.1.1 2020-09-01 <zicklag@github>

   ### Fixed
      - Add eval to POST_SCRIPT execution


## 2.1.0 2020-08-29 <dave at tiredofit dot ca>

   ### Added
      - Add Exit Code variable to be used for custom scripts - See README.md for placement
      - Add POST_SCRIPT environment variable to execute command instead of relying on custom script


## 2.0.0 2020-06-17 <dave at tiredofit dot ca>

   ### Added
      - Reworked compression routines to remove dependency on temporary files
      - Changed the way that MongoDB compression works - only supports GZ going forward

   ### Changed
      - Code cleanup (removed function prefixes, added verbosity)

   ### Reverted
      - Removed Rethink Support


## 1.23.0 2020-06-15 <dave at tiredofit dot ca>

   ### Added
      - Add zstd compression support
      - Add choice of compression level


## 1.22.0 2020-06-10 <dave at tiredofit dot ca>

   ### Added
      - Added EXTRA_OPTS variable to all backup commands to pass extra arguments


## 1.21.3 2020-06-10 <dave at tiredofit dot ca>

   ### Changed
      - Fix `backup-now` manual script due to services.available change


## 1.21.2 2020-06-08 <dave at tiredofit dot ca>

   ### Added
      - Change to support tiredofit/alpine base image 5.0.0


## 1.21.1 2020-06-04 <dave at tiredofit dot ca>

   ### Changed
      - Bugfix to initalization routine


## 1.21.0 2020-06-03 <dave at tiredofit dot ca>

   ### Added
      - Add S3 Compatible Storage Support

   ### Changed
      - Switch some variables to support tiredofit/alpine base image better
      - Fix issue with parallel compression not working correctly


## 1.20.1 2020-04-24 <dave at tiredofit dot ca>

   ### Changed
      - Fix Auto Cleanup routines when using `root` as username


## 1.20.0 2020-04-22 <dave at tiredofit dot ca>

   ### Added
      - Docker Secrets Support for DB_USER and DB_PASS variables


## 1.19.0 2020-04-22 <dave at tiredofit dot ca>

   ### Added
      - Custom Script support to execute upon compleition of backup


## 1.18.2 2020-04-08 <hyun007 @ github>

   ### Changed
      - Rework to allow passwords with spaces in them for MariaDB / MySQL

## 1.18.1 2020-03-14 <dave at tiredofit dot ca>

   ### Changed
      - Allow for passwords with spaces in them for MariaDB / MySQL


## 1.18.0 2019-12-29 <dave at tiredofit dot ca>

   ### Added
      - Update image to support new tiredofit/alpine base images


## 1.17.3 2019-12-12 <dave at tiredofit dot ca>

   ### Changed
      - Quiet down Zabbix Agent


## 1.17.2 2019-12-12 <dave at tiredofit dot ca>

   ### Changed
      - Re Enable ZABBIX


## 1.17.1 2019-12-10 <dave at tiredofit dot ca>

   ### Changed
      - Fix spelling mistake in container initialization


## 1.17.0 2019-12-09 <dave at tiredofit dot ca>

   ### Changed
      - Stop compiling mongodb-tools as it is back in Alpine:edge repositories
      - Cleanup Code


## 1.16 - 2019-06-16 - <dave at tiredofit dot ca>

* Check to see if Database Exists before performing backup
* Fix for MysQL/MariaDB custom ports - Credit to <spumer@github>

## 1.15 - 2019-05-24 - <claudioaltamura @ github>

* Added abaility to backup password protected Redis Hosts

## 1.14 - 2019-04-20 - <dave at tiredofit dot ca>

* Switch to using locally built mongodb-tools from tiredofit/mongo-builder due to Alpine removing precompiled packages from repositories

## 1.13 - 2019-03-09 - <dave at tiredofit dot ca>

* Fixed Postgres backup without SPLIT_DB enabled (credit MelwinKfr@github)
* Added DB_PORT reference to properly backup Postgres with non default ports (thanks Maxximus007@github)

## 1.12 - 2019-03-01 - <stevetodorov at github>

* Fix for XZ Compression failing

## 1.11 - 2018-11-19 - <skylord123 at github>

* Fix for Urnary Operator Error

## 1.10 - 2018-11-19 - <dave at tiredofit dot ca>

* Fix for InfluxDB for backing up and supporting DB_PORT variable - Thanks skylord123@github

## 1.9 - 2018-11-03 - <dave at tiredofit dot ca>

* Switch from OpenSSL to LibreSSL

## 1.8 - 2018-07-18 - <dave at tiredofit dot ca>

* Fix warnings on startup related to 1.7 Changes

## 1.7 - 2018-06-06 - <dave at tiredofit dot ca>

* Added ability for Manual Backup (enter container and type `backup-now`)

## 1.6 - 2018-02-26 - <dave at tiredofit dot ca>

* Add Parallel Compression mode (Default TRUE

## 1.5 - 2018-01-28 - <dave at tiredofit dot ca>

* Add Zabbix Checks

## 1.4 - 2017-11-17 - <dave at tiredofit dot ca>

* Switch to Packages Postgres

## 1.31 - 2017-11-17 - <dave at tiredofit dot ca>

* Fix to SPLIT_DB Postgresql Backup

## 1.3 - 2017-10-25 - <dave at tiredofit dot ca>

* Remove Alpine postgres package and recompile version 10

## 1.2 - 2017-10-19 - <dave at tiredofit dot ca>

* Syntax Error Fix
* Fix some environment variables for Postgres and Redis

## 1.1 - 2017-09-14 - <dave at tiredofit dot ca>

* Added CouchDB

## 1.0 - 2017-09-14 - <dave at tiredofit dot ca>

* Initial Release
* Alpine:Edge

