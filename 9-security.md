
# 安全

## 用户隐私信息保护

1. 用户密码非明文保存，加动态salt。
2. 身份证号，手机号如果要显示，用 “\*” 替代部分字符。
3. 联系方式在的显示与否由用户自己控制。
4. TODO

* [《个人隐私包括哪些》](https://zhidao.baidu.com/question/1988017976673661587.html)
* [《在互联网上，隐私的范围包括哪些？》](https://www.zhihu.com/question/20137108)

* [《用户密码保存》](https://coderxing.gitbooks.io/architecture-evolution/di-san-pian-ff1a-bu-luo/642-shu-ju-jia-mi/6425-jia-mi-chang-jing-ff1a-yong-hu-mi-ma-bao-cun.html)

## 序列化漏洞
* [《Lib之过？Java反序列化漏洞通用利用分析》](https://blog.chaitin.cn/2015-11-11_java_unserialize_rce/)

## 加密解密

[常见安全算法（MD5、SHA1、Base64等等）总结](https://github.com/Snailclimb/Java_Guide/blob/master/数据结构与算法/常见安全算法（MD5、SHA1、Base64等等）总结.md)

### 对称加密

* [《常见对称加密算法》](https://coderxing.gitbooks.io/architecture-evolution/di-san-pian-ff1a-bu-luo/642-shu-ju-jia-mi/6421-chang-jian-dui-cheng-jia-mi-suan-fa.html)
	* DES、3DES、Blowfish、AES
	* DES 采用 56位秘钥，Blowfish 采用1到448位变长秘钥，AES 128，192和256位长度的秘钥。
	* DES 秘钥太短（只有56位）算法目前已经被 AES 取代，并且 AES 有硬件加速，性能很好。
	
### 哈希算法
* [《常用的哈希算法》](https://coderxing.gitbooks.io/architecture-evolution/di-san-pian-ff1a-bu-luo/642-shu-ju-jia-mi/6422-chang-jian-ha-xi-suan-fa-and-hmac.html)
	* MD5 和 SHA-1 已经不再安全，已被弃用。
	* 目前 SHA-256 是比较安全的。
	
* [《基于Hash摘要签名的公网URL签名验证设计方案》](https://blog.csdn.net/zhangruhong168/article/details/78033202)

### 非对称加密
* [《常见非对称加密算法》](https://coderxing.gitbooks.io/architecture-evolution/di-san-pian-ff1a-bu-luo/642-shu-ju-jia-mi/6424-chang-yong-fei-dui-cheng-jia-mi-suan-fa.html)
	* RSA、DSA、ECDSA(螺旋曲线加密算法)
	* 和 RSA 不同的是 DSA 仅能用于数字签名，不能进行数据加密解密，其安全性和RSA相当，但其性能要比RSA快。
	* 256位的ECC秘钥的安全性等同于3072位的RSA秘钥。

		[《区块链的加密技术》](http://baijiahao.baidu.com/s?id=1578348858092033763&wfr=spider&for=pc)	


## 授权、认证
### RBAC 
* [《基于组织角色的权限设计》](https://www.cnblogs.com/zq8024/p/5003050.html)
* [《权限系统与RBAC模型概述》](https://www.cnblogs.com/shijiaqi1066/p/3793894.html)
* [《Spring整合Shiro做权限控制模块详细案例分析》](https://blog.csdn.net/he90227/article/details/38663553)

### OAuth2.0
* [《理解OAuth 2.0》](http://www.ruanyifeng.com/blog/2014/05/oauth_2_0.html)
* [《一张图搞定OAuth2.0》](https://www.cnblogs.com/flashsun/p/7424071.html)

### 双因素认证（2FA）

2FA - Two-factor authentication，用于加强登录验证

常用做法是 登录密码 + 手机验证码（或者令牌Key，类似于与网银的 USB key）

* 【《双因素认证（2FA）教程》】(http://www.ruanyifeng.com/blog/2017/11/2fa-tutorial.html)

### 单点登录(SSO)

* [《单点登录原理与简单实现》](https://www.cnblogs.com/ywlaker/p/6113927.html)

* [CAS单点登录框架](https://github.com/apereo/cas)
