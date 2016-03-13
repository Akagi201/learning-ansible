## `ansible` 配置文件的位置
* `ANSIBLE_CONFIG` (环境变量)
* `ansible.cfg` (当前目录下)
* `.ansible.cfg` (用户家目录下)
* `/etc/ansible/ansible.cfg`

## 在命令行中指定 `hosts` 文件
* `ansible -i hosts all -a 'who'`
* `-a`: 表示是 `ad-hoc` 命令, 临时执行命令.
* `all`: 表示 `hosts`中的所有服务器.
* `ansible -i hosts local -a 'who'` 根据组名指定服务器.

## 从 `ansible.cfg` 中的配置读取指定的 `hosts` 文件

```
# ansible.cfg
[defaults]
hostfile=./hosts
```
* 这样下次执行就不需要 `-i` 参数了.
* `ansible local -a 'who'`

## 模块
* `ansible -i hosts all -m command -a 'who'`
* `ansible -i hosts all -m ping`
