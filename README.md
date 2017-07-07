# Grafana Ansible role

This ansible role installs an Grafana server in a debian environment.
The server is installed using pre-packaged  debfile from [Official website](https://grafana.com/grafana/download).

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Versioning](#versioning)
- [Authors](#authors)
- [Thanks to](#thanks-to)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your ansible playbook. Once launched, it will install an [Grafana](https://grafana.com) server in a Debian system.

### Prerequisities

Ansible 2.2.0.0 version installed.
Inventory destination should be a Debian environment.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: http://github.com/eagafonov/ansible_grafana_deb-role.git
  scm: git
  version: master
  name: grafana
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
---
- hosts: someserver
  roles:
    - role: grafana
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

This is thery intial version of the role so there are only a few properties are configured with Ansible variables.

Pull-requests are welcome

## Versioning

For the versions available, see the [tags on this repository](https://github.com/eagafonov/ansible_grafana_deb-role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* [Eugene Agafonov](https://github.com/eagafonov)

See also the list of [contributors](https://github.com/eagafonov/ansible_grafana_deb-role/contributors) who participated in this project.


## Thanks to

* [idealista](https://github.com/idealista) for the base stuff of this role

## License

![Apache 2.0 Licence](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE.txt](LICENSE.txt) file for details.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## TODO

* Testing with molecule/watever
