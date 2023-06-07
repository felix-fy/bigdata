## 一、主机和端口
1.1 jobmanager.rpc.address="192.168.1.1"  
定义单个jobmanager的静态IP地址，在jobmanager-HA模式中不生效

1.2 jobmanager.rpc.port=223  
定义jobmanager的端口，在jobmanager-HA模式中不生效  

1.3 metrics.internal.query-service.port="50100-50200"  
定义Flink内部指标查询服务的端口范围  

1.4 rest.bind-address="192.168.1.1"  
定义rest服务绑定的地址  

1.5 rest.bind-port="50100-50200"  
定义rest服务端口范围  

1.6 rest.port=223  
定义单个rest的静态IP地址，在rest-HA模式中不生效  

1.7 taskmanager.data.port=223  
定义taskmanager的数据端口  

1.8 taskmanager.host="192.168.1.1"  
定义taskmanager的静态IP地址  

1.9 taskmanager.rpc.port=223  
定义taskmanager的rpc端口  


## 二、容错
2.1 restart-strategy.type=  
定义在作业失败时使用的重新启动策略  
none：不重新启动  
fixeddelay：修复延迟重启策略  
failurerate：失败率重启策略  
exponentialdelay：指数延迟重启策略  

2.2 restart-strategy.fixed-delay.try="1"  
任务标记为失败之前重试执行的次数  

2.3 restart-strategy.fixed-delay.delay="1m"  
定义两次连续重新启动尝试之间的时间间隔  

2.4 restart-strategy.failure-rate.delay="1m"  
定义因故障而重启的两次连续重新启动尝试之间的时间间隔  

2.5 restart-strategy.failure-rate.max-failures-per-interval="10"  
定义因故障二重启的最大重启次数  

## 三、清理任务
3.1 cleanup-strategy.type
none：只执行一次清理
fixed-delay：按固定间隔执行清理任务，直到清理成功或达到设定重试次数
exponential-delay：指数延迟重新启动策略以指数增加的延迟触发清理，直到清理成功或达到设定数量。达到配置的限制后需要手动清理作业

3.2 cleanup-strategy.fixed-delay.attempts
清理任务标记为失败前的重试次数

3.3 cleanup-strategy.fixed-delay.delay
清理任务失败后重试前的延迟时间

3.4 cleanup-strategy.exponential-delay.try
定义重试清理任务的次数

3.7 cleanup-strategy.exponential-delay.initial-backoff


3.8 cleanup-strategy.exponential-delay.max-backoff



## 四、检查点和后端状态


## 五、故障恢复


## 六、内存配置


## 七、其他参数


## 八、安全


## 九、编排框架


## 十、kubernetes相关参数
.1 kubernetes.namespace=
定义jobmanager和taskmanager部署的namespace

.2 kubernetes.jobmanager.labels=
定义部署jobmanager容器的labels

.3 kubernetes.taskmanager.labels=
定义部署taskmanager容器的labels

.4 kubernetes.container.image.pull-secrets
定义连接镜像仓库的密钥信息

.5 kubernetes.service-account
定义创建jobmanager和taskmanager的service-account

.6 flink-main-container
定义容器名称

.7 jobmanager.memory.process.size
定义jobmanager容器的requests和limits

.8 taskmanager.memory.process.size
定义taskmanager容器的requests和limits


## 十一、监控指标


## 十二、历史记录服务器


## 十三、jobmanager配置参数


## 十四、taskmanager配置参数
## 客户端


