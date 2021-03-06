# [0.12.6](https://github.com/dashevo/mn-bootstrap/compare/v0.12.5...v0.12.6) (2020-05-23)


### Features

* update Evonet configs ([#56](https://github.com/dashevo/mn-bootstrap/issues/56))



# [0.12.5](https://github.com/dashevo/mn-bootstrap/compare/v0.12.4...v0.12.5) (2020-05-01)


### Bug Fixes

* use updated sentinel image ([#41](https://github.com/dashevo/mn-bootstrap/issues/41))



# [0.12.4](https://github.com/dashevo/mn-bootstrap/compare/v0.12.3...v0.12.4) (2020-04-30)


### Bug Fixes

* MongoDB replica set doesn't work sometimes ([#40](https://github.com/dashevo/mn-bootstrap/issues/40)) ([a5e31cd](https://github.com/dashevo/mn-bootstrap/commit/a5e31cd341bfd3e18240e3ee4c8f5dfeebfd249c))



# [0.12.3](https://github.com/dashevo/mn-bootstrap/compare/v0.12.2...v0.12.3) (2020-04-28)


### Bug Fixes

* outdated genesis config for Tendermint ([#37](https://github.com/dashevo/mn-bootstrap/issues/37))
* outdated persistent node IDs in Tendermint config ([#38](https://github.com/dashevo/mn-bootstrap/issues/38))



## [0.12.2](https://github.com/dashevo/mn-bootstrap/compare/v0.12.1...v0.12.2) (2020-04-22)


### Bug Fixes

* update DPNS identities for evonet ([#31](https://github.com/dashevo/mn-bootstrap/issues/31))


## [0.12.1](https://github.com/dashevo/mn-bootstrap/compare/v0.11.1...v0.12.0) (2020-04-21)


## Bug Fixes

* `latest` envoy docker image tag is not present anymore ([#29](https://github.com/dashevo/mn-bootstrap/issues/29))


# [0.12.0](https://github.com/dashevo/mn-bootstrap/compare/v0.11.1...v0.12.0) (2020-04-19)


### Bug Fixes

* dash-cli doesn't work without default config ([#18](https://github.com/dashevo/mn-bootstrap/issues/18))
* explicitly load core conf file ([#23](https://github.com/dashevo/mn-bootstrap/issues/23))
* invalid gRPC Web configuration ([#25](https://github.com/dashevo/mn-bootstrap/issues/25), [#26](https://github.com/dashevo/mn-bootstrap/issues/26))
* remove spork private key from сore config ([#11](https://github.com/dashevo/mn-bootstrap/issues/11))


### Code Refactoring

* tidy up services and configs ([#27](https://github.com/dashevo/mn-bootstrap/issues/27))


### Features

* add testnet preset ([#15](https://github.com/dashevo/mn-bootstrap/issues/15))
* update to new Drive ([#21](https://github.com/dashevo/mn-bootstrap/issues/21), [#24](https://github.com/dashevo/mn-bootstrap/issues/24))


### BREAKING CHANGES

* data and config dir paths are changed
* `tendermint` service now called `drive_tendermint`
* `machine` is removed due to merging Machine into Drive
* new version of Drive is incompatible with 0.11 so you need to wipe data before run 0.12:
  * drop `drive_mongodb` and `drive_leveldb` volumes
  * `docker-commpose --env-file=.env.<PRESET> run drive_tendermint unsafe_reset_all`


## 0.11.1 (2020-03-17)


### Bug Fixes

*  update configs for Evonet ([#7](https://github.com/dashevo/mn-bootstrap/issues/7))


# 0.11.0 (2020-03-09)


### Features

* update configurations and docker-compose file for `local` and `evonet` envs ([230ea62](https://github.com/dashevo/mn-bootstrap/commit/230ea62a856b986127eb3b8e52bf7a19a5169818))


### BREAKING CHANGES

* `testnet` and `mainnet` is not supported anymore
