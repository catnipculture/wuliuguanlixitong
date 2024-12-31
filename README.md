> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

物流管理系统有管理员和用户两个角色。

管理员功能有个人中心，用户管理，车辆信息管理，公告信息管理，司机管理，物流信息管理，运单信息管理，车辆类型管理，车辆状态管理，公告类型管理，物流状态管理，运单状态管理。



用户可以注册登录，查看公告信息，查看物流信息，可以添加运单信息。



# 环境要求



1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。 

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA; 

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可 

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS; 

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目 

6.数据库：MySql5.7/8.0等版本均可；





# 技术栈



运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：SpringBoot + MyBatis + Vue + Bootstrap + jQuery





# 使用说明





1.使用Navicat或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件； 

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目； 

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；





# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq 

源码看好后直接在网站付款下单即可，付款成功会自动弹出百度网盘链接，网站地址：[http://www.codegym.top](http://www.codegym.top/)

其它问题请关注公众号：**IT小舟**,关注后发送消息即可，都会给您回复的。若没有及时回复请耐心等待，通常当天会有回复



# 运行截图

![img](https://img-blog.csdnimg.cn/img_convert/994de7659dee6403d7667f01db48ee47.png)



![springboot208基于springboot物流管理系统4](https://img-blog.csdnimg.cn/img_convert/79b497d326565c9755bdffabfaf59531.png)

![springboot208基于springboot物流管理系统5](https://img-blog.csdnimg.cn/img_convert/eed34eafadde0a794fc5ab0a1531016c.png)

![springboot208基于springboot物流管理系统6](https://img-blog.csdnimg.cn/img_convert/3c8f801a4865ffeb3154c75c599c37d1.png)

![springboot208基于springboot物流管理系统7](https://img-blog.csdnimg.cn/img_convert/c7f00686888efca8890218334590aa65.png)

![springboot208基于springboot物流管理系统8](https://img-blog.csdnimg.cn/img_convert/ca38c47f72f62e24553112e44731e496.png)

![springboot208基于springboot物流管理系统9](https://img-blog.csdnimg.cn/img_convert/7f8adcfbc906f38c73fe8e05d7415a48.png)

![springboot208基于springboot物流管理系统10](https://img-blog.csdnimg.cn/img_convert/14d7acad9b403197b72a513ea1576dc3.png)

![springboot208基于springboot物流管理系统11](https://img-blog.csdnimg.cn/img_convert/897e6b16a300b50f75c8f275b7500cdd.png)### 代码

```
    @Override
    public PageUtils queryPage(Map<String, Object> params) {
        Page<DingdanxinxiEntity> page = this.selectPage(
                new Query<DingdanxinxiEntity>(params).getPage(),
                new EntityWrapper<DingdanxinxiEntity>()
        );
        return new PageUtils(page);
    }
    
    @Override
	public PageUtils queryPage(Map<String, Object> params, Wrapper<DingdanxinxiEntity> wrapper) {
		  Page<DingdanxinxiView> page =new Query<DingdanxinxiView>(params).getPage();
	        page.setRecords(baseMapper.selectListView(page,wrapper));
	    	PageUtils pageUtil = new PageUtils(page);
	    	return pageUtil;
 	}
    
```
