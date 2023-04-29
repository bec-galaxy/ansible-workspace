# Workspace for Ansible

Predefined tasks for Visual Studio code. These can be used to test Ansible roles and collections.

After opening the `ansible.code-workspace` file, the following shortcuts are available under the Tasks `Terminal->Run Task…` menu:

| Befehl               | Beschreibung                                  |
| -------------------- | --------------------------------------------- |
| 🧬 molecule test      | Performs a complete test.                     |
| 🧬 molecule converge  | Performs a quick test without destroy.        |
| 🧬 molecule verify    | Performs a quick test without destroy.        |
| 🧬 molecule login     | Opens a shell on the quick test container.    |
| 🧬 molecule destroy   | Use the provisioner to destroy the instances. |
| 🔑 ansible-vault edit | Edits the current selected vault file.        |


## Molecule

To test a ansible-collection e.g. after changes, Molecule tasks are included.

Molecule is executed in the currently selected project.

### Preparation

The test framework molecule can be installed with [this packages](https://github.com/bec-galaxy/setup-molecule/blob/main/requirements.txt).

## WSL

With a shortcut, the workspace can be opened directly in Ubuntu (WSL).

```shell
"C:\Program Files\Microsoft VS Code\bin\code.cmd" --remote wsl+Ubuntu "/home/<your-path>/ansible-workspace/ansible.code-workspace"
```

> Set the `Run` property to `Minimized` to hide the terminal when opening the workspace.