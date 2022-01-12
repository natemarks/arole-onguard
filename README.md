# natemarks/onguard

```yaml
---
# example playbook
- hosts: localhost
  become: false
  vars:
    # defaults
    download: "{{ ansible_env.HOME }}/.onguard_downloads"
    extract: "{{ download }}/onguard"
    installer:  ClearPassOnGuardInstall.tar.gz
    # required
    aws_access_key_id: AAAAAAA
    aws_secret_access_key: abc123
    s3_uri: "s3://my_bucket/ClearpassOnguard/linux/ClearPassOnGuardInstall.tar.gz"
  roles:
    - /opt/ansible/onguard
```
