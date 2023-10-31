# Workspace for Ansible

Predefined tasks for Visual Studio code. These can be used to test Ansible roles and collections.

After opening the `bec-galaxy.code-workspace` file, the following shortcuts are available under the Tasks `Terminal->Run Task…` menu:

| Befehl               | Beschreibung                                  |
| -------------------- | --------------------------------------------- |
| 🧬 molecule test      | Performs a complete test.                     |
| 🧬 molecule converge  | Performs a quick test without destroy.        |
| 🧬 molecule verify    | Performs a quick test without destroy.        |
| 🧬 molecule login     | Opens a shell on the quick test container.    |
| 🧬 molecule destroy   | Use the provisioner to destroy the instances. |
| 🔑 ansible-vault edit | Edits the current selected vault file.        |

### Preparation

Install Ansible and the Molecule testing Framework with the required dependencies using this command:
```
pip install --user ansible ansible-lint molecule molecule-plugins docker
```

Upgrade existing packages with this command:
```
pip install --upgrade --user ansible ansible-lint molecule molecule-plugins docker
```

> Install the package only in the user context, depending on the environment installing python packages as root can cause problems. If any Ansible packages were previously installed as root, it is recommended to uninstall these packages first.

## Molecule

To test a ansible-collection e.g. after changes, Molecule tasks are included.

Molecule is executed in the currently selected project.
