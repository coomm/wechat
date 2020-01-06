# wechat
真机调试时微信小程序报错wx.request:fail ssl hand shake error，经检查发现服务器缺少中间证书，百度了很久都没有解决，网上的解决方法都是添加SSLCertificateChainFile配置项，然而这个配置项在apache2.4.8及以上版本已经废弃，最后发现改为SSLCACertificatePath即可
#私匙
SSLCertificateKeyFile private.key
#服务器证书
SSLCertificateFile server.pem
#客户端证书
#SSLCertificateChainFile ca.pem
SSLCACertificatePath ca.pem
