## Image Builder

用于创建 Cluster-API-Provider-Elf 所需模板。

### 创建流程
1. 在 Elf 平台创建虚拟机，操作系统选择 CentOS7 Minimal
2. 编辑 inventory 文件，填写对应 IP，用户名，密码
3. `export ANSIBLE_HOST_KEY_CHECKING=False`
4. `ansible-playbook -i inventory playbook.yml`
