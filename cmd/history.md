---
---
# history - 查看命令行历史

## 附加命令

| 命令                   | 描述                         |
| ---------------------- | ---------------------------- |
| `!n`（`n` 是命令编号） | 再次执行第 `n` 行历史命令    |
| `!!`                   | 执行上一条命令               |
| `!$`                   | 返回上一条命令的最后一个参数 |

## 示例

```sh
$ cat /etc/hosts | grep -i '127.0.0.1' -A 1
127.0.0.1	localhost
255.255.255.255	broadcasthost

$ echo !$
echo 1
1
```
