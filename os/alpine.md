# alpine

## 常用命令

1. 从远程镜像源中更新本地镜像源索引 `apk update`
2. 安装PACKAGES并自动解决依赖关系 `apk add`
3. 卸载并删除PACKAGES `apk del`
4. 升级当前已安装的软件包 `apk upgrade`
5. 搜索软件包 `apk search`
6. 列出PACKAGES或镜像源的详细信息 `apk info`

## 使用国内源

```shell
echo -e "https://mirrors.aliyun.com/alpine/v3.7/main" > /etc/apk/repositories
```

## 容器化

### 问题

alpine 3.4~3.9（后面版本未验证），k8s集群部署，coredns配置的域名服务器，在容器中无法解析地址。
[kubernetes-dns-resolution-ndots-options-and-why-it-may-affect-application-performances.html](https://pracucci.com/kubernetes-dns-resolution-ndots-options-and-why-it-may-affect-application-performances.html)
[解决Kubernetes Pod DNS超时问题_每天进步一点的技术博客_51CTO博客](https://blog.51cto.com/kusorz/2387623)
[musl dns client  stop further search domain when one search domain return something unexpected. (#9017) · Issues · alpine / aports](https://gitlab.alpinelinux.org/alpine/aports/-/issues/9017)
[ndots breaks DNS resolving · Issue #64924 · kubernetes/kubernetes](https://github.com/kubernetes/kubernetes/issues/64924)
[DNS Issue · Issue #255 · gliderlabs/docker-alpine](https://github.com/gliderlabs/docker-alpine/issues/255)
[一场纠结，事关Microk8s，Alpine和kubedns_pushme_pli的专栏-CSDN博客_alpine k8s](https://blog.csdn.net/pushme_pli/article/details/91351247)
[kubernetes-alpine-image-resolve-ext-dns](https://www.sudops.com/kubernetes-alpine-image-resolve-ext-dns.html)
[DNS ndots的使用](https://juejin.cn/post/6844903951393882125)
