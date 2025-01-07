# Ansible role [influxdb2](https://galaxy.ansible.com/localh0rst/ansible-role-influxdb2)

## [Example Playbook](#example-playbook)

```yaml
---
- name: 
  hosts: localhost
  become: yes
  vars:
  roles:
    - role: buluma.influxdb2
      influxdb_orgs:
        - name: main-org
          description: Main organization
        - name: guest-org

      influxdb_users:
        - name: admin01
          org: main-org
          password: secretPassword
        - name: guest01
          org: guest-org
          password: secretPassword

      influxdb_buckets:
        - name: bucket01
          description: First bucket
          org: main-org
          retention: 1d
        - name: bucket02
          org: main-org
```

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-influxdb2/blob/master/defaults/main.yml):

```yaml
---
```

## [Requirements](#requirements)
