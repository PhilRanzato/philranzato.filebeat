philranzato.filebeat
=========

Install and configure filebeat

Requirements
------------

None.

Role Variables
--------------

```yaml
---
# Wheter to install filebeat
install: true
# Wheter to configure filebeat
configure: true

# Logstash hosts that will be targeted
logstash_hosts:
- "logstash1.test.net"
- "logstash2.test.net"

# SSL parameters
ssl:
  enabled: true
  # Wheter to upload CA to the host
  ca.upload: false
  # Wheter to upload filebeat certificates to the host
  ca.path: /path/to/ca.pem
  certificate.upload: false
  # Certificates parameters
  certificate.cert: /path/to/cert.pem
  certificate.key: /path/to/key.pem
  certificate.key_passphrase: "F1lebeat!"
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- name: "Install and Configure Filebeat"
  hosts: servers
  roles:
  - { role: philranzato.filebeat }
  vars_files:
  - vars/filebeat.yml
```

License
-------

MIT License

Author Information
------------------

Get in touch with me at:
- [LinkedIn](www.linkedin.com/in/phil-ranzato-47b8bb194)
- [GitHub](https://github.com/PhilRanzato)
- [Medium](https://medium.com/@philranzato)
