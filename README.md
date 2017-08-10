# Install or remove packages

* list of packages to remove
* list of packages to install
* optionaly update packages

# Usage

Define the Configuration hash some place . Check Examples at defaults/main.yml.ex

## Configuration Capabilities

```yaml
packages:
  remove: # []                     # Optional list of packages to be removed
    # - "libselinux-python"
  install:                         # Optional list of packages to install
    - { name: "libselinux-python", state: "latest" }
    - { name: "bind-utils",        state: "latest" }
    - { name: "nmap" }
  upgrade: True                  # upgrade or not installed packages

```

# License

MIT

# Author Information

Created by Miguel Rodrigues
