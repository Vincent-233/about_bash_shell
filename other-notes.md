## sort 和 uniq
ls -Rl|sort|uniq       # 显示去重之后的结果
ls -Rl|sort|uniq -c    # 去重计数(类似于count ... group by ...)
ls -Rl|sort|uniq -dc   # 去重计数仅显示计数大于1的,即有重复的

## 零散
- 赋值符号中间不能有空格： `$x=1` 不能写为 `$x = 1`
- 重定向, 0,1,2 分别代表 stdin stdout stderr
  - ls -l > output.txt       # 默认stdout重定向到文件
  - ls -l 2> output.txt      # 将stderror重定向到文件
  - ls -l > output.txt 2>&1  # stdout 和 stderr均重定向到文件
  - ls -l &> output.txt      # stdout 和 stderr均重定向的新写法
  - ls -l 2> /dev/null       # 将输出重定向到空设备,相当于丢弃输出
- tee, 接受管道结果再传递给下一个管道,可用于将管道的中间结果保存下来,用于review
  - ls -lR|tee result.txt|grep '.py$' 


  
