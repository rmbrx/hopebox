# jenkins流水线

## 简介

### Jenkins 流水线是什么

- 一套插件
- 提供了一组可扩展的工具
- 通过流水线 DSL 将简单到复杂的交付流水线建模为“代码”
- DSL(domain specific language 领域专用语言)

### 为什么要用流水线？

### 怎么用流水线？

- pipeline as code
  - 独立的Jenkinsfile代码库（Pipeline script from SCM，推荐）
  - 共享库的方式（系统配置/Global Pipeline Libraries）
  - 跟随代码的Jenkinsfile（多分流水线）
- 静态Jenkinsfile（Pipeline script）、

## 流水线语法

### Declarative vs. scripted pipelines

#### 声明式流水线

```pipeline
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                //
            }
        }
        stage('Test') {
            steps {
                //
            }
        }
        stage('Deploy') {
            steps {
                //
            }
        }
    }
}
```

agent: 指示 Jenkins 为整个流水线分配一个执行器（在 Jenkins 环境中的任何可用代理/节点上）和工作区。

- 优先选择使用
- 使用声明式编程模型
- 简单易用
- 隔离复杂逻辑：插件，共享库
- 将复杂的代码排除在流水线之外一直是最佳实践，声明式管道强制执行此操作

#### 脚本化流水线

```pipeline
node {
    stage('Build') {
        //
    }
    stage('Test') {
        //
    }
    stage('Deploy') {
        //
    }
}
```

node: 与声明式流水线中的 agent 做了同样的事情（分配执行器和工作区）。

- 不推荐使用
- 使用命令式编程模型
- 可自由嵌入groovy脚本
- 可使用groovy实现所需功能
- 过于复杂，不易阅读，不易管理
- 熟悉Groovy不甚熟悉DSL的人造轮子
- 永远不要将复杂的代码放入管道中，无论它看起来是否可行

### 效率工具与变量

#### 片段生成器

- JENKINS_URL/pipeline-syntax

#### 声明式指令生成器

- Declarative Directive Generator
- JENKINS_URL/directive-generator
- 生成嵌套的指令配置
- when 指令内的条件
- stage 内的 steps 或 post 内的条件如 always 或 failure

#### 全局环境变量

- JENKINS_URL/pipeline-syntax/globals
- env.PATH
- env.BUILD_ID

#### 参数

- 流水线定义的所有参数作为Map
- params.MY_PARAM_NAME

#### currentBuild

- JENKINS_URL/pipeline-syntax/globals
- currentBuild.result
- currentBuild.displayName

## 参考文档

- [Declarative vs. scripted pipelines](https://www.theserverside.com/answer/Declarative-vs-scripted-pipelines-Whats-the-difference)
- [流水线语法](https://www.jenkins.io/zh/doc/book/pipeline/syntax/)
- [Jenkins2 流水线核心语法_GitChat-CSDN博客](https://blog.csdn.net/valada/article/details/104272154)