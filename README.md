# 欢迎使用EasyNest，基于nest.js的企业级服务端开发全家桶
###### 预告，过段时间会放出详细的代码、使用文档和demo

### 让后端开发更加简单高效
[nest.js](https://github.com/nestjs "nest.js")是一个web开发框架，结合了AngularJS式的模块化开发和RXJS函数式响应编程理念，再搭配上TypeScript, 因此也就非常适合企业级后端开发。EasyNest是建立在nest.js和[EasyType](https://github.com/davanchen/easytype "EasyType")之上的一套企业级服务端开发框架，完善了一些nest.js目前不够完美的地方，诸如：借鉴了egg.js的loader和约定优于配置的理念、缓存、定时任务、消息队列、API文档等。

### 目前提供的包包
|  包名 | 备注  |
| ------------ | ------------ |
|  common | 申明了一些类型和接口，定义了几个用于前端显示的Exceptions, 也包含了一些有用没用的utils |
|  core |  实现了egg.js的loader机制，解决了nest.js每个module都要显式声明的繁琐步骤，能够自动按照环境加载配置和语言文件 |
|  api |  API文档模块，基于EasyType，无需增加任何的装饰器、代码或者注释，自动生成API文档、RPC接口文档和swagger文档 |
|  cache |  分布式缓存，nest.js自带的缓存只能缓存控制器方法， 这个可以劫持所有方法缓存controller和service，并且能够配置消息队列实现缓存统一的更新 |
|  event |  消息队列，目前实现了本地消息、rabbitmq和redis |
|  mongoose |  基于EasyType重复造了一个轮子，不用再写mongoose schema了 |
|  passport |  重复造了一个轮子，也是基于passport.js |
|  pay | （未完成） 统一支付模块，使用统一接口完成微信和支付宝支付 |
|  redis | 也是重复造的轮子，主要为了整个框架服务  |
|  schedule | 定时任务模块  |
|  session | 统一session管理模块，要结合passport包一起使用  |
|  storage | 统一储存管理模块，目前只实现了aliyun-oss, 每个微服务模块只要引入包就可以实现文件上传，控制器等都已经实现，不用写任何代码了 |
| validator  | 数据验证模块，基于ajv的包装，同样需要借助EasyType生成类型声明  |
| microservice  | （未全部完成）微服务模块，借助EasyType和API文档模块，可以一键生成proto申明文件、interface文件和RPC代理调用代码，目前写了一个vscode插件可以生成本地的，后期可以根据远程api地址生成  |

### 借助插件一键生成proto
![](https://github.com/davanchen/easynest/raw/master/Code_7GLTwoRGAx.png)
![](https://github.com/davanchen/easynest/raw/master/Code_oBYASf68Uo.png)

### API文档自动生成（枚举、控制器、模型）
![](https://github.com/davanchen/easynest/raw/master/screenshot_enums.PNG)
![](https://github.com/davanchen/easynest/raw/master/screenshot_controller.PNG)
![](https://github.com/davanchen/easynest/raw/master/screenshot_models.PNG)
