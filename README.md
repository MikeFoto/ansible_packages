# Install or remove packages

* Support both yum and apt packages managers
* list of packages to remove
* list of packages to install
* optionaly update packages

# Usage

Define the Configuration hash some place . Check Examples at defaults/main.yml.ex

## Configuration Capabilities

```yaml
packages:
  yum:                           # For Centos/RHEL distros
    remove: # []                 # Optional list of packages to be removed
      # - "libselinux-python"
    install:                         # Optional list of packages to install
      - { name: "libselinux-python", state: "latest" }
      - { name: "bind-utils",        state: "latest" }
      - { name: "nmap" }
    upgrade: True                  # upgrade or not installed packages
  apt:                           # Same options for debian distros
    .......
  tests:                         # optional . lists of shell tests
    - {
        name: test1,
        command: "echo 'test1 succeed' "
      }
    - {
        name: test2,
        command: "echo 'test2 succeed' "
      }

```

# Platforms
* centos
* debian

# License

MIT

# Author Information

Created by Miguel Rodrigues
