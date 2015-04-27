package com.fojavally;

public class matchMain {

> /
    * @param args
    * 
> public static void main(String[.md](.md) args) {
> > // TODO Auto-generated method stub
> > > String str = "琉璃渠村地形示意图&nbsp;&nbsp;<p><a href='img.md'>src=http://image.fojavally.com/image/con/2010/12/23/14 /c3199425551489644945.jpg</a>&nbsp;&nbsp;琉璃渠村为龙泉镇辖村从元代起，朝廷即在此设琉璃局，素有“中国皇家琉璃之乡”的美誉。&nbsp;&nbsp;<p><a href='img.md'>src=http://image.fojavally.com/image/con/2010/12/23/14 /c3199425551489644945.jpg</a>&nbsp;&nbsp;琉璃渠村的窑火700多年不熄，是北京最大的琉璃品生产基地。目前故宫大修中所使用的琉璃，大多是琉璃渠村的琉璃厂生产的。&nbsp;&nbsp;<p><a href='img.md'>src=http://image.fojavally.com/image/con/2010/12/23/14 /c3199425551489644945.jpg</a>&nbsp;&nbsp;文并摄/实习生高春洁记者王璐&nbsp;&nbsp;<p><a href='img.md'>src=http://image.fojavally.com/image/con/2010/12/23/14 /c3199425551489644945.jpg</a>&nbsp;&nbsp;(责任编辑：曾安能)&nbsp;&nbsp;<p><a href='img.md'>src=http://image.fojavally.com/image/con/2010/12/23/14/c3199425551489644945.jpg</a>&nbsp;&nbsp;<p><a href='img.md'>src=http://image.fojavally.com/image/con/2010/12/23/14/c3199425551489644945.jpg</a>";</li></ul></li></ul></li></ul>



> while(true){
> > int i = str.indexOf("[");
> > int j = str.indexOf("]");
> > if(i == -1 || j == -1){
> > > break;
> > > }
> > > String result = str.substring(i+9, j);
> > > System.out.println(result);
> > > str = str.substring(j+1,str.length());

> > }


> }
}