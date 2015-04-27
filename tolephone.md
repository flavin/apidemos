##### 1.删除Android中的地图支持 #####
  1. com.fojapalm.android.ad.AdMapAct.java
> 2.com.fojapalm.android.ad.AdActionAct.showMap（）
> 3.com.fojapalm.android.ad.AdShow.buildAction()
> > adImage.setOnClickListener()
> > > case 9:
  * //                    String map[.md](.md) = ad.getActionParam().split(",");
  * //                    adactionact.showMap(map[0](0.md), map[1](1.md), map[2](2.md), map[3](3.md));

> > break;


> 4.AndroidManifest.xml
> > <activity android:name=".ad.AdMapAct">
> > 

&lt;intent-filter&gt;


> > > <action android:name="android.intent.action.MAIN" />

> > 

&lt;/intent-filter&gt;


> > 

Unknown end tag for &lt;/activity&gt;




##### 2.修改资源 #####
  1. 桌面图标 :Drawle/logo.png

> 2.开机画面 :Drawle/welcome.jpg
> 3.关于标题 :取消版本号 SingleDesktopAct

> AlertDialog aboutDialog = new AlertDialog.Builder(SingleDesktopAct.this)
> > .setTitle("欢迎您使用“挖挖资讯”\n").setView(v).setMessage(
> > > "每天挖一挖，尽知天下事。\n\n多定制，多搜索，乐趣无穷\n\n第一次使用时，请您先开始阅读").create


##### 3.窗口顶部添加返回键 #####

> 在以下页面添加：
    * 桌面 SingleDesktopAct
    * 文章列表 ArticlesListAct
    * 定制 SettingsAct 
    * 收藏 FavArticlesListAct 
    * 搜索 SearchResultAct 
    * 热点 HotspotAct 


### 1.在onCreate()方法中添加 ###
> requestWindowFeature(Window.FEATURE\_CUSTOM\_TITLE);
> setContentView(View);
> getWindow().setFeatureInt(Window.FEATURE\_CUSTOM\_TITLE, R.layout.view\_title);
> TextView titleTextView = (TextView) findViewById(R.id.title\_text);
> titleTextView.setText("挖挖资讯 - 热点"); //根据不同的页面做对应的修改
> Button titleButton = (Button) findViewById(R.id.back);
> titleButton.setOnClickListener(new OnClickListener() {

> @Override
> public void onClick(View v) {
> > // TODO Auto-generated method stub
> > act.finish();

> }
> });


### 2.viewtitle 修改为 ###
> <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
> > android:id="@+id/screen"
> > android:layout\_width="fill\_parent"
> > android:layout\_height="fill\_parent"
> > android:orientation="horizontal">


> <Button android:id="@+id/back"
> > android:layout\_width="wrap\_content"
> > android:layout\_height="wrap\_content"
> > android:layout\_centerVertical="true"
> > android:textSize="14px"
> > android:text="@string/title\_back"/>


> <TextView android:id="@+id/title\_text"
> > android:layout\_width="wrap\_content"
> > android:layout\_height="wrap\_content"
> > > android:layout\_centerInParent="true"

> > android:text="@string/app\_name"
> > android:textSize="20px"
> > android:textColor="#FFFFFF"
> > android:layout\_weight="0" [[/>]]


> 

Unknown end tag for &lt;/RelativeLayout&gt;




### 3.String.xml中添加按钮上文字 ###
> 

&lt;string name="title\_back"&gt;

<![CDATA[<  返回 ]]>

&lt;/string&gt;

