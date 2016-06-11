# iNot-eclient
广东天翼校园shell脚本

## 脚本说明
基于[Padavan固件](http://www.right.com.cn/forum/thread-161324-1-1.html)开发
，支持openwrt（需修改IP获取方式）

## Install
### Padavan

**方法一：**【 运行路由器初始化之前: 】(尾部添加)

``` bash
cat > "/tmp/eclient.sh" <<-\EOF
    #脚本内容
EOF
chmod 777 "/tmp/eclient.sh"
```
【 自定义设置 - 脚本 - 运行后WAN上/下活动: 】(尾部添加)
``` bash
if [ "$1" == "up" ]; then
    /tmp/eclient.sh start &
fi
```
保存，重启

**方法二：**把脚本放到/tmp（保存到闪存芯片）
【 自定义设置 - 脚本 - 运行后WAN上/下活动: 】(尾部添加)
``` bash
if [ "$1" == "up" ]; then
    /tmp/eclient.sh start &
fi
```
保存，重启
