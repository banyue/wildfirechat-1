# 自定义消息内容
野火IM内置了文本，图片，语言，视频等一系列的消息类型，但这远远不能满足客户各种各样的需要。我们需要一种机制来任意添加新的消息类型，满足一下几步就可以。

#### Step 1 定义消息内容类型并注册
消息内容都有一个共同的基类[```MessageContent```](message_content.md)，自定义消息也需要继承这个类，并实现其中的方法，可以参考内置的消息类型。

消息定义完成后，需要在connect之前，调用```registerMessageContent```方法来注册到SDK中.

#### Setp 2 修改UI，找到消息列表界面添加对这个消息的UI支持
iOS和Android请找到对应的代码，直接添加到工程中。
