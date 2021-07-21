# jenkins流水线

## 简介

### Jenkins 流水线是什么

- 一套插件
- 提供了一组可扩展的工

## 为什么要用流水线？

## 怎么用流水线？

- pipeline as code
  - 共享库的方式
  - 跟随代码的Jenkinsfile
- 静态Jenkinsfile

## 效率工具

### 片段生成器

- JENKINS_URL/pipeline-syntax

### 声明式指令生成器

- JENKINS_URL/directive-generator
- 生成嵌套的指令配置
- when 指令内的条件
- stage 内的 steps 或 post 内的条件如 always 或 failure

## 流水线语法

### 全局变量

#### env

- JENKINS_URL/pipeline-syntax/globals
- env.PATH
- env.BUILD_ID

#### params

- 流水线定义的所有参数作为Map
- params.MY_PARAM_NAME

#### currentBuild

- JENKINS_URL/pipeline-syntax/globals
- currentBuild.result
- currentBuild.displayName

[流水线语法](https://www.jenkins.io/zh/doc/book/pipeline/syntax/)

[Jenkins2 流水线核心语法_GitChat-CSDN博客](https://blog.csdn.net/valada/article/details/104272154)
