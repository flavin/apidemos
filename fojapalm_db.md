## 解析之后直接将数据写入DB ##
> 添加定制的Topic表
> 提供定制的Topic的存储（包括父topic和其子Topic）
> <新闻、博客>采用相同操作
> 修改位置
  1. 添加ParentId字段（区分父Topic和子Topic）
> > 存：解析父Topic并将ParentId赋值为0写入数据库
> > > 解析子Topic并将ParentId赋值为其父TopicId写入数据库


> 取：根据ParentId=0获取所有的父Topic

> 将父Topic对象和其对象位置写入Map缓存

> 根据ParentId<>0获取所有的子Topic

> 根据每个父Topic获取其对应的子Topic并写入到Topic对象


2.在welcome中取广告一次
3.SingDeskAct中将firstrun改为数据库存取
4.解析广告的同时将广告写入DB
> 3.1 解析后的JSon串写入到AD表
> 3.2 获取图片的URL写入到到SD卡中
5.自定义关键词
> 添加自定义关键词到FLOW表中

