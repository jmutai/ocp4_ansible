## OpenShift 4 Ansible tasks and Jinja templates for Bastion/Helper Node setup

Here is the directory structure of all the files in this directory:

```bash
$ tree
.
├── LICENSE
├── README.md
├── ansible.cfg
├── files
│   └── set-dns-serial.sh
├── handlers
│   └── main.yml
├── inventory
├── tasks
│   ├── configure_bind_dns.yml
│   ├── configure_dhcpd.yml
│   ├── configure_haproxy_lb.yml
│   ├── configure_tftp_pxe.yml
│   └── validate_host_names.yaml
├── templates
│   ├── default.j2
│   ├── dhcpd-uefi.conf.j2
│   ├── dhcpd.conf.j2
│   ├── haproxy.cfg.j2
│   ├── named.conf.j2
│   ├── pxe-bootstrap.j2
│   ├── pxe-master.j2
│   ├── pxe-worker.j2
│   ├── reverse.j2
│   └── zonefile.j2
└── vars
    └── main.yml
```

The `tasks` folder contain all the tasks to configure:
- Bind DNS server
- DHCP Server
- HAProxy Load balancer
- PXE / TFTP Server
