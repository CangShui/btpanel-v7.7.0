# btpanel-v7.7.0
btpanel-v7.7.0-backup  官方原版v7.7.0版本面板备份

**Centos/Ubuntu/Debian安装命令 独立运行环境（py3.7）**

```Bash
curl -sSO https://raw.githubusercontent.com/CangShui/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```

去除登陆绑定手机号
```
rm -f /www/server/panel/data/bind.pl
```


手动解锁宝塔所有付费插件为永不过期
```
文件路径：www/server/panel/data/plugin.json
搜索字符串："endtime": -1 全部替换为 "endtime": 999999999999
```
手动阻止解锁插件后自动修复为免费版
```
chattr +i /www/server/panel/data/plugin.json
```
