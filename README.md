## Image Builder

用于创建 Cluster-API-Provider-Elf 所需模板。

### 创建流程
1. 在 Elf 平台创建虚拟机，操作系统选择 CentOS7 Minimal
2. 安装 SMTX vmtools（由于 ISO 文件过大，耗时过长，因此不在 Ansible 中处理该问题
3. 编辑 inventory 文件，填写对应 IP，用户名，密码
4. `export ANSIBLE_HOST_KEY_CHECKING=False`
5. `ansible-playbook -i inventory playbook.yml`
6. 安装完成后，将虚拟机关机，并克隆为虚拟机模板
