# 🔧 Ansible Lab — Create a File on Remote Server

This repository contains a basic Ansible project to demonstrate automation of a simple task: **creating a file on a remote Linux server**.

---

## 📌 Context

In real-world system administration or DevSecOps, we often need to:

- Apply changes to remote servers automatically.
- Avoid manual SSH into each server.
- Use one tool (like Ansible) to describe and apply actions in a repeatable way.

This lab simulates such a task, using a **playbook** and a **static inventory file** to target one server and create a file.

---

## 📁 Project Structure

ansible-lab-create-file/
│
├── README.md ← This documentation
├── inventory ← Static INI inventory
└── playbook.yml ← Ansible playbook with task




---

## 🔧 Technologies

- ✅ Ansible
- ✅ Linux SSH
- ✅ YAML

---

## 🧠 What I Learned

- Structure and syntax of an **Ansible playbook**
- How to write a **task** using the `file` module
- Use of an **inventory file** to define remote hosts
- Execution of a playbook using `ansible-playbook`

---

## 🧱 Playbook Structure (Reminder)

name: <Play Name>
hosts: <target_group_or_host>
tasks:

name: <Task Name>
<ansible_module>:
param1: value1
param2: value2



> ✅ Important: YAML format is space-sensitive. Use **spaces**, not tabs. Indentation matters.

---

## 📜 playbook.yml

```yaml
- name: Create file on App Server 2
  hosts: stapp02
  tasks:
    - name: Create empty file /tmp/file.txt
      file:
        path: /tmp/file.txt
        state: touch

## 🧱 inventory

stapp02 ansible_host=172.16.238.11 ansible_user=steve ansible_ssh_pass="Am3ric@" ansible_ssh_common_args="-o StrictHostKeyChecking=no"
## 🧱 how to run
ansible-playbook -i inventory playbook.yml


