## 安装 virtualenv 模块：pip install virtualenv
## 查看virtualenv是否安装成功 virtualenv -h
## 

## cd env
## 激活虚拟环境Scripts\activate （退出虚拟环境：deactivate）

## 切换到需要执行.py 文件的目录，运行 * pip install -r requirements.txt *

# 打开Proxy SwitchyOmega插件的 Proxy功能, 打开后浏览器的网络应该是不可用的

# 启动Replay Server
## mitmdump -s replayer.py --set har_file_path=${network.json文件的路径}


# 使用Data Dumper

## 打开chrome Devtool，切换到Data Dumper面板

## 选择session.json文件后会打开隐身窗口，并自动运行Minty插件

## 重复测试同一份dump文件时，需要重新启动下Replay Server（mitmdump -s replayer.py --set har_file_path=${har_file_path}）， 关闭上一次测试打开的隐身窗口。如果session.json文件已经选择，可以直接点击Relay auto apply按钮开始。