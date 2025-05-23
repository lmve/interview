# 开发工具

## git 
- 提交发生冲突 
```csharp-interactive
git stash // 暂存当前文件
git pull  // 拉取远程仓库代码合并到本地分支
git stash pop // 恢复暂存文件
```
- 误提交撤回
```dotnetcli
git reset HEAD file
```
- 修改提交记录
```dotnetcli
git commit –amend // 最近一次
// 修改之前提交的历史记录 
git log  // 查看提交记录
git rebase -i HEAD~3 // 倒数第三提交记录开始，然后将 pick 改为 edit
git commit –amend  // 修改
git rebase --continue // 提交修改
```
- 查询某行代码的作者
```dotnetcli
git blame src/app.js  // 整个文件
git blame -L 5,10 src/app.js  // 具体到行
```


## gdb
- 设置断点
```dotnetcli
break main.c:64
```

- 执行
```dotnetcli
next  // 下一步，不进入函数
step  // 会进入函数
continue  // 到断点
```
- 查看变量的值
```dotnetcli
print x
```

- 修改变量的值
```dotnetcli
set var x=10
```

- 查看调用堆栈
```dotnetcli
backtrace
```

- 加载符号文件
```dotnetcli
file myprogram
```
- 查看寄存器值
```dotnetcli
info registers
```
- 查看内存值
```dotnetcli
x/4xw 0x1000
```
- 查看函数的参数
```dotnetcli
info args
```

