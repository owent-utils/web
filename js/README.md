OWenT’s Utils -- Web -- js
=============

### jquery.browser.ts
环境检测类 -- 支持作为jQuery插件(typescript)

### showJson.js
显示JSON结构 -- web的js开发很方便啊，但是碰到iframe里的东西还是不方便看到变量的内容，所以就写了这么个看json内容的玩意，还可以当控制台输出用。

很简单,有需要以后开发新功能
#### 更新记录
+ 1.1 更新对不同类型着色
+ 1.2 如果载入了jQuery UI 则使用jQuery UI的Dialog打开，用于解决嵌套iframe时浏览器拦截问题
+ 1.3 解决Object循环引用时栈溢出问题，同时增加引用的指向锚点


### TQueryString.js
这是学校USRP项目需要而写的一个类，但是既然写出来了，以后也可能用到，就共享出来吧。

这个类用于解析网页URL的QueryString参数，或者也可以当做操作一些其他设置的类库。

本类库支持任意类型的值的记录，支持JSON语法，支持类似“a=b&c=d”作为设置参数，支持对数组和JSON的转换。
#### 修正记录：
+ 1.1  –  修正对’转换错误的BUG
+ 1.2  –  修正字符串包含换行符的bug
+ 1.3  –  增加value可记录任意类型，兼容性修正，key中的空格默认转换为下划线
+ 1.4  –  可从自定义URL获取参数
+ 1.5  –  去除key的特殊转义，支持把value为数组或json的结构转换为QueryString，注：暂不支持解析QueryString中的数组，目前下标符号和下标均会被认为是key的一部分
+ 1.5.1 — 修正IE浏览器下类型判断的严重BUG
+ 1.5.2 — 获取当前URL的参数支持多分隔符（采用正则表达式，URL参数必须包含=号，如：a=&b=c）
+ 1.6 — 增加支持把结构体和数组字符串转换成相应结构（注意：解析字符串时不能包含[和]，这两个字符会被认为是key分隔符）
+ 支持解析数字类型和布尔类型
+ 支持自定义关键字分隔过滤器、关键字提取过滤器和URL分隔符过滤器
+ 1.7 — 修正使用window变量的问题
          修正参数只按&符号分割的问题
          增加$符号作为默认参数分隔符