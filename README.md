# MF-language
This is a computer language(explain type) that designed by myself.
Now it has many problems that I have to deal with.
I will show this to you and wish you can help me deal with difficulties or communicate with me to develop it.Thanks~

I will rewrite the code in c++ after I solve all the basic problems.
Of course we can do this together.
If I can,I will try to make the complier of MF.

communication:qq group:916289058

please join in with your github name or sketch how you know this.

It runs successfully on the MacOS(OS X).

please make a file named 'test.mfs' or change the code of reading file to use.

# MF语言
这是我自己设计的一门解释型计算机语言，现在还存在着许多的问题等待解决。
我将会将源代码公布出来，希望各位能和我一起来解决问题或是一起做开发，谢谢~

我将会在所有基础问题解决后用c++重写代码。
当然我们可以一起来做这件事情。

如果可以的话，我会尝试去做MF的编译器。

请创建一个名为test.mfs的文本文件或是修改读取代码来使用。

联系方式：
qq群：916289058

请在加群时附带你的github名称或是简略描述你的得知渠道。

目前在苹果系统上能够成功运行。

# grammar(wait to improve)

### define
`def valuename value`

special value(these are key words that can do something before calculating):
`false`
`true`
`undefined(js)``nil(lua)`
`obj`

### define function
`deffun functionname parms(or arguments.the same meaning there.use<,>to separate arguments);sentence1;sentence2;……;endfun;`

use `return value` to give the result of the function

### quote function
`fun functionname parm1 parm2……`

### change value
`let valuename value`

### output
`out toObj value`

### if
`if condition;sentence1;sentence2;……;endif;`

`if a<b;s1;……;else;s1;……;endif`

### loop
`rep conditon;sentence1;sentence2;……;endrep;`

### end
`endif`
`endrep`

### load file and run
`load filename`

after loading,it will run

warning:if you want to load a file that is not in the folder(or the same list),you have to write the absolute address.

e.g.:`load test` or `load /desktop/test`

## already finished
out(lua:only support toobj:`console`)(js:support `console` and `output`)

def

let

rep

if

else

deffun

return

fun

load(only for lua version)

## rules
1.all the symbol`\n`must be neglected.

2.`;` is seen as the split symbol of each sentence.

3.each sentence must use ` `(space)as the word split symbol.

4.sign symbol:

`~`:the letters after this are seen as strings.

### calculate
#### number
`+-*/`

`#x`:# means root and x is the power number.

`^x`:power

`$x`:$ means get negative number.

#### logic
`><=!|&`(only for js:`≥≤`)

`>`:greater than

`<`:less than

`=`:equal

`!`:not equal

`|`:or

`&`:and

#### object
`.`:get object member value

e.g.:`object.1(for number)` `object.~x(for string)`

`@`:add object members or change the value of the object(must define first)

e.g.:`object@(~atk,1)`

#### function
`,`:add parms(arguments)

`@`:quote function

e.g.:`x@(1,2)`

# 语法（待完善）
`def 变量名 值`———————|定义变量

`fun 函数名 参数1 参数2……`——- |执行函数

`let 变量名 值`———————|设置变量，出现未定义的变量时报错

`out 目标 值`-————————————|输出语句

`deffun 函数名 参数;语句1;语句2;……;endfun;`|定义函数，用逗号来隔开每个参数

`return 值` ——————|函数返回值，不填返回`nil`（lua）`undefined`(js)

`load 文件名/文件的绝对路径`————|用于加载并运行.mfs源代码(仅用于lua版)

### 定义变量时的特殊值
`true`
`false`
`nil(lua)` `undefined(js)`
`obj`

### 条件语句
`if a<b;语句1;语句2;……;endif;`

`if a<b;语句1;……;else;语句1;……;endif`

### 循环语句

`rep a<b;语句1;语句2;……;endrep;`

### 结束语句
`endif`

`endrep`

## 已完成
out（lua:当前只支持目标`console`)(js:支持`console`和`output`)

def

let

rep

if

else

deffun

return

fun

load(仅用于lua版)

### 规则：
1.所有的换行(``\n``)全部忽略

2.以`;`作为句子与句子间的分割符

3.每一句中每空一格`` ``算一个单词

4.变量标识符：

`~`：~后的字符将视作字符串处理

### 计算表达式 规定所有运算为:
算数：`+-*/  ^平n次方 #开n次根 $取负`

逻辑：`><=!&|`(仅js可用:`≥≤`)

对象：`.`取对象成员 `@`给对象成员赋值/添加对象成员(需先进行对象定义)

例如:`对象.1(对于数字成员名来说)` `对象.~攻击(对于字符串或文字来说)`

例如:`对象@(~攻击,1)`

函数：`,`追加参数 `@`引用函数

例如：`a@(1,2)`
