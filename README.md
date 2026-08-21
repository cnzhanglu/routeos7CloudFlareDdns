# ROS新版本的ddns脚本

在网上找了各种版本，都不好使。最后自己花了一天时间一点点调试出来的，测试更新没有问题。

# 修改内容

改了临时文件的名字，不然多个脚本并行时有影响。

兼容 RouterOS 7.24：不再使用 `:execute script=... file=...` 写临时文件，
改用 `/file add` 和 `/file set`，同时修复调试日志中的引号解析错误。


原始脚本：https://cloud.tencent.com/developer/article/2198814
