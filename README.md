# 说明

本仓库提供了下载 Win10 字体的快捷方式，和打包字体的 CMake 脚本。并包含了 Win10 [列表](https://docs.microsoft.com/zh-cn/typography/fonts/windows_10_font_list) 中所有的必备字体和中文补充字体。（除了 HoloLens ，这个在 Win10 系统中实际上不存在）

注意！根据 [微软最终用户许可](http://www.microsoft.com/typography/fonts/product.aspx?PID=164)：

> Please note, that usage of Microsoft fonts outside running Windows
> system is prohibited by EULA (although in certain countries EULA is invalid).
> Please consult Microsoft license before using fonts.

和 [重新分发和扩展权限](https://docs.microsoft.com/zh-cn/typography/fonts/font-faq#%E9%87%8D%E6%96%B0%E5%88%86%E5%8F%91%E5%92%8C%E6%89%A9%E5%B1%95%E6%9D%83%E9%99%90)

> 你无法重新分发 Windows 字体。 你不能将它们复制到其他计算机或服务器，也不能将它们转换为其他格式（包括位图格式）或对它们进行修改。

在非 Windows 系统中使用 Windows 字体是被阻止的。而且微软不允许重新分发 Windows 字体。因此我不会以任何形式提供打包好的二进制文件。需要字体的有三种方式：

- 下载此仓库并自行决定如何使用 fonts/ 下的文件
- 下载此仓库后使用 CMake 脚本 将字体打包成 rpm 包后进行安装
- 自己从 WIndows 系统中拷贝

# 许可

我没有任何来自微软公司或者其他字体提供商的许可，由于时间原因，我尚未完整研读所有字体的许可。如果您发现我违反了许可，请告知我，我会以最快的速度将其删除

因此，本仓库除非有法律人士直接指出我可以以何种方式授权，否则我不会添加任何许可。所有许可与微软用户许可保持一致。

# 构建

1. 下载此仓库并解压
2. CMake -B build
3. cd build
4. cpack -C CPackConfig.cmake

生成的 rpm 包位于 build/pack 下。

# 鸣谢

感谢 [ttf-ms-win10](https://github.com/streetsamurai00mi/ttf-ms-win10)
提供的模板。最初我是在它的仓库基础上完成的，但是后来发现缺失了一部分字体，因此就自己弄了一份拷贝。

# 版权声明

我对字体文件没有所有权，而且也并没有获得任何来自微软公司的许可，这里字体只是为了分流存在，避免部分用于为了使用字体而导致下载整个
系统镜像。违反微软最终用户许可的用户请自行承担责任。

如果微软公司对我共享字体文件的请求感到不满，请联系我的邮箱： DragonBillow@outlook.com
。我将立即删除此仓库

# 最后

非法律人士看这些东西真累啊，要是所有软件的许可都是 MIT 多方便。。。
