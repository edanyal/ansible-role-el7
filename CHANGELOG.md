# Change log

This file contains al notable changes to the EL7 Ansible role. It adheres to the guidelines of [http://keepachangelog.com/](http://keepachangelog.com/). Versioning follows [Semantic Versioning](http://semver.org/).

## 2.0.0 - 2016-05-10

### Changed

- (GH-15) The variable for enabling repositories (`el7_enable_repositories`) was changed so it also works for .repo files with several sections. This change breaks existing playbooks, hence the major version bump.

## 1.4.1 - 2016-04-27

### Changed

- Enabling repos is now idempotent
- Fix Ansible 2.0 deprecation warnings
- Improved task names (include category name, e.g. Install, Security, etc.)
- Fix missing dependency

## 1.4.0 - 2015-11-03

### Added

- (GH-8) Optionally update all packages. Credit [@JeroenED](https://github.com/JeroenED)
- Allow packages to be excluded from an update

## 1.3.0 - 2015-08-24

### Added

- Allow the SELinux state to be configured (was always on)

## 1.2.2 - 2015-08-16

### Changed

- Bugfix: handle the case when the IPv4 address of a network interface is not defined.

## 1.2.1 - 2015-08-18

### Added

- Adding an entry to the hosts file is made optional (still interferes with bertvv.hosts)

## 1.2.0 - 2015-08-18

### Added

- (GH-11) Optionally, install a `/etc/motd` file with info about the host name and IP addresses.

### Changed

- Modified the way the hosts entry in `/etc/hosts` is detected (previous implementation interferes with [bertvv.hosts](https://galaxy.ansible.com/list#/roles/4617))
- Updated the base box for the Vagrant test environment to CentOS 7.1, and add a download link

## 1.1.0 - 2015-03-13

### Added

- (GH-4) Make yum.conf configurable
- (GH-5) Make ports/services allowed by firewalld configurable

### Changed

- (GH-7) Abandon Ansible-specific key=value settings in favour of valid YAML structured map

## 1.0.2 - 2015-01-24

### Added

- Patched ifup scripts that don't overrule some firewalld settings after reboot. This is a workaround for CentOS [bug #7526](https://bugs.centos.org/view.php?id=7526).


## 1.0.1 - 2014-12-12

### Added

- Change log
- Testing section in the README


## 1.0.0 - 2014-12-05

First release!

### Added

- Install external repos from RPM package(s)
- Install packages not in the default installation
- Turn services on or off
- Create users and groups
- Set up SSH key for administrator account
- Apply basic security settings, like turning on SELinux and the firewall

