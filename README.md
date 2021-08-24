# ansible-role-lxd_exporter

Installs the LXD Exporter for Prometheus.


# Requirements

# Role Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `lxd_exporter_version`| Version of the exporter to use | `0.7.1` |
| `lxd_exporter_tarball_checksum` | checksum of the tarball | sha1 checksum of 0.7.1 tarball |
| `lxd_exporter_options`| Command line options | ['-haproxy.scrape-uri=http://admin:admin@localhost:9101/haproxy?stats;csv'] |

Other variables are in defaults/main.yml


# Dependencies

    `bdellegrazie.ansible-role-prometheus_exporter`

# Example Playbook

    - hosts: all
      roles:
        - { role: marianschmotzer.lxd_exporter }

# License

GPLv3

Author Information
------------------
https://github.com/marianschmotzer/lxd_exporter.git

Based on 

https://github.com/bdellegrazie/ansible-role-haproxy_exporter
