# ShellcodeBypassAntiVirus

引流密码：shellcode, bypass, anti virus

这是我的毕业设计，2021年5月18日之后就没更新啦，是shellcode免杀工具，静态免杀效果非常好，加密了 cobalt strike 和 mimikatz 的shellcode，在有360卫士的虚拟机环境里都是能正常运行的。

但是没做动态免杀，所以可能运行一段时间，杀软反应过来了就会被杀了。

免杀这种东西公开出来肯定就没什么效果啦，懂得都懂，不过我这个东西技术含量不高，所以也没什么可惜的。

现在是2021年9月2日，加密了一个cobalt strike的shellcode，能够正常上线的，VT测试了一下效果还是可以哦！3/67（我都用VT了说明真的不在乎什么了- -）

https://www.virustotal.com/gui/file/f47eb13ef5b62a6539681a7e4f5219fb32c0d819e781528694b36102c734aa20/detection

用到的技术主要是 syscall 调用API，shellcode加密这块其实做了一点小小小小小小的创新就是没有使用加密算法，所以不会被检测到加解密循环。

工作方式就是将任意shellcode转成混淆过的c/c++源码，然后你可以把这个源码嵌入到一个正常的项目里，达到白加黑的效果。

要达到最好的效果，建议找一个流行的开源项目，把生成的免杀源码藏在里面。

用法其实挺简单的，自己用vs2019编译一下，主程序有提示的，目前只支持x64。

我是一个小菜鸡，这是我的博客：

https://blog.csdn.net/Kwansy

欢迎给我点赞哦！
