# k8s 简介
![k8s](img/kubernetes-high-level-component-archtecture.jpg)



# K8s 整体架构

# k8s 主要组件和功能作用

## Master 主要组件
- apiserver   
    暴露了对外提供服务的API，供界面操控K8S,k8s api doc (https://kubernetes.io/docs/concepts/overview/kubernetes-api/)

- etcd    
   用于Kubernetes的后端存储。所有集群数据都存储在此处,它是一个高可用的k-v数据库，内部采用raft协议
   [raft算法参考这里](https://cizixs.com/2017/12/04/raft-consensus-algorithm/）作为一致性
   算法,它是基于GO语言实现，在命令行可以通过命令查看etcd存储的数据，它存储的结构有点类似于文件存储系统，是树结构，可以通过etcdctl查看  `etcdctl get / --prefix --keys-only` 这里是etcd官网(https://etcd.io)

- controller manager    
   作为集群内部的管理控制中心，负责集群内的Node、Pod副本、服务端点（Endpoint）、命名空间（Namespace）、服务账号（ServiceAccount）、资源定额（ResourceQuota）的管理，当某个Node意外宕机时，Controller Manager会及时发现并执行
   自动化修复流程，确保集群始终处于预期的工作状态。它包含一系列controller.例如如下：
   ```
Replication Controller
Node Controller
CronJob Controller
Daemon Controller
Deployment Controller
Endpoint Controller
Garbage Collector
Namespace Controller
Job Controller
Pod AutoScaler
RelicaSet
Service Controller
ServiceAccount Controller
StatefulSet Controller
Volume Controller
Resource quota Controller
   ```

- scheduler
- kubelet
- container runtime
- kube-proxy


## Node 组要组件
