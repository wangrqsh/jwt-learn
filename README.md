JWT是什么?

使用场景?

如何正确的使用?

*JSON Web Token* 

*由 header、payload 和 signature 三部分组成*

**header**.payload.signature

JWT 适合用于向 Web 应用传递一些非敏感信息

**payload 是一定不能够携带敏感数据如密码等信息的**

signature 验证数据是否被修改过

JWT保证的是数据传输过程中的完整性而不是机密性



### 什么场景该适合使用 jwt？



## JWT 的几个特点

（1）JWT 默认是不加密，但也是可以加密的。生成原始 Token 以后，可以用密钥再加密一次。

（2）JWT 不加密的情况下，不能将秘密数据写入 JWT。

（3）JWT 不仅可以用于认证，也可以用于交换信息。有效使用 JWT，可以降低服务器查询数据库的次数。

（4）JWT 的最大缺点是，由于服务器不保存 session 状态，因此无法在使用过程中废止某个 token，或者更改 token 的权限。也就是说，一旦 JWT 签发了，在到期之前就会始终有效，除非服务器部署额外的逻辑。

（5）JWT 本身包含了认证信息，一旦泄露，任何人都可以获得该令牌的所有权限。为了减少盗用，JWT 的有效期应该设置得比较短。对于一些比较重要的权限，使用时应该再次对用户进行认证。

（6）为了减少盗用，JWT 不应该使用 HTTP 协议明码传输，要使用 HTTPS 协议传输。



https://www.cnkirito.moe/jwt-learn/

https://www.cnkirito.moe/jwt-learn-3/

https://www.ruanyifeng.com/blog/2018/07/json_web_token-tutorial.html

https://zhuanlan.zhihu.com/p/70275218