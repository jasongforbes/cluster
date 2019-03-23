# Ansible Playbooks for Raspbi Cluster

This project is directly inspired by [Rak8s](https://github.com/rak8s/rak8s).

To run this playbook:

```bash
ansible-playbook cluster.yml --ask-become-pass
```

The first time you run this, you will want to set `remote_user` to a known user, such as `pi`.

## Configuration

* For each device, set up a static-route.
  * Change the routes in the `hosts.ini` file correspondingly

### `ansible.cfg`

* `host_key_checking = False`
  * Do not check ssh fingerprint.
* `inventory = hosts.ini`
  * Location for hosts file. Overrides `/etc/ansible/hosts`.
* `log_path = ansible.log`
  * Log file path.
* `remote_user = kube`
  * the user to execute the playbook
