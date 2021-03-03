# ddnsto-openwrt
ddnsto for openwrt

## 使用方法

把文件夹 ddnsto 拷贝到 Openwrt 源代码的 package/network/services 里面，拷贝之后为：

```
tree package/network/services/ddnsto
package/network/services/ddnsto
├── files
│   ├── ddnsto.config
│   ├── ddnsto.init
│   └── ddnsto.uci-default
└── Makefile
```

### make menuconfig 选择方法

```
make menuconfig

Network --->
Web Servers/Proxies --->
<*> ddnsto....................................... DDNS.to - the reverse proxy

LuCI --->
3. Applications --->
<*> luci-app-ddnsto.................................. LuCI support for ddnsto
```

### 部分 Openwrt 老版本兼容性问题

安装完成点击配置，需要手动运行命令：

```
/etc/init.d/ddnsto enable
```
