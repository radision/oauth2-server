# Changelog

## 2.0.0 (released 2013-05-06)

**If you're upgrading from v1.0.8 there are lots of breaking changes**

* Rewrote the session storage interface from scratch so methods are more obvious
* Included a PDO driver which implements the storage interfaces so the library is more "get up and go"
* Further normalised the database structure so all sessions no longer contain infomation related to authorization grant (which may or may not be enabled)
* A session can have multiple associated access tokens
* Induvidual grants can have custom expire times for access tokens
* Authorization codes now have a TTL of 10 minutes by default (can be manually set)
* Refresh tokens now have a TTL of one week by default (can be manually set)
* The client credentials grant will no longer gives out refresh tokens as per the specification

## 1.0.8 (released 2013-03-18)

* Fixed check for required state parameter
* Fixed check that user's credentials are correct in Password grant

## 1.0.7 (released 2013-03-04)

* Added method `requireStateParam()`
* Added method `requireScopeParam()`

## 1.0.6 (released 2013-02-22)

* Added links to tutorials in the README
* Added missing `state` parameter request to the `checkAuthoriseParams()` method.

## 1.0.5 (released 2013-02-21)

* Fixed the SQL example for SessionInterface::getScopes()

## 1.0.3 (released 2013-02-20)

* Changed all instances of the "authentication server" to "authorization server"

## 1.0.2 (released 2013-02-20)

* Fixed MySQL create table order
* Fixed version number in composer.json

## 1.0.1 (released 2013-02-19)

* Updated AuthServer.php to use `self::getParam()`

## 1.0.0 (released 2013-02-15)

* First major release