jpush_push_PHP_server
=====================

jpush_push_PHP_server

最近整合了phonegap 的andriod的消息推送。
实在是，挺不容易，之前找个各种办法，都不是很好，用极光的jpush，发现效果不错，所以就想把这个块做好点。
 
查看了极光的API文档，发现可以做server的远程调用 API。所以我也抽时间写了一个，官方有一些服务器端，但是都是v1的最老版本的。所以我根据v2写了一个简单的。
有很多其他语言写的api，但是都是基于原来旧版本的，
想想还是重写一个v2新版本的。所以就有了以下文件
。
主要功能：发推送通知，并存储发送记录到数据库端，同时记录是否发送到客户这样的功能。
 
现在我把代码分享给大家：

主要修改一下代码就可以了：
 【config.inc.php】


  define('DB_HOST', 'localhost');
  define('DB_USER', '××××'); //数据库用户名
	define('DB_PWD', '××××'); //数据库密码
	define('DB_NAME', '××××'); //数据库
	define('DB_TAB', '××××');//数据表
	define('DB_CODE','utf8');	
	define('appkeys','×××××');	//appkey值 极光portal上面提供 
	define('masterSecret', '××××××');    //API MasterSecert值 极光portal上面提供 
	define('platform', 'android');    //推送平台
