
#### 1. GTP connector download and instructions for use
```
gtp-linker_linux // linux client
gtp-linker_mac // osx client
gtp-linker_windows.exe //windows client
```
#### 2. Explanation for the config file
```
{
 user:
   user: ""  # login account
   password: "" #login password
 game:
   safe_time: 0 #safe time(sec)，will be reduced in time_left
   min_time: 0 # when time_left < safe_time, it will be used as your ai engine thinking time
   kgs_time: false # new setting，can support kgs-time_settings
   shell: "" # AI GTP Engine
}
```
