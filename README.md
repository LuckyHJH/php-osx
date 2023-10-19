# php-osx
用于旧版mac安装旧版php。譬如10.13的mac系统安装PHP7.2。

### 一句命令安装
```
curl -s https://raw.githubusercontent.com/LuckyHJH/php-osx/master/install.sh | bash -s 7.2
```

##### 离线安装
也可以把install.sh放在本地，再安装
```
cat php-osx_install.sh | bash -s 7.2
```

##### 如果提示已经安装(is already installed)
1. 修改/usr/local/packager/packager.py，直接去掉223行的那段if判断。
2. 手动执行打印出来的关键命令，如：sudo /usr/bin/python2.7 /usr/local/packager/packager.py install 7.2-10.10-frontenddev

##### 如果还没生效
如果php -v还是没生效
1. 编辑 ~/.bash_profile
2. 添加一行 export PATH="/usr/local/php5/bin:$PATH"
3. 最后再 source ~/.bash_profile
