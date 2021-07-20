# jenkins流水线

## 简介

### Jenkins 流水线是什么

- 一套插件
- 提供了一组可扩展的工具
- 通过DSL将交付流水线建模为“代码”

## 为什么要用流水线？

### 代码化（pipeline as code）

流水线是在代码中实现的，通常会存放到源代码控制，使团队具有编辑、审查和更新他们项目的交付流水线的能力。

### 耐用性

流水线可以从 Jenkins 的 master 节点重启后继续运行。

### 可暂停的

流水线可以由人功输入或批准继续执行流水线。

### 解决复杂发布

支持复杂的交付流程。例如循环、并行执行。

### 可扩展性

支持扩展 DSL 和其他插件集成。

## 怎么用流水线？

1. 共享库的方式
2. Jenkinsfile和
3. 静态Jenkinsfile（直接配置的流水线）

## 流水线语法

[流水线语法](https://www.jenkins.io/zh/doc/book/pipeline/syntax/)

[Jenkins2 流水线核心语法_GitChat-CSDN博客](https://blog.csdn.net/valada/article/details/104272154)
