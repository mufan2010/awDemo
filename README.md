# 微信阿里相关组件

## 兼容性

* Python
* Django

注：如果稍以修改可适用于任意py框架 

## 使用虚拟环境(virturalenv)

```
pip3 install virtualenv

virtualenv env
source env/bin/activate

pip install -r requirements.txt

git checkout -b YOUR-USERNAME

# 期望在新分支进行功能开发

```

## 使用

```
# 支付类使用

> from utils.ali.api import ali_api
> ali_api.pay.pc.direct("洗发水", "1231312", "100", "http://www.notycy.com")

#微信jsapi支付：
from utils.wx.api import wx_api
wx_pay = wx_api.pay.jsapi.WeChatJSAPI("prepay_id", "timestamp=None", "nonce_str=None")
wx_order = wx_api.pay.order.WeChatOrder("body", "out_trade_no", "total_fee", "spbill_create_ip", "notify_url", "JSAPI")

# 消息类使用

> from utils.wx.api import wx_api
> wx_api.client.message.send_text("ogPhC1Il5Vy4YmHR4PM3c3WqKOKE", "日天同学，你洗洗头好不好")

```
