# EFramework
解决代码之间耦合性的框架 For Unity3D  
====  
概述：  
- 
该框架非常简单，只有三个脚本，使用委托和事件的机制，使用事件码枚举将监听的同事件码的方法链接到一起。  
EventCenter脚本负责添加监听、移除监听、广播事件码。  
EventType脚本是定义事件码的地方。  
CallBack是定义委托的脚本，默认实现了带有五个参数的委托，使用者可以再次扩展，相应的需要在EventCenter脚本中书写添加/移除/广播该数量参数的方法。<br>  
如何使用： 
-
1.将框架的三个脚本放进项目中  
2.在EventType枚举中定义好事件码  
3.在需要监听该事件码的脚本中Awake方法里调用EventCenter.AddListener(事件码，执行的方法)  
3.在需要监听该事件码的脚本中OnDestroy方法里调用EventCenter.RemoveListener(事件码，执行的方法)  
4.使用EventCenter.Brocast()方法广播事件码，就可以调用所有监听该事件码的方法  <br>
视频讲解链接：SiKi学院
-
http://www.sikiedu.com/course/304
