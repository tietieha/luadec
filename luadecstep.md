[#反编译lua字节码](https://blog.palug.cn/3000.html)

1. 首先看到安装包内有共享库libxlua.so,可以知道xlua版本号,关键字:LuaVersion
2. 测试
> - 如果报错:format mismatch in precompiled chunk
> - 自己编译一个helloworld.lua比较一下
> - 对比文件头,替换应该是可以反编译成功的
3. 修改luadec
> - 可以对比ldump.c的dumpHeader函数和xlua的区别
> - 修改文件头check
