[English](https://github.com/ZhuRongJian/gtp-linker) | 简体中文

### 2020福州世界人工智能赛-AI连接器使用文档

##### 请确保您的连接器为大会最新版本，当前版本v1.3。

#### 一.下载连接器和文件解释

> https://github.com/ZhuRongJian/gtp-linker/releases

> 在资源包中有4个文件分别为：

```
config.json //连接器的配置文件
gtp-linker_linux //Linux客户端
gtp-linker_mac //osx客户端
gtp-linker_windows.exe //Windows客户端
```

#### 二.配置文件详解

```
user:
  account:"" #登录名，由主办方提供
  password:"" #登录密码，由主办方提供
game:
  kgs_time:false #是否支持kgs-time_setting
  min_time:0 #当剩余时间(秒) < 安全时间时，使用此值作为引擎思考时间
  safe_time:0 #安全时间(秒)，会在time_left中自动扣减
  shell:"" # AI GTP Engine
```

> 您可使用如下方式修改配置内容

1. 使用命令行工具输入如下内容，并根据提示进行操作。
```
> cd  "linker dir"
> ./gtp-linker_[os] config
```

2. 手工修改 `config.json` 文件并保存。

#### 三.调试流程

使用命令行工具输入如下内容，并根据提示进行操作。
```
> cd  "linker dir"
> ./gtp-linker_[os] debug
```

#### 四.比赛流程

使用命令行工具输入如下内容，并根据提示进行操作。
```
> cd  "linker dir"
> ./gtp-linker_[os] run
```


#### 五.关于连接器使用到的命令有

```
clear_board
boardsize
time_settings
play
gen_move
time_left
komi
kgs-time_settings
```

#### 六.其它说明

1. 关于safe_time和min_time的使用，如果您的引擎有自己的时间策略，建议将来保留为默认值0。

2. 连接器启动命令中有一个可选参数，用于保留完整的连接器收发消息的履历，正式比赛时必须使用。

```
./gtp-linker_[os] -l xx.log run/debug
```
