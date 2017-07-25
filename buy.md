## 买入

POST /buy

<table>
	<tr>
		<td>字段名</td>
		<td>是否必填</td>
		<td>描述</td>
	</tr>
	<tr>
		<td>key</td>
		<td>是</td>
		<td>公钥</td>
	</tr>
	<tr>
		<td>coin_type</td>
		<td>是</td>
		<td>币种：1-唐币</td>
	</tr>
	<tr>
		<td>price</td>
		<td>是</td>
		<td>买入价格</td>
	</tr>
	<tr>
		<td>amount</td>
		<td>是</td>
		<td>买入数量</td>
	</tr>
	<tr>
		<td>created</td>
		<td>是</td>
		<td>10位提交时间戳</td>
	</tr>
	<tr>
		<td>sign</td>
		<td>是</td>
		<td>md5签名结果:sign=md5(amount=1&coin_type=1&created=xxx&key=xxx&price=1)</td>
	</tr>
	<tr>
		<td>password</td>
		<td>否</td>
		<td>如果开启下单输入密码，必须填此参数，不参与签名</td>
	</tr>
</table>

返回结果：

<table>
	<tr>
		<td>字段名</td>
		<td>描述</td>
	</tr>
	<tr>
		<td>result</td>
		<td>买入结果：成功则为success，失败为failure</td>
	</tr>
	<tr>
		<td>id</td>
		<td>交易id</td>
	</tr>
</table>