Failed to connect to 127.0.0.1 port 7890 after 2003 ms: Couldn't connect to server '

给想进行自行安装的朋友，如果遇到这个问题，可以优先检查自己上网工具的端口

可以看到报错这里写着，Git 仍然在尝试通过 127.0.0.1:7890 代理端口连接，我检查翻墙工具给我的代理端口是7897

打开终端执行对应代码执行就能成功了。
​
git config --global http.proxy http://127.0.0.1:xxxx（上网端口）
git config --global https.proxy http://127.0.0.1:xxxx（上网端口）

希望对大家有帮助。

​