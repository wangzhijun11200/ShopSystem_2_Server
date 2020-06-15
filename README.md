**[项目演示PPT][1]**

##项目介绍
###项目名称
淘宝贝电子商务平台(2018.8-2018.9)
###开发技术
>Spring，SpringMVC，Spring Cloud相关组件
>Mybatis，Maven
>Mysql，Redis
>Jquery，Ajax，
>Solr
>Android
###项目描述：
基于SpringCloud微服务架构的B2C电子商务系统，主要分为用户服务				         (service-user),管理员服务(service-admin),通信服务(service-message)以及注册中心(Eureka-Server)
1)用户服务：
>a.用户管理：用户认证，信息修改，手机及邮箱绑定，找回密码
>b.商品模块：商品检索，分页展示，详情及评论明细，购物车明细
>c.订单模块：加入购物车及结算，订单确认及状态查询，订单明细
>d.其他：商品收藏列表，浏览及搜索历史，我的评价

2)管理员服务:
>用户列表，商品管理，订单管理，分类及属性管理
###责任描述
1).利用Spring-Session+Redis缓存实现各服务间登录用户信息共享

2).利用Rest WebService客户端(Feign)实现服务间调用

3).利用断路器(Hystrix)处理服务调用超时和失败，防止故障扩散

4).利用服务网关(Zuul)实现动态路由，利用ZuulFilter进行权限控制

5).完成商品分类表，商品表，订单表等相关数据库表结构设计

6)部署solr搜索引擎，录入数据整合到项目中进行全文搜索

7).完成用户认证模块，密码加密，手机短信、邮箱验证码(Freemarker)   
        
8).完成用户订单和购物车模块前端、后端service层和dao层的实现及测试调试

9). 利用SpringBoot的文件上传完成用户头像上传，Ajax实现商品多图片上传

##项目收获：
1.开发中遇到服务之间静态资源的调用由于浏览器同源策略的限制抛出跨域问题，网上查阅后通过在网关中增加CorsFilter解决，也对jsonp的相关知识有所理解。

2.通过对订单模块的设计与开发，更加熟练的掌握了半自动化的基于关系-对象映射(ORM)的MyBatis数据库访问技术以及动态Sql，CRUD操作Sql语句优化。

3.通过service层的编写，对Spring基于数据库对事务的支持实现的声明式事务有了更深的理解，Spring通过IOC划分事务处理单元，将事务各种配置放入IOC容器，然后通过AOP(动态代理)拦截需要进行事务处理的类进行合适的事务处理。

4通过该项目的开发，更加熟练的利用框架编程，更加深入的理解Spring的相关思想和操作流程，增强了动手能力，更深刻的明白团队合作的重要性。  

   [1]: https://cdn.itudo.cn/resume/defence-B2C.pdf
