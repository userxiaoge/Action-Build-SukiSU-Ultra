# Action-Build
**```Build OnePlus SukiSU Ultra KPM Kernel```**
# 更新日志
--允许自定义内核后缀  <- **`beta`**  
```
1.当自定义内核后缀为空时,使用随机字符串,不再是默认的“x.xx.xxx-androidxx-8-o-g3b1e97b8b29f”
2.当自定义启用时,修改内核为“x.xx.xxx-androidxx-自定义内容”,同时也不再保留androidxx-8-o-g3b1e97b8b29f
3.当使用clang make(Fast Build)时,为新的源内核信息x.xx.xxx-o-g3b1e97b8b29f添加缺失的内核android版本号,再进行1或2中的操作
```  
--支持部分机型极速编译`(目前支持5.10、5.15、6.1、6.6)`  
--修复`OnePlus Ace5Pro、OnePlus 13`跑不出来无法开机问题,直接使用官方dtbo就可以直接开机[@reigadegr](https://github.com/reigadegr)  
--支持显示自己填入的内容在`Show selected inputs debug`这一步,同时工作流名称也可以看到一些东西  
--从写入 `ak3.zip` 的配置文件后缀中删除潜在的版本代码,替换成精确的 `Android` 版本号`XX.X.X`
```
AnyKernel3_SukiSUUltra_12896_oneplus_ace2pro_Android15.0.0_KPM_VFS.zip
AnyKernel3_SukiSUUltra_12896_oneplus_13_Android15.0.2_KPM_VFS.zip
AnyKernel3_SukiSUUltra_12896_oneplus_11_Android14.1.0_KPM_VFS.zip
```
--`KPM` 默认关闭  
--新增 `dir4`、`dir5` 路径用于支持 `sm8750` 和部分机型开启 `ZRAM` 后的新路径（比如 `ace2p`、`13T`）[@ShirkNeko](https://github.com/ShirkNeko)  
--添加 `zram` 模块的 `LZ4K` 压缩算法支持[@ShirkNeko](https://github.com/ShirkNeko)  
--同步 `susfs` 模块上游下载频道的变化，解决无法下载的问题  
--优化 `sm8750`、`sm7675` 的 `build` 方案  
--新增 `dir3` 路径用于支持 `sm8475`（比如 `ace2`）  
--支持自动下载最新 `CI` 的 `susfs` 模块并调用 `ksud` 安装
--支持 `VFS HOOK`（自选是否开启）

[![Build](https://img.shields.io/badge/GitHub%20Actions-Build-181717?logo=github&logoColor=white&style=flat-square)](https://github.com/Numbersf/Action-Build/actions/workflows/Build%20SukiSU%20Ultra%20OnePlus.yml) [![Channel](https://img.shields.io/badge/Follow-Telegram-blue.svg?logo=telegram)](https://t.me/taichi91) [![OnePlus Kernel Manifest](https://img.shields.io/badge/OnePlus%20Kernel%20Manifest-EB0029?logo=oneplus&logoColor=white&style=flat-square)](https://github.com/OnePlusOSS/kernel_manifest) [![Coolapk](https://img.shields.io/badge/Follow-Coolapk-3DDC84?style=flat-square&logo=android&logoColor=white)](http://www.coolapk.com/u/28259173)[![Coolapk](https://img.shields.io/badge/Follow-Coolapk-3DDC84?style=flat-square&logo=android&logoColor=white)](http://www.coolapk.com/u/23244807)
