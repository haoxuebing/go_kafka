## kafka生产者与消费者

### producer 文件夹是生产者
- 向topic `web_log` 中生产消息

### consumer_group 文件夹
- 可以自定义group
- 只要不更改group.id，每次重新消费kafka，都是从上次消费结束的地方继续开始
- session.MarkMessage(message, "") 手动提交offset

### consumer_patition
- 一次可监听多个切片
- sarama.OffsetOldest 重头开始消费
- sarama.OffsetNewest 程序启动后生产的消息开始消费

### consumer_topic
- 一次可监听多个topic