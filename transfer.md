## 转账

POST /transfer

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
		<td>account_from</td>
		<td>是</td>
		<td>转出账户</td>
	</tr>
	<tr>
		<td>account_to</td>
		<td>是</td>
		<td>转入账户</td>
	</tr>
	<tr>
		<td>amount</td>
		<td>是</td>
		<td>转账数量</td>
	</tr>
	<tr>
		<td>created</td>
		<td>是</td>
		<td>10位提交时间戳</td>
	</tr>
	<tr>
		<td>sign</td>
		<td>是</td>
		<td>md5签名结果:sign=md5(account_from=xxx&account_to=xxx&amount=xxx&created=xxx&key=xxx)</td>
	</tr>
</table>

返回结果：

<table>
	<tr>
		<td>字段名</td>
		<td>描述</td>
	</tr>
	<tr>
		<td>id</td>
		<td>转账记录id</td>
	</tr>
	<tr>
		<td>result</td>
		<td>转账结果，成功为success，失败为failure</td>
	</tr>
</table>