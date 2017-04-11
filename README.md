PHP
===

This Ansible role will create a self-signed SSL certificate.

Role Variables
--------------

The following variables are used by this role. The default settings (found in `defaults/main.yml`) are as follows:

```yaml
---

dev_ssl_base_dir: /etc/dev-ssl
dev_ssl_domains: [ '{{ ansible_fqdn }}' ]
dev_ssl_base_domain: '{{ dev_ssl_domains[0] }}'
dev_ssl_email: 'dev@example.com'
```

Example requirements.yml
------------------------

```yml
---

- src: git+git@code.siftware.com:ansible/dev-ssl-self-signed.git
  version: "1.0"
  name: siftware.dev-ssl-self-signed
```

Example Playbook
----------------

An example playbook of how to use the role.

```yaml
---

- hosts: all
  roles:
  - siftware.dev-ssl-self-signed
```

License
-------

MIT

Author Information
------------------

Written by Iain Cuthbertson of [Siftware Ltd](http://siftware.com/)
