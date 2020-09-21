English | [简体中文](https://github.com/ZhuRongJian/gtp-linker/blob/master/zh-cn.md)

### Competition Notes for 2020 Fuzhou World AI Go Provisions 

##### Please ensure your AI connector version is the latest, it's v1.0.
##### 
#### 1. GTP connector download and instructions for use
> https://github.com/ZhuRongJian/gtp-linker/releases

> 4 files included in the resource：

```
config.json //config file
gtp-linker_linux //linux client
gtp-linker_mac //osx client
gtp-linker_windows.exe //windows client
```

#### 2.Explanation for the config file

```
user:
  account:""  #login account
  password:""  #login password
game:
  kgs_time:false #support kgs-time_setting
  min_time:0 #when time_left(sec) < safe_time, it will be used as your ai engine thinking time
  safe_time:0 #safe time(sec)，will be reduced in time_left
  shell:"" # AI GTP Engine
```
> You can modify the settings as follows

1. Use the command line tool to enter the following words， and operate according to the feedback.
```
> cd  "linker dir"
> ./gtp-linker_[os] config
```

2. Manually modify the `config.json` file and save.

#### 3.Flow for debug game

Use the command line tool to enter the following words， and operate according to the feedback.

```
> cd  "linker dir"
> ./gtp-linker_[os] debug
```

#### 4.Flow for regulation game

Use the command line tool to enter the following words， and operate according to the feedback.

```
> cd  "linker dir"
> ./gtp-linker_[os] run
```

#### 5.The commands used by the connnector are

```
clear_board
boardsize
time_settings
play
gen_move
undo
time_left
komi
kgs-time_settings
```

#### 6.Other Notes
 1、Regarding the use of `safe_time` and `min_time`, if your engine has its own time strategy, it is recommended to leave it as the default value of 0 in the future.

2、There is an optional parameter in the connector startup command, which is used to keep a log of the complete connector sending and receiving messages. You need to use it 
```
./gtp-linker_[os] -l xx.log run/debug
```


