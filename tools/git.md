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

2. git 忽略目录，但不忽略其下某个文件
    .gitignore如下配置，达到忽略node_modules目录，但不忽略其下fileSaver的效果。

    ```markdown
    /node_modules/*
    !/node_modules/fileSaver
    ```
