<h1 align="center">AniCh-Continue (Unofficial)</h1>

<p align="center">一个支持超分辨率的在线动漫弹幕APP。多平台，多番剧源，多弹幕，高清无广告。追番看番必备软件。

<div align="center">

[![GitHub release](https://img.shields.io/github/v/release/Sle2p/AniCh)](https://github.com/Sle2p/AniCh/releases/latest)
[![Stars](https://img.shields.io/github/stars/Sle2p/AniCh)](https://github.com/Sle2p/AniCh/stargazers)
[![GitHub all releases](https://img.shields.io/github/downloads/Sle2p/AniCh/total)](https://github.com/Sle2p/AniCh/releases/latest)

</div>

## GO: https://github.com/Enthalpiex/NeoHcina

#### 别问，问就是寄了，作者大大的源码和最新发行版之间账户系统存在许多调整，导致想要实现破解的时间大大增加

不过经过了一些解包工作，这里提供一些基本信息供各位参考

该项目通过Token验证的方式运行

### 1. 文件结构

某 .hive 文件存储了用户的账户信息和相关数据，采用类似 Protobuf 的二进制编码格式，包含：

登录 Token，用户基本信息（头像、邮箱、昵称等），账户状态（经验、积分、角色等），时间戳（注册和更新时间），地址和其它辅助信息

### 2. 主要字段介绍

| 字段名        | 说明                | 格式          |
| ---------- | ----------------- | ----------- |
| `token`    | 登录凭证，认证使用         | ASCII字符串    |
| `avatar`   | 头像URL             | ASCII字符串URL |
| `email`    | 邮箱                | ASCII字符串    |
| `name`     | 昵称                | UTF-8中文字符串  | 
| `role`     | 用户角色（如user/admin） | ASCII字符串    |
| `sex`      | 性别                | ASCII字符串    |
| `exp`      | 经验值               | 二进制浮点数      |
| `coin`     | 账户金币/积分           | 二进制浮点数      |
| `color`    | 个人颜色标签            | ASCII字符串    |
| `created`  | 注册时间戳             | 64位整数或时间戳   |
| `updated`  | 更新时间戳             | 64位整数或时间戳   |
| `id`       | 唯一用户ID            | 二进制UUID     |
| `address`  | 地址信息              | UTF-8中文字符串  |
| `spEnable` | 功能开关或特权标志         | 二进制数据       |


### 3. 额外说明

token在每次重新登陆时会刷新，长度固定约为 142 个字符，未测试时效

乱码主要集中在数值字段（exp、coin、created、updated、id、spEnable）鉴定为二进制编码玩的


以上。玩得开心！


---

逆向已暂停，欢迎大家继续尝试。
