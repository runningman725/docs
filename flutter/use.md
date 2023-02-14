使用前：
1.cmd->flutter create demo1 方式或者用IDE创建
2.vs code 安装 dart,flutter,code runner, awesome flutter snippets等插件

使用中：
1.MaterialApp 和 Scaffold两个组件装饰app

material app常用属性：
home（主页）
tilte
color
theme
routes

scaffold常用属性:
appbar 显示在界面定不的一个appbar
body 当前界面所显示的主要内容widget
drawer 抽屉菜单控件
snackbar
底部sheet的api

2.flutter把内容单独抽离成一个组件，自定义组件其实是一个类
StatelessWidget是无状态组件，状态不可变的widget
StatefulWidget是有状态组件，持有的状态可能在widget生命周期改变

3.Container 容器组件
alignment 对齐方向
decoration 圆角，渐变，背景颜色
margin 
padding
transform 旋转，位移,缩放
height
width
child 容器子元素

4.Image.asset 本地图片
Image.network 远程图片

5.Container 只能放一个元素
Containner 和 Sizedbox类似，需要设置padding或者背景的时候用container

6.生成动态list
(1)创建方法for 循环
（2）listview.builder

7.double.infinity 主要用在container容器里头，在其他地方可能不生效

8.有时候没有设置width height ，运行之后没有任何效果
比如positioned需要给子组件通过width 和 height设置宽高才显示子组件

9.final size=MediaQuery.of(context).size 
size.width 	size.height
获取屏幕的宽度和高度

10.stack (层叠组件)
--positioned 是基于外层定位，所以通常是在容器里头使用的

11.生成圆形图片组件
ClipOval  CircleAvatar

12.在Column组件中也可以使用ListTile

13.按钮
ElevatedButton
TextButton
OutlinedButton
IconButton
修改按钮的宽度高度，在外面套SizedBox 或者 Container

14.主题设置
style:Theme.of(context).textTheme.headline6

15.ListView中嵌套列表的时候，使用Column再用ListTile

16.
Scaffold
appbar
title/bottom:tabbar
     		body:TabBarView

17.AutomativeKeepAliveClientMxin 做缓存组件
如果缓存页面比较多，会消耗内存

18.
基本跳转路由
Navigator.of(context).push(
MaterialPageRoute(builder:(BuildContext context){
return const SearchPage();//指定路由
})
);

返回上一页
Navigator.pop(context);
Navigator.of(context).pop();

命名路由跳转
在main.dart中命名路由之后调用时无需引入import
Navigator.pushNamed(context,"/search");

onGenerateRoute 配置命名路由传参

替换路由
Navigator.of(context).pushReplacementNamed('/register');

返回根路由
Navigator.of(context).pushAndRemoveUntil(
MaterialPageRoute(builder:(BuildContext context)){
return const Tabs();
),(route)=>false);

ios/android使用同样风格路由跳转：
MaterialPageRoute 改为 CupertinoPageRoute

19.dialog
alerdialog
simpledialog:可以做选择框
modelBottomSheet:底部弹出窗口
flutterToast: 短暂弹出并消失
上pub.dev/packages去加载fluttertoast

自定义dialog，自定义一个类extends Dialog

20.InkWell 也可以代替IconButton，因为有点击事件

21.Material组件可以设置背景透明

22.PageView/PageView.Builder 需要放在 Scaffold里头,不然屏幕变黑
无线滑动调用 onPageChanged方法

自动轮播 添加计时器 Timer.periodic
  
23.实现组件的排序或者动画的时候需要传key
key不能重复，所以用来做唯一表示
状态的保存主要通过判断组件的类型或者key值是否一致

key分两类（局部，全局）
局部(LocalKey): ValueKey(传string), ObjectKey(传Object), UniqueKey(可空)
全局(GlobalKey): GlobalKey, GlobalObjectKey

24.MediaQuery.of(context).orientation 获取屏幕方向

25.globalKey.currentState 可以获取子组件的状态，执行子组件的方法。（最常用）
globalKey.currentWidget 可以获取子组件的属性
_globalKey.currentContext!.findRenderObject()可以获取渲染的属性

26.AnimatedList 可以在列表中插入或者删除节点时执行一个动画
insertItem(), removeItem()
 
27.隐式动画
AnimatedContainer 属性改变时有动画
AnimatedPadding 	属性改变
AnimatedPositioned	属性改变
AnimatedOpacity	属性改变
AnimatedDefaultTextStyle	属性改变
AnimatedSwitcher 	子组件改变时有动画效果

28.getX 状态管理（弹框，主题设置等更加方便）
使用简单，然后无需传入context
路由跳转也方便










