# Jenkins 运维

## 安装jenkins

## 维护

### 重启

`JENKINS_URL/restart/`

## 问题及解决方法

### 安装时无法安装插件

1. 原因是默认updateCenter不可用的
    修改updateCenter，即修改`JENKINS_HOME/hudson.model.UpdateCenter.xml`文件。当然，也可以跳过后进入jenkins再设置UC地址，只是这样还要自行选择需要安装的插件，不如安装时方便。

    ```xml
    <?xml version=‘1.0‘ encoding=‘UTF-8‘?>
    <sites>
    <site>
        <id>default</id>
        <url>https://mirrors.tuna.tsinghua.edu.cn/jenkins/updates/stable-2.7/update-center.json</url>
    </site>
    </sites>
    ```

### 安装后无法安装插件

1. 原因是默认updateCenter不可用的
    `系统管理 / 插件管理 / 高级 / 升级站点 / URL` 改成 `https://mirrors.tuna.tsinghua.edu.cn/jenkins/updates/stable-2.7/update-center.json`，点击“提交”按钮。
