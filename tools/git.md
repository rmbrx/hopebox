# Git

1. [git status 显示中文和解决中文乱码](https://blog.csdn.net/u012145252/article/details/81775362)

    ```shell
    # 方法一
    git config --global core.quotepath false
    # 方法二
    vi ~/.gitconfig
    [core]
        quotepath = false
    ```
