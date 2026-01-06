# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0](https://github.com/nat-vpn/opennhp/compare/v0.6.0...v1.0.0) (2026-01-06)


### ⚠ BREAKING CHANGES

* **crypto:** The cipher scheme numeric values have changed. Existing configurations with DefaultCipherScheme=0 will now use CURVE instead of GMSM. To maintain GMSM, change the value to 1.

### Features

* add cool startup banners with version info for all NHP components ([c25d138](https://github.com/nat-vpn/opennhp/commit/c25d138e7e7da3c1b2fa5d2994b16b7a8e8c9089))
* add multi-language support, dual IP display, footer sponsor info ([086a437](https://github.com/nat-vpn/opennhp/commit/086a4371044285c99ea2592ec53ca6e6c410808f))
* add nhp-agent to Docker debugging environment ([a8fe76a](https://github.com/nat-vpn/opennhp/commit/a8fe76a70b9129913c67b7dac55a5359b2fbd97d))


### Bug Fixes

* add bounds checking to prevent panics from malformed input ([#1358](https://github.com/nat-vpn/opennhp/issues/1358)) ([6508248](https://github.com/nat-vpn/opennhp/commit/65082485c68a9e851304312eae48f4587fafeea8))
* **ci:** Skip latest-release job on pull requests ([2228f55](https://github.com/nat-vpn/opennhp/commit/2228f550790f4e7ce5f3bf89aca92a7b46085ed5))
* **ci:** Skip latest-release job on pull requests ([9855cd6](https://github.com/nat-vpn/opennhp/commit/9855cd61e8945b565b1c4c83ad0108ecf1fcdde3))
* **ci:** Update Go version and fix grpc-gcp-go dependency ([9e76211](https://github.com/nat-vpn/opennhp/commit/9e762115633a706d304251a7e0e44740df6b617b))
* **ci:** Update Go version to 1.24 in build-binaries workflow ([c152689](https://github.com/nat-vpn/opennhp/commit/c152689971b42f7c06767f772c617fce4de66380))
* **crypto:** change default cipher scheme from GMSM to CURVE ([#1330](https://github.com/nat-vpn/opennhp/issues/1330)) ([96baabd](https://github.com/nat-vpn/opennhp/commit/96baabd75bbe98788d03e6fb170e05197a6bec81))
* demo templates ([1f50bf1](https://github.com/nat-vpn/opennhp/commit/1f50bf181f33a26863c8ddd9b47a0ee5adfed62b))
* **deps:** Upgrade grpc-gcp-go to v1.6.0 for grpc v1.78.0 compatibility ([ae58134](https://github.com/nat-vpn/opennhp/commit/ae58134e93964975e45ace768515146138ebc718))
* image path issue in the doc ([4d9b4df](https://github.com/nat-vpn/opennhp/commit/4d9b4df6ab9beee81228d43fbdf1f35b6ac9a7dc))
* **iptables:** fix rsyslog typo, permission issues and add log cleanup ([6e0f81c](https://github.com/nat-vpn/opennhp/commit/6e0f81c3f37a983501907ffea3696467782fd208))
* **ipv6:** fix critical bugs in IPv6 support implementation ([2261567](https://github.com/nat-vpn/opennhp/commit/22615674fc9fc7c46eb5bc0c14a37f0d125c3192))
* **ipv6:** fix critical bugs in IPv6 support implementation ([27e3d6b](https://github.com/nat-vpn/opennhp/commit/27e3d6bcfd2a2602635b46b83b678a485a362eaf))
* **ipv6:** implement full IPv6 support for iptables and AC ([#1329](https://github.com/nat-vpn/opennhp/issues/1329)) ([9ed0cf6](https://github.com/nat-vpn/opennhp/commit/9ed0cf6c059919e04de95c72c5747eff46c97022))
* Optimize quick start doc ([64cdee8](https://github.com/nat-vpn/opennhp/commit/64cdee8183f3c5be5d38680e5e5958d005dd037e))
* prevent panics discovered by fuzz testing ([6534cf6](https://github.com/nat-vpn/opennhp/commit/6534cf632eed48b546fc4a6b3e64230f2fdcd2c2))
* prevent panics in crypto, peer, and compression functions ([1b69b37](https://github.com/nat-vpn/opennhp/commit/1b69b375b83cd02acf76afb8b5a5f2db8579901b))
* rename remote.toml to remote.toml.example to disable etcd by default ([00b8bdb](https://github.com/nat-vpn/opennhp/commit/00b8bdb26ef9418721d3a3de7aea969065f8cb64))
* **security:** Upgrade golang.org/x/crypto to v0.46.0 in examples/server_plugin ([7f3934a](https://github.com/nat-vpn/opennhp/commit/7f3934a4a4a69be07874b424bf512ec392c23a76))
* **security:** Upgrade golang.org/x/crypto to v0.46.0 in examples/server_plugin ([dfb1ee3](https://github.com/nat-vpn/opennhp/commit/dfb1ee30f6cb63fe6e396f7c98339af463d2f90b))
* sync plugin dependencies with endpoints to fix version mismatch ([4226842](https://github.com/nat-vpn/opennhp/commit/422684228cc3fdd582eec0018aa72e6e3b32db82))
* **utils:** use format specifiers in fmt.Errorf calls ([cfa028d](https://github.com/nat-vpn/opennhp/commit/cfa028db55392700292c53fe6e3409727c3309aa))
* **utils:** use format specifiers in fmt.Errorf calls ([c797179](https://github.com/nat-vpn/opennhp/commit/c7971799eb134b6fbcba2bb9232189456e10ce8d))

## [Unreleased]

## [0.6.0] - 2025-06-11

### Added
- eBPF/XDP packet filtering support for high-performance knocking
- Docker local debugging environment
- `PASS_KNOCKIP_WITH_RANGE` mode for AC to include IP address ranges

### Changed
- Refactored peer hostname resolve logic
- Aligned UDP open resource behavior with HTTP version
- Server now continues when AC connections are lost in resource groups

### Fixed
- CGO compilation issues
- Escape mod bug
- Possible nil pointer dereference
- Size comparison error

## [0.5.0] - 2025-04-13

### Added
- Plugin system for NHP-Server with separate modules
- Improved build system for server plugins

### Changed
- Separated modules to accommodate building of nhp-serverd and its plugins

## [0.4.1] - 2025-04-06

### Added
- DHP (Data Hiding Protocol) function code
- SM2 P256 ECDH curve support
- Default cipher scheme configuration for DE

### Changed
- Using GMSM as default cipher scheme
- Updated Makefile for building DE on Linux

### Fixed
- Removed redundant logging
- Fixed SM2 P256 ECDH curve usage

## [0.4.0] - 2024-09-04

### Added
- Initial public release
- Jekyll-based documentation site
- GitHub Pages deployment

### Changed
- Updated code structure and symbols to be more self-explanatory

## [0.3.6] - 2024-09-03

### Added
- Pre-release version with core NHP protocol implementation
- Agent, Server, and AC components
- Noise Protocol Framework integration
- Curve25519 and SM2 cipher scheme support

[Unreleased]: https://github.com/OpenNHP/opennhp/compare/v0.6.0...HEAD
[0.6.0]: https://github.com/OpenNHP/opennhp/compare/v0.5.0...v0.6.0
[0.5.0]: https://github.com/OpenNHP/opennhp/compare/v0.4.1...v0.5.0
[0.4.1]: https://github.com/OpenNHP/opennhp/compare/v0.4.0...v0.4.1
[0.4.0]: https://github.com/OpenNHP/opennhp/compare/v0.3.6...v0.4.0
[0.3.6]: https://github.com/OpenNHP/opennhp/releases/tag/v0.3.6
