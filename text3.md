# node.js 应用开发测验题

## 一、全局：Buffer

1. Buffer 对象的用途是什么？  
处理二进制数据
2. 如何实例化一个 Buffer 对象？
buffer=new Buffer()

3. Buffer 对象的填充方法是什么？  
fill()
5. 实例化 Buffer 的三种方法分别是什么？
（1）数组
（2）字符串
（3）拷贝旧的Buffer
6. Buffer 支持的六种编码格式分别是什么？
UTF-8 base64（编码） hex（十六进制） binary（二进制） ASCII码 UTF16LE
7. 把字符串转化成另一种编码格式用的方法是什么？
buffer.toString('CodingName');
8. 在网页中内嵌图片的 HTML 代码是怎样的？
<img src="data:[MIME-TYPE][;charset=<encoding>[;base64]<data>]" >
9. 调用文件模块的语句是怎样的?
var fs=require('fs');
10. 调用 http 模块的语句是怎样的？
var http=require('http');
11. 计算机上的数据分为哪两种？
可读的纯文本数据，二进制数据
12. bmp 缩写于什么？
Bitmap
13. 如何从网页上获取一个位图？
wget URL
14. 怎样保存文件到 Windows 本机上？
sz filename
15. 位图二进制文件格式是怎样的？ 
头信息+数据部分
16. 写入二进制数据用的是什么方法？
write方法

## 二、全局：模块管理

1. node.js 中进行模块管理的全局对象有哪几个？分别是什么功能？  
require() 引用模块,export 暴露模块接口,module 代表当前模块
2. JS 模块化的两种方案是什么？
前端的：AMD
后端的：CommonJS
3. 什么时候要用 require()？ 
引用非全局模块的时候
3. npm 是什么的缩写？有什么作用？
缩写于 Node Packaged Modules,是node.js的模块管理器
4. 如何安装要使用的第三方模块？
npm install data-now
5. 使用 package.json 配置文件管理第三方模块的过程是怎样的？
  +初始化一个 package.json 文件：npm init
  +安装第三方模块：npm install moduleName -S(--save)
  + 发布程序和 package.json 配置文件
  + 使用时：运行 npm install 安装第三方模块
6. 删除一个文件夹的命令是什么？
rm -rf
7. 用什么方法让别人可以使用我们自定义的模块？
module.exports=something
8. 怎样暴露模块中的一个变量？
module.exports=value
9. 怎样暴露模块中的一个函数?
module.exports=function(){};
11. node.js 中require()返回的是什么？
是 exports 对象,或者是 module.exports 变量
12. 画图表示怎样加载一组相关的模块？

13. node.js 中的顶层对象是什么？
global 对象
14. 前端中的顶层对象是什么？
window 对象
15. 查看 module 时，都包含哪些信息？ 
+id：模块的识别符，通常是带有绝对路径的模块文件名
+exports：表示模块对外输出的值
+parent：返回一个对象，表示调用该模块的模块
+filename：模块的文件名，带有绝对路径
+children：返回一个数组，表示该模块要用到的其他模块
+loaded：返回一个布尔值，表示模块是否已经完成加载
