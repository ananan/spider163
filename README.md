 ![spider163 logo](https://github.com/Chengyumeng/spider163/blob/master/logo.jpeg)
# 抓取网易云音乐 spider163 v2.4.5


## 安装模块
- 第一步：使用pip install -r requirements.txt安装第三方依赖
- 第二步：使用Python setup.py install 安装爬虫模块
- 第三步：指定SPIDER163_PATH环境变量，缺省情况下为$HOME/spider163
- 第四步：把默认配置文件spider163.conf拷贝到SPIDER163_PATH下，并配置数据库
- spider163 --help

## 功能模块
- initdb
- resetdb
- playlist
- music
- comment
- lyric
- search
- get


## 使用指南

```console
$ spider163 initdb
$ # 根据配置文件的数据库信息自动创建数据库表，删除全部数据通过resetdb实现
```
```console
$ spider163 resetdb
$ # 重建相关数据库
```
```console
$ spider163 playlist
$ # 默认下载全部推荐歌单（1000+），也可以通过指定页码去下载（-p=1）
```
```console
$ spider163 music
$ # 默认下载10个歌单的歌曲数据，也可以通过指定循环大小（-c=2）来下载10 * c 个歌单内歌曲
```
```console
$ spider163 comment
$ # 默认根据数据库存储的未下载歌曲随机下载一首单曲的评论，也可以通过-c指定需要下载的单曲数量和-s强制指定歌曲id
$ # spider163 comment -c 10 | spider163 comment -s 209115
```
```console
$ spider163 lyric --count=10
$ # 抓取10首音乐的歌词，可以通过制定歌曲ID抓取特定一首音乐（--song）
```
```console
$ spider163 search -q="林依晨"
$ # 搜索功能（待完善，暂支持歌曲搜索）
```
```console
$ spider163 get -s 209115
$ # 阅读歌曲基本信息、歌词、热评
```
```console
$ spider163 get --playlist 922064582
$ # 获取歌单的基本信息、歌曲等
```


## TODO
- [2017 Q4](https://github.com/Chengyumeng/spider163/blob/master/TODO.md)
- ...

# 欢迎关注微信公众账号：程天写代码
![guojingcoooool](https://github.com/Chengyumeng/spider163/blob/master/wechat.jpeg)
