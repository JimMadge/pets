# Pets

Configuration management for my pets 🐱🐶🐰

## Example playbook

```yaml
---

- hosts: localhost

  vars:
    user_password: "{{ 'mypassword' | password_hash('sha512', 'mysecretsalt') }}"

  roles:
    - pets
```
