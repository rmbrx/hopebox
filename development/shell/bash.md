# bash

## 常用参数

| 参数 | 作用 | 示例 |
| --- | --- | --- |
| -s | 传参 | `curl url/test.sh | bash -s p1 p2 p3`  |
| -x | 调试 | `bash -x x.sh` |

## 获取参数

| 参数处理 | 说明 |
| --- | --- |
| $# | 参数个数 |
| $* | 所有参数, "$*" = "$1 $2 … $n" |
| $@ | 所有参数, "$@" = "$1" "$2""$3" … "$n" |
| $$ | 脚本运行的当前进程ID号 |
| $! | 后台运行的最后一个进程的ID号|
| $- | 显示Shell使用的当前选项，与set命令功能相同 |
| $? | 显示最后命令的退出状态。0表示没有错误，其他任何值表明有错误 |
| $0 | 文件名 |
| $1 | 第1个参数，第n个参数用$n，n为数字 |

## 判断

## 循环
