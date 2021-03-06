#### 1. 简述
   - 目的：通过封装常见中间件为 Chart 包，并微调默认配置项，减少学习部署成本。
   - 学习成本：如
      - **提供形式不一**：如 Helm Chart、Operator、docker image、纯源代码形式等；
      - **配置不一**：如控制暴露形式不同 (ClustorIP、NodePort)，持久化 pvc 策略不同等；
      - ......
   - 备注：
      - 但包装微调后，自然无法自动享受开源更新
         - 建议时常更新该仓库
         - 在对 K8S 有基础的前提下，建议直接获取源端部署
      - 常见源端如：
         - [artifact-hub](https://artifacthub.io/)：Helm 官方仓库
         - [github](https://github.com/)：常见形式如 {}-operator，如 rocketmq-operator
         - [bitnami](https://bitnami.com/)：出版多，更新快
         - ........

#### 2. GUI 控制台汇总

   - 控制台均默认使用 NodePort 暴露出去，可访问 任一node节点ip + 指定端口 访问
   - 默认端口汇总如下
      - **kubeSphere**：30880，local K8S 控制台，可观测集群负载，内存使用等；
      - **kubeApps**：30890，Helm 安装工具
      - **mysql**：30801，未选型
      - **redis-insight**：30802
      - **dubbo-admin**：30803
      - **rocketmq**：30804
      - **xxl-job**：30805
      - **nacos**：30806
      - **kibana**：30807
      - **minIO**：30808
      - .......
