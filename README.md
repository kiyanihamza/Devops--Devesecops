# Ansible Lab — Create a File on Remote Server

This is a simple Ansible lab exercise demonstrating how to use Ansible to create a file on a remote Linux server.

## 🧠 What I Learned

- How to define a static inventory in INI format.
- How to write a basic Ansible playbook using the `file` module.
- How to run `ansible-playbook` with a custom inventory file.
- Managing remote server tasks over SSH without installing an agent.

## ✅ What I Did

- Configured the Ansible inventory to connect to a remote host.
- Wrote a playbook to create an empty file `/tmp/file.txt` on the remote server.
- Executed the playbook with the command:

```bash
ansible-playbook -i inventory playbook.yml
