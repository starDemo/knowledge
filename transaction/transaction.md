事物
	ACID
	Atomicity原子性
	Consistency一致性
	Isolation隔离线
	Durability持久性


CAP理论

消息中间件在分布式系统中的主要作用：
	异步通讯
	解耦
	并发缓冲


XA协议：两段提交协议

如何保证消息一致性（消息发送存在失败的可能）
	1.发送到消息中间件，待发送状态
	2.执行业务，若成功，则发送状态
	3.将操作结果发送中间件
	
	
可靠消息最终一致性
	1.本地消息服务（同一个事物中），异常消息通过消息恢复系统处理。并通过回调或确认消息队列的方式确认消息。
	2.独立消息服务，通过消息服务存储消息，通过收到业务成功消息才发送消息