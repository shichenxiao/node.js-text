# node.js 应用开发测验题

## 一、全局：路径变量

1. node.js 的 API 分为哪两类？ 
  全局对象  普通模块
1. 全局路径变量是什么？其返回值是什么？
   __dirname  当前运行的脚本所在目录    
1. 全局文件名变量是什么？其返回值是什么？  
   __filename  当前运行的脚本文件
## 二、全局：控制台

1. 全局控制台对象是什么？  
   console
2. 控制台打印日志信息的语句是什么？
   console.log
2. JS 中的占位符有哪三种？  
   %s: 字符串占位符
   %d: 整数占位符
   %j: json 输出占位符
2. 标准输出流和标准错误流分别是什么？
   标准输出流:stdout
   标准错误流:stderr
2. 如何在控制台输出标准输出流和标准错误流？
   标准输出流:console.log
   标准错误流:console.errror
2. 将标准输出流重定向到一个文件中要如何操作？
   command > 目标文件
2. 将标准错误流重定向到一个文件中要如何操作？
   command  2 > 目标文件
## 三、全局：进程

1. 进程对象是什么？
   process
2. 进程对象指的是什么？可以通过它获得哪些信息？
   指当前运行的进程，可以获得当前进程的宿主环境信息
   cpu框架，系统信息，当前进程id，绝对路径，可用内存，退出码
3. 如何获得当前程序宿主的 CPU 架构？  
   console.log('architecture',process.arch);
3. 如何获得当前程序宿主的系统信息？
   console.log('platform',process.platform);
3. 如何获得当前进程的 ID？
   console.log('process id',process.pid);
3. 如何获得 node.js 执行的绝对路径？
   console.log('execPath',process.execPath);
3. 在命令行如何查看当前运行的进程？
   ps aux 
3. 使进程不结束的两种方法是什么？
  (1) process.stdin.resume();
  (2) 设置一个超时的时间
3. 如何获得当前用户的 ID?
   console.log('user id',process.getuid());
3. 如何获得当前位置路径？
   console.log('cwd',process.cwd());
3. 在命令行如何查看当前位置路径、用户 ID、node.js版本这些信息？
   node-v:查看版本信息   id:查看用户登录id  pwd:查看当前路径  
3. 如何查看系统的常驻内存大小？
   console.log('memoryUsage',process.memoryUsag().rss);
3. 如何查看 V8 动态分配的总内存大小？
   console.log('memoryUsage',process.memoryUsag().heapTotal);
3. 如何查看 v8 动态分配的已用内存大小？
   console.log('memoryUsage',process.memoryUsag().heapUsed);
3. 如何查看 v8 管理的绑定到 JS 对象上的 C++ 对象的内存？  
   console.log('memoryUsage',process.memoryUsag().external);
3. 如何获得命令行参数？
   process.argv
3. 在命令行中如何查看程序退出码？
   echo $?
3. 如何指定程序退出码？
   程序中：process.exit(exit-code);
   然后在命令行执行程序时后面跟上指定的退出码
3. 标准输入流一般指哪里？
   键盘
3. 标准输出流一般指哪里？
   屏幕
3. 如何在命令行向某进程发信息？
   kill 信息  目标进程的 ID

## 四、全局：定时器

1. 和定时器相关的全局函数有哪些？
   setInterval();  clearInterval(); setTimeout(); clearTimeout(); setImmediate(); clearImmediate();
2. 延迟执行和取消延迟执行的函数是什么？以及他们如何使用？
   setTimeout(回调函数,延迟时长);  clearTimeout(id);
3. 周期执行和取消周期执行的函数是什么？以及他们怎么使用？
   setInterval(回调函数,延迟时长);  clearInterval(id); 
4. 取消周期执行的方法有三种，是哪三种？
   clearInterval()
   通过计数器来控制周期执行的次数
   添加一个耗时操作，当耗时操作结束时，周期执行也会结束
