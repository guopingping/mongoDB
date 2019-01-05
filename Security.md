```javaScript
Security
    mongodb访问控制能够有效保证数据库的安全
    访问控制是指绑定Application监听的IP地址，设置监听端口，使用账号和密码登录

安全部署Mongodb最佳实践
    不要把mongodb服务器部署在互联网上或DMZ里；
        应该部署在公司内部网络，使用路由器或防火墙技术把Mongodb服务器保护起来
        不允许直接从互联网访问mongodb端口，通过这种方式防止未授权的访问及DDos攻击
    为mongodb实例启用安全模块
        始终开启安全模式，并为需要访问的数据库用户建立相应的权限
    使用SSL
        使用SSL对性能没有影响并且可以防范类似于man-in-the-middle的攻击。
    禁止HTTP和REST端口
    合理配置用户权限
        不建议做法：
            仅仅使用一个高权限用户来执行所有操作
            给一个用户多于他需要的权限
            使用弱密码或多个账号同用一个密码
            删除数据库后没有删除相应的用户
    合理配置操作系统权限
        不要使用root或其他高权限用户来启动mongodb。
    保护好密钥文件
    ssl配置须知
        需要妥善的配置才可以防止可能的安全漏洞。以下几点应遵循：
            给mongodb实例一个或多个CA用以认证
            不要使用自签名证书
    使用审计功能
        记录用户对数据库的所有相关操作。
        
```