# 1.gRPC理论
  - ## 1.1 RPC框架原理
  　　RPC全称:Remote Procedure Call Protocol,即为远程调用另外一台服务器上的服务过程,由于不能直接调用，需要通过网络传达语义及数据   
  　　Ａ服务器调用Ｂ服务器上的服务,A是如何寻找到Ｂ的？
  - ## 1.2 常用的RPC框架
       1. Facebook Thrift
       2. Google gRPC
       3. Sina   Motan(只支持特定语言)
  - ## 1.3 gRPC简介
    - ### 1.3.1 gRPC概览
      gRPC 是Google开源的RPC框架,目前支持的语言有python, java, C/C++, GO等仓库地址为:
      https://github.com/grpc/ ,gRPC出来比较外，外面的文档较少，具体案例可以参考官方的github
      里面的案例，下面有部分资料可供参考:    
      官方文档: https://grpc.io/docs/guides/concepts/   
      gRPC讲解比较到位的博客: http://jiangew.me/grpc-01/   

    - ### 1.3.2 gRPC特点
       1. 通信协议基于http2之上的二进制协议(Protobuf 序列化机制),http2自带头部压缩
       2. 多路复用,每次是与服务端建立一个TCP连接,处理多个请求
       3. 基于IDL文件,支持多语言内库支持并可以自动编译服务端代码
       4. gRPC相较于JSON，拥有更高的序列化/反序列化效率，易于实现更高的吞吐性能
    - ### 1.3.3 gRPC缺点

    - ### 1.3.4 IDL描述文件proto
       gRPC 默认使用 protocol buffers，这是 Google 开源的一套成熟的结构数据序列化机制

# 2. gRPC简单实践
  - ## 简单API gRPC服务
    - ### 流式rpc
    - ### server streaming
    - ### client streaming
    - ### double streaming




# 3. other
- ## HTTP2  
