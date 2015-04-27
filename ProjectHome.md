

&lt;P&gt;

SDK中自带的DEMO运行时会报错

&lt;/P&gt;




&lt;P&gt;

具体修改：

&lt;/P&gt;




&lt;P&gt;

错误信息
[2010-10-19 08:58:26 - ApiDemos] libpng warning: Ignoring attempt to set cHRM RGB triangle with zero area

[2010-10-19 08:58:26 - ApiDemos] D:\QQDownload\android-sdk\_r07-windows\android-sdk-windows\platforms\android-3\samples\ApiDemos\res\values\strings.xml:365: error: Apostrophe not preceded by \ (in I'm on! :))

[2010-10-19 08:58:26 - ApiDemos] D:\QQDownload\android-sdk\_r07-windows\android-sdk-windows\platforms\android-3\samples\ApiDemos\res\values\strings.xml:366: error: Apostrophe not preceded by \ (in I'm off! :()

[2010-10-19 08:58:26 - ApiDemos] D:\QQDownload\android-sdk\_r07-windows\android-sdk-windows\platforms\android-3\samples\ApiDemos\res\values\strings.xml:640: error: Apostrophe not preceded by \ (in  The Android platform is a software stack for mobile devices including an



解决：

Apostrophe not preceded by \ (in I'm on! :))

提示在有单引号（撇号）前加上\

处理步骤如下：

1）        检查设置

（1）  检查Android设置

（2）  Java Build Path设置

i.             Java Build Path  > Source选项卡

ii.           Java Build Path  > Libaries选项卡

iii.         Order and Export选项卡

2）       修改文件ApiDemos\res\values\ strings.xml 在撇号前加\

（1）  修改364行：


&lt;string name="summary\_on\_advanced\_toggle\_preference"&gt;

I'm on! :)

&lt;/string&gt;


为


&lt;string name="summary\_on\_advanced\_toggle\_preference"&gt;

I\'m on! :)

&lt;/string&gt;


（2）  修改365行


&lt;string name="summary\_off\_advanced\_toggle\_preference"&gt;

I'm off! :(

&lt;/string&gt;


为


&lt;string name="summary\_off\_advanced\_toggle\_preference"&gt;

I\'m off! :(

&lt;/string&gt;



（3）  修改625 – 640 行在所有撇号前加\

3）       查看gen文件加下生成R文件

4）       运行后效果
具体代码见：
svn checkout http://apidemos.googlecode.com/svn/trunk/

&lt;/P&gt;




&lt;P&gt;

此代码为修改后并可以使用的并在不断的更新注释中...

&lt;/P&gt;

