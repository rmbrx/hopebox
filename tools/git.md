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

    ```shell
    /node_modules/*
    !/node_modules/fileSaver
    ```

3. 推送时报错

    ```shell
    warning: ----------------- SECURITY WARNING ----------------
    warning: | TLS certificate verification has been disabled! |
    warning: ---------------------------------------------------
    warning: HTTPS connections may not be secure. See https://aka.ms/gcmcore-tlsverify for more information.
    ```

    检查发现，因为之前使用其他代码仓库时，因其证书问题，暂时不做验证（`git config http.sslVerify`为false），只要将其改成true即可:`git config --global http.sslVerify true`。
