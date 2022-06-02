1. 该应用通过 NodePort 暴露出去，端口配置可参见 values.yaml 中 service.nodePort 字段，可使用任一节点 ip 的 NodePort （默认为 30802）访问，如
```console
https://{节点ip}:30802
```

2. 该 Chart 包来源自 https://docs.redis.com/latest/ri/installing/install-k8s/
   修改添加持久化 PVC 配置
