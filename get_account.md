## 获取个人资产信息

POST /get_account

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
		<td>created</td>
		<td>是</td>
		<td>10位请求时间的时间戳</td>
	</tr>
	<tr>
		<td>market</td>
		<td>否</td>
		<td>交易市场类型，此项不参与签名</td>
	</tr>
	<tr>
		<td>sign</td>
		<td>是</td>
		<td>md5签名结果:sign=md5(key=xxx&created=xxxxx)</td>
	</tr>
</table>

返回结果：

<table>
	<tr>
		<td>字段名</td>
		<td>描述</td>
	</tr>
	<tr>
		<td>total</td>
		<td>总资产</td>
	</tr>
	<tr>
		<td>available_cny</td>
		<td>可用人民币</td>
	</tr>
	<tr>
		<td>available_tk</td>
		<td>可用唐币</td>
	</tr>
</table>