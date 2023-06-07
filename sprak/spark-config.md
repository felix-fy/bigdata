## 一、主机和端口
1.1 jobmanager.rpc.address="192.168.1.1" \n
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

