## 请求过程

1. 通过POST方式提交交易请求。

2. 请求头信息中必须声明Content-Type:application/x-www-form-urlencoded。

3. 根据接口请求返还对应的JSON格式数据。

4. 交易接口只支持https请求。

5. 生成sign时，参与签名的参数按照a-z字母排序，签名MD5必须是小写字母。

6. 签名时的字符一律采用UTF-8编码。
