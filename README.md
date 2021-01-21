<h1 style="text-align: center">yshop意象商城系统</h1>

#### 3.2版本预告：
1、新增商城装修模块

2、新增商户订单通知

3、提现接入企业付款接口

4、新增app端后台版本控制

5、新增商家端退款申请通知

6、新增商品积分兑换模块（同步主商品sku）

7、升级wxjava版本4.0.0

8、升级springboot最新版本2.4.2

9、新增docker一键部署方案

10、后台商城首页优化

11、新增快递鸟查询顺丰轨迹

12、关键bug修复：
  - 移除roketmq依赖及相关逻辑
  - 修改退款扣库存
  - 去除素材分组分页，防止素材过多显示不完全
  - 修改订单金额为0时，支付不成功直接报错
#### 项目简介
yshop基于当前流行技术组合的前后端分离商城系统： SpringBoot2+MybatisPlus+SpringSecurity+jwt+redis+Vue的前后端分离的商城系统， 包含商城、小程序直播、拼团、砍价、商户管理、 秒杀、优惠券、积分、分销、会员、充值、多门店等功能，更适合企业或个人二次开发；；



#### 官网体验地址（里面有演示地址与文档）
|  官网文档地址  |  https://www.yixiang.co |
|---|---|
| 管理后台演示地址：  |   https://demo2.yixiang.co |
| 关注公众号点击单商户体验小程序与H5  |  ![输入图片说明](https://images.gitee.com/uploads/images/2021/0121/154904_12c09826_477893.png "77a93e8c07a913b838a756abadb383b9.png") |



### docker部署

- 1、创建一个存储第三方软件服务Docker Compose文件目录：
```
     mkdir -p /yshop/soft
```
- 2、然后在该目录下新建一个docker-compose.yml文件：
```
    vim /yshop/soft/docker-compose.yml
```
- 3、接着创建上面docker-compose.yml里定义的挂载目录：
```
    mkdir -p /yshop/mysql/data /yshop/redis/data /yshop/redis/conf
```
- 4、创建Redis配置文件redis.conf：
```
    touch /yshop/redis/conf/redis.conf
```
- 5、docker 部署参考根目录docker文件夹
- 6、以上创建好之后参考docker下文件，先执行软件安装：
```
  cd /yshop/soft
  docker-compose up -d  启动
  docker ps -a 查看镜像
```
- 7、运行docker/applicatiion目录下 docker-compose,当然之前一定要打包jar包，构建镜像
  切换到Dockerfile 文件下：
  ```
  docker build -t yshop-admin .  
  ```

#### 项目源码

|     |  后台系统源码 |   后台系统前端源码  |
|---  |--- | --- |
|   码云  |  https://gitee.com/guchengwuyue/yshopmall  | https://gitee.com/guchengwuyue/yshopmall_qd |
|   github   |  https://github.com/guchengwuyue/yshopmall |https://github.com/guchengwuyue/yshopmall_qd  |



## 商城功能

* 一：商品模块：商品添加、规格设置，商品上下架等
* 二：订单模块：下单、购物车、支付，发货、收货、评价、退款等
* 三：营销模块：积分、优惠券、分销、砍价、拼团、秒杀、多门店等
* 四：微信模块：自定义菜单、自动回复、微信授权、图文管理、模板消息推送
* 五：配置模块：各种配置
* 六：用户模块：登陆、注册、会员卡、充值等
* 七：其他等

    


#### 项目结构
项目采用分模块开发方式
- yshop-weixin        微信相关模块
- yshop-common    公共模块
- yshop-admin    后台模块
- yshop-logging   日志模块
- yshop-tools     第三方工具模块
- yshop-generator 代码生成模块
- yshop-shop      商城模块
- yshop-mproot    mybatisPlus

#### 系统预览
<table>
    <tr>
        <td><img src="https://images.gitee.com/uploads/images/2019/1107/194017_9207632f_477893.png"/></td>
        <td><img src="https://images.gitee.com/uploads/images/2019/1121/230257_5844f5f1_477893.png"/></td>
    </tr>
    <tr>
        <td><img src="https://images.gitee.com/uploads/images/2019/1121/230051_971db503_477893.png"/></td>
        <td><img src="https://images.gitee.com/uploads/images/2019/1121/230342_f379583e_477893.png"/></td>
    </tr>
    <tr>
        <td><img src="https://images.gitee.com/uploads/images/2019/1121/230224_5f0dec5d_477893.png"/></td>
        <td><img src="https://images.gitee.com/uploads/images/2019/1107/194207_7b3b1f53_477893.png"/></td>
    </tr>
    <tr>   
         <td><img src="https://images.gitee.com/uploads/images/2019/1121/230424_f01fca77_477893.png"/></td>
         <td><img src="https://images.gitee.com/uploads/images/2019/1127/211402_4103f8e0_477893.png"/></td>
    </tr>
</table>


## 技术选型
* 1 后端使用技术
    * 1.1 SpringBoot2
    * 1.2 mybatis、MyBatis-Plus
    * 1.3 SpringSecurity
    * 1.5 Druid
    * 1.6 Slf4j
    * 1.7 Fastjson
    * 1.8 JWT
    * 1.9 Redis
    * 1.10 Quartz
    * 1.11 Mysql
    * 1.12 swagger
    * 1.13 WxJava
    * 1.14 Lombok
    * 1.15 Hutool
        
* 前端使用技术
    * 2.1 Vue 全家桶
    * 2.2 Element
    * 2.3 uniapp



	
#### 反馈交流
- 喜欢这个商城后台的小伙伴留下你的小星星啦,star,star哦！

####  特别鸣谢
- eladmin:https://github.com/elunez/eladmin
- mybaitsplus:https://github.com/baomidou/mybatis-plus
- hutool:https://github.com/looly/hutool
- wxjava:https://github.com/Wechat-Group/WxJava
- vue:https://github.com/vuejs/vue
- element:https://github.com/ElemeFE/element
