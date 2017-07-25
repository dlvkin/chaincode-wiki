## 查询个人最新成交订单

GET /get_orders

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
		<td>created</td>
		<td>是</td>
		<td>10位提交时间戳</td>
	</tr>
	<tr>
		<td>sign</td>
		<td>是</td>
		<td>md5签名结果:sign=md5(coin_type=1&created=xxx&key=xxx)</td>
	</tr>
</table>

返回结果：

orders: [订单列表，具体订单信息定义如下]

<table>
	<tr>
		<td>字段名</td>
		<td>描述</td>
	</tr>
	<tr>
		<td>id</td>
		<td>交易id</td>
	</tr>
	<tr>
		<td>type</td>
		<td>交易类型：1-限价买，2-限价卖，3-市价买，4-市价卖</td>
	</tr>
	<tr>
		<td>order_price</td>
		<td>订单价格</td>
	</tr>
	<tr>
		<td>order_amount</td>
		<td>订单数量</td>
	</tr>
	<tr>
		<td>order_time</td>
		<td>订单发生时间</td>
	</tr>
	<tr>
		<td>status</td>
		<td>交易状态：0-完成，1-未成交，2-部分成交，3-取消</td>
	</tr>
</table>