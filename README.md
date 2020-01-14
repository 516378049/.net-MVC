# .net-MVC
the source of .net mvc

.net MVC Project Template

note:
you should regenerate you resovle so that it will import the package from NuGet

function:

All of the Contrller should be inherit BaseController， so  that you can use  BaseController's function
All of the DataAccess should be inherit DBContextBase， so  that you can use  DBContextBase's function 
All of the Bussiness should be inherit BussinessBase， so  that you can use  BussinessBase's function 
1、写日志功能
	1、在方法上加上[UserOptionLog]自定义过滤器
	2、在方法返回数据中使用父类的Json方法格式化数据 eg: return Json("", JsonRequestBehavior.AllowGet);

2、
//usage scenario for access database
for below function , we suggest fllow's scenario
1、ExcuteProEntpriseLib ： excute the sp  with returnValue
2、ExcuteSqlEntpriseLib ： excute the sql  with returnValue
3、getDataTableEntpriseLib ： excute the sp  with DataTable and  ReturnValue and outputs
4、getListEntpriseLibsql ： excute the sql  with List<> 
	
3、write log 
use below sentense
LogManager.DefaultLogger.Info("DefaultLogger");
LogManager.StorageLogger.Info("StorageLogger");
