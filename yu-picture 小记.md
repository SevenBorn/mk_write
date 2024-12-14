# yu-picture 小记

1. `@EnableAspectJAutoProxy(exposeProxy = true)` 默认参数 exposeProxy = false，开启之后就可以对类进行 **切面编程**（Spring AOP)生成代理类，否则如果遇见需要事务处理等需要代理类的操作时并且当前类不是代理类，就需要这种方式生成当前类的代理类进行操作。

2. ```java
    /**
            * HTTP 状态码
            *  400 Bad Request
            *  401 Unauthorized 没权限
            *  403 Forbidden 禁止访问
            *  404 Not Found 资源不存在
            *  405 Method Not Allowed 请求方法不允许
            *  406 Not Acceptable 不接受
            *  408 Request Timeout 请求超时
            *  409 Conflict 冲突
            *  410 Gone 资源被永久删除
            *  411 Length Required 长度必须
            *  412 Precondition Failed 前置条件失败
            *  413 Payload Too Large 负载过大
            *  414 URI Too Long URI过长
            *  415 Unsupported Media Type 不支持媒体类型
            *  416 Range Not Satisfiable 范围不满足
            *  417 Expectation Failed 期望失败
            *  418 I'm a teapot 茶壶
            *  422 Unprocessable Entity 无法处理实体
            *  423 Locked 资源被锁定
            *  424 Failed Dependency 依赖失败
            *  426 Upgrade Required 升级要求
            *  428 Precondition Required 预处理要求
            *  429 Too Many Requests 请求过多
            *  431 Request Header Fields Too Large 请求头字段太大
            *  433 Request Header Fields Too Large 请求头字段太大
            *  440 Login Timeout 登录超时
            *  444 No Response 无响应
            *  449 Retry With 重试
            *  450 Blocked by Windows Parental Controls Windows parental controls are turned on and are blocking access to this website.
            *  451 Redirect 重定向
            *  ------------------------------------
            *  500 Internal Server Error 服务器内部错误
            *  501 Not Implemented 接口未实现
            *  502 Bad Gateway 网关错误
            *  503 Service Unavailable 服务不可用
            *  504 Gateway Timeout 网关超时
            *  505 HTTP Version Not Supported HTTP版本不受支持
            *
            */
   ```

3. 