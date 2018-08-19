# Http

## http2.0

1. 多路复用 (Multiplexing)

多路复用允许同时通过单一的 HTTP/2 连接发起多重的请求-响应消息。
HTTP/2 可以很容易的去实现多流并行而不用依赖建立多个 TCP 连接，HTTP/2 把 HTTP 协议通信的基本单位缩小为一个一个的帧，这些帧对应着逻辑流中的消息。并行地在同一个 TCP 连接上双向交换消息。
2. 二进制分帧
HTTP/2在 应用层(HTTP/2)和传输层(TCP or UDP)之间增加一个二进制分帧层。
3. 首部压缩（Header Compression）
4. 服务端推送（Server Push）