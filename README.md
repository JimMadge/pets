# Pets

Configuration management for my pets 🐱🐶🐰

## Tags

Tags can be used (with the `--tags` flag) to control which parts of the role are
run.

| tag      | tasks                                                     |
|----------|-----------------------------------------------------------|
| packages | Install common packages for every distributon             |
| user     | User configuration including SSH keys and dotfiles        |
| arch     | Arch specific configuration (arch packages, pacman hooks) |

## Example playbook

```yaml
---

- hosts: localhost

  vars:
    user_password: "{{ 'mypassword' | password_hash('sha512', 'mysecretsalt') }}"

  roles:
    - pets
```
