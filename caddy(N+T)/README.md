介绍：

本示例使用 Caddy 源码加改进版 forwardproxy 插件、caddy-trojan 插件编译而成 Caddy 文件，实现了 NaïveProxy 与 Trojan-Go 服务端加伪装网站应用。

注意：

1、使用本人 Releases 中编译好的 Caddy 文件，可同时支持 NaïveProxy、Trojan-Go 等应用。

2、本示例中 NaïveProxy 除了支持 HTTP/2 代理应用，还同时支持 HTTP/3 代理应用，即 QUIC 协议传输。

3、若 NaïveProxy 使用 HTTP/3 代理应用，即 QUIC 协议传输，建议增加 [UDP 接收缓冲区大小](https://github.com/lucas-clemente/quic-go/wiki/UDP-Receive-Buffer-Size)。

4、本示例中 Trojan-Go 兼容原版 Trojan-Go，继承了其服务端核心特色：支持 Trojan 应用与 Trojan-Go 的 WebSocket 应用共存；支持 CDN 流量中转(基于 WebSocket over TLS)。

5、本示例 Caddy 支持自动 HTTPS，即自动申请与更新 TLS 证书，自动 HTTP 重定向到 HTTPS。
