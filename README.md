原项目：https://gist.github.com/BlueSkyXN/f451b01af21bbda885d191444356401f

# 为什么要签到答题？

坚持签到和答题一年17*365=6205成长值，相当于开三年会员赠送的成长值，再算上svip每天30（一年10950）的成长值，只要成长值到10w，减去1.5万开通v10，可以实现正常续费无限v10（引用自：https://hostloc.com/thread-1392878-1-1.html）

# 为什么有这个项目

因为上面说的，所以我一直有签到的需求，最开始发现 [qd](https://github.com/qd-today/qd) 上面有现成的，但是发现不够方便，又在网上搜寻一番发现了

https://www.blueskyxn.com/202410/7228.html 这一篇博文，里面有现成的代码，能在ql上面使用，就拿过来叫大模型改了改。

# Cookie获取

打开：https://pan.baidu.com ，F12，网络，main文档里面把cookie，全部弄到变量里面，我的变量为 `XFI=***ndut_fmt=***`（只列出了开头和结尾两个变量）


这个 [fork](https://gist.github.com/RunwangGuo/48d98ff5763c9a3883907e9a593e18fb ) 的修改应该是只需要 `  "BDUSS=xxxx; BAIDUID=xxxx;" ` 但是我找不到 BAIDUID 这个变量

# 通知配置

## TG通知

需要配置以下环境变量：
- `TG_BOT_TOKEN`: Telegram机器人Token
- `TG_USER_ID`: Telegram聊天ID

## 飞书通知

需要配置以下环境变量：
- `FEISHU_WEBHOOK_URL`: 飞书机器人Webhook URL（必填）
- `FEISHU_SECRET`: 飞书机器人安全密钥（可选，如果机器人配置了签名校验则需要填写）

### 飞书机器人配置步骤

1. 在飞书群聊中添加自定义机器人
2. 复制Webhook地址，设置为环境变量 `FEISHU_WEBHOOK_URL`
3. 如果启用了签名校验，将密钥设置为环境变量 `FEISHU_SECRET`

# TG通知示例

当天第一次成功签到

![image](https://raw.githubusercontent.com/tunecc/DuPan/refs/heads/main/resources/photo/first.jpg)

当天重复签到

![image](https://raw.githubusercontent.com/tunecc/DuPan/refs/heads/main/resources/photo/repeat.jpg)

# 注意（[引用自原文](https://www.blueskyxn.com/202410/7228.html)）

基于Python，需要Cookie

建议在本地或固定登录百度网盘的设备（包括Windows服务器、Alist）使用，避免多IP风控。

不建议使用云函数，因为动态IP。

虽然百度的大部分风控不影响签到，但是会影响你下载。