### 2015/09/30 JS 笔记
###1.这是同步流线思维的方式
M
(1) var 这里是全局变量
(2) function 这里是封装的code业务代码

V
setHTML 设置和组装DOM结构的操作（这里需要用到前面的var或者数据data，data可以是同步也可以是异步的），也是可以封装到function里去
setCSS 设置样式的操作，也是可以封装到function里去
BindEvnet 可以封装到function里去

C
流程init 也是可以封装到function里去
但是这个东西肯定是有入口init调用的，就是OBJ.init()


-----------------------------------------------

###2.这是obj字面量有点跳跃思维的方式

工具的MV对象字面量
```
var tool = {
	"toolA":function(){},
	"toolA1":function(){},
	"toolA2":function(){},
	"toolA3":function(){},
	"toolA4":function(){},
	"toolA5":function(){},
	"initTool":function(){
		//code 
	}
}
```
主流程的MV对象字面量，他依赖上面的tool对象
```
var obj = {
	"A":function(){},
	"A1":function(){},
	"A2":function(){},
	"A3":function(){},
	"A4":function(){},
	"A5":function(){},
	"init":function(){
		//code 
	}
}
```
C
主流程的业务入口
```
obj.init()
```
