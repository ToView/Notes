## Postman Pre-request Script demo  



使用 Postman 发送请求,在发送请求之前执行脚本  

使用脚本生成接口请求签名(MD5签名)  

#### 常用签名规则

请求参数按照ASCII码从小到大排序，追加秘钥，再进行MD5加密得到签名值`sign`。具体步骤如下：
首先，构造待签名字符串。待签名字符的生成规则如下：

1. 请求参数都按照名称ASCII码，升序排列(参数名称不允许相同)
2. 如果参数值带有中文， 需要制定字符集编码为UTF-8
3. 如果参数值为空，那么该参数不参与签名
4. 秘钥作为最后一个参数， 参数名为：key 将请求参数按上述顺序用`&`拼接。 然后，用MD5算法，对待签名字符串进行加密， 生成的签名数据（32位字符）， 即是参数中`sign`的值。

待签名字符串示例:  

```
accessToken=d36476fa4de57fd2bb0d466f001ceca6&appId=10010&clientGuid=a55f2085-d40b-407f-9780-3d126739af09&clientTimestamp=1531377612&clientVersion=1&key=fe515a9ce6e3967cd0ab3417bc975f51
```



Postman 内置变量:  

| 变量名     | 使用           | 描述                       |
| ---------- | -------------- | -------------------------- |
| guid       | {{$guid}}      | GUID,设备识别码            |
| timestamp  | {{$timestamp}} | 精确到秒的时间戳(10位数字) |
| randdominT | {{$randomInt}} | 1-1000以内的随机整数       |

脚本使用示例：

Pre-request:  

```javascript
var appId = 1001;
var clientTimestamp = parseInt((new Date()).getTime() / 1000);  // 时间戳(精确到秒,10位数字)
var clientGuid = require('uuid').v4();  // GUID

pm.environment.set("appId", appId);
pm.environment.set("clientTimestamp", clientTimestamp);
pm.environment.set("clientGuid", clientGuid);



var params = JSON.parse(request.data);
var keys = Object.keys(params).sort() //请求参数名按照ASCII码升序排序

console.log("keys: " + keys);

//拼接待签名字符串
var str = []
for (var p = 0; p < keys.length; p++) { 
    if(keys[p] == "sign" || pm.environment.get(keys[p]) === ""){ // "==" ==宽松相等，隐性类型转换，值相等，返回true; "===" 严格相等，值和类型都相等，返回true
        continue;
    }
    str.push(keys[p] + "=" +pm.environment.get(keys[p]));
}
str.push('key=' + "fe515a9ce6e3967cd0ab3417bc975f51")
var sign = str.join("&");

console.log("signStr: " + sign);

//MD5加密签名规格，并赋值给环境变量`sign`
pm.environment.unset("sign");
pm.environment.set("sign", CryptoJS.MD5(sign).toString());


```



Body:  

```json
{
    "appId":"{{appId}}",
	"clientTimestamp":"{{clientTimestamp}}",
	"clientGuid":"{{clientGuid}}",
	"sign":"{{sign}}"    
}
```



Headers:  

| key          | Value            |
| ------------ | ---------------- |
| Content-Type | application/json |



