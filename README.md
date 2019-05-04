# ivansible.dev_packer

Install HashiCorp Packer on Linux
If the host belongs to `permitted` group, this role will also checkout
user's Packer templates.


## Requirements

None


## Variables

    packer_templates_repo: ""
    packer_templates_dir: ~/devel/packer
If current host belongs to the `permitted` group and the URL of Git repository
with user _packer templates_ is defined and not empty, the repository will be
checked out in the given local directory.

    packer_version: latest
Version of the packer binary to install.

    packer_allow_reinstall: no
Allows to override already installed binary.


## Tags

- `ip4only` -- Mark this role as inappropriate for IPv6-only hosts (due to github)
- `dev_packer` -- The whole role
- `dev_packer_install` -- Install Packer binary
- `dev_packer_templates` -- Checkout user's packer templates


## Dependencies

None


## Example Playbook

    - hosts: devbox
      roles:
        - role: ivansible.dev_packer


## License

MIT

## Author Information

Created in 2019 by [IvanSible](https://github.com/ivansible)
