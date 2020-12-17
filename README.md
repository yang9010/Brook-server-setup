# Brook-server-setup
Nami setup the brook server
使用nami安装brook
curl -L https://git.io/getnami | bash && sleep 6 && exec -l $SHELL
使用nami安装brook, 他会自动帮你选择适用你系统的最新版brook文件
nami install github.com/txthinking/brook
使用joker运行brook server守护进程
nami install github.com/txthinking/joker
我们建议你先在前台直接运行brook server, 确保一切都正常后再结合joker使用
joker brook server -l :9999 -p hello

brook socks5 运行一个独立的socks5 server, 支持 TCP and UDP, 假设你的服务器IP是 1.2.3.4, 你想创建一个 socks5 server 1.2.3.4:1080
brook socks5 --socks5 1.2.3.4:1080

joker 守护
joker brook socks5 --socks5 1.2.3.4:1080
