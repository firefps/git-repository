# git-repository

oauth 授权码模式验证流程

parm1:response_type=code,client_id='客户端的ID,必选项',redirect_uri='表示重定向URI,可选项',scope='表示申请的权限范围可选项',state='表示客户端的当前状态,可以指定任意值,认证服务器会原封不动地返回这个值'.

1.client--parm1-->授权服务器

2.授权服务器-->需要resouce owner确认是否授权

parm2:授权码

3.resouce owner确认后授权服务器 重定向--parm2-->client

parm3:授权码,重定向地址

4.client --parm3--> 授权服务器

parm4:access_token:表示访问令牌,必选项;token_type 表示令牌类型,该值大小写不敏感,必选项,可以是bearer类型或mac类型;expires_in:表示过期时间,单位为秒.如果省略该参数,必须其他方式设置过期时间;refresh_token:表示更新令牌,用来获取下一次的访问令牌,可选项。scope:表示权限范围,如果与客户端申请的范围一致,此项可省略.

5.授权服务器 --parm4--> client

6.client--access_token-->资源服务器申请资源
