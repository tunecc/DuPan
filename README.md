原项目：https://gist.github.com/BlueSkyXN/f451b01af21bbda885d191444356401f

# 为什么要签到答题？

坚持签到和答题一年17*365=6205成长值，相当于开三年会员赠送的成长值，再算上svip每天30（一年10950）的成长值，只要成长值到10w，减去1.5万开通v10，可以实现正常续费无限v10（引用自：https://hostloc.com/thread-1392878-1-1.html）

# 为什么有这个项目

因为上面说的，所以我一直有签到的需求，最开始发现 [qd](https://github.com/qd-today/qd) 上面有现成的，但是发现不够方便，又在网上搜寻一番发现了

https://www.blueskyxn.com/202410/7228.html 这一篇博文，里面有现成的代码，能在ql上面使用，就拿过来叫大模型改了改。

# Cookie获取

插件方法：

* 下载插件 [Get Cookies](https://chromewebstore.google.com/detail/get-cookies/hdablekeodiopcnddiamhahahkiiloph)，（之前我用同类扩展获取cookies的无法使用，这个扩展获取的能用）

  打开 https://pan.baidu.com ，点击扩展插件

  ![https://chromewebstore.google.com/detail/get-cookies/hdablekeodiopcnddiamhahahkiiloph](https://lh3.googleusercontent.com/8PCDjNdA8k4hCluZQotnnAEvJzyQY-A3ZNvNQFPm9OUUeqqSmSb_Yfroz2smMkLGK44ukjiGnDHmm8Ho2ahv7B_P=s1280-w1280-h800)

  复制Cookies，粘贴到我们的脚本里面就可以使用了，

  注意，我们这个Cookies 需要使用单引号来包围 `''` 



手动方法：

* 打开：https://pan.baidu.com ，F12，网络，main文档里面把cookie，全部弄到变量里面，我的变量为 `XFI=***ndut_fmt=***`（只列出了开头和结尾两个变量）

  这个 [fork](https://gist.github.com/RunwangGuo/48d98ff5763c9a3883907e9a593e18fb ) 的修改应该是只需要 `  "BDUSS=xxxx; BAIDUID=xxxx;" ` 但是我找不到 BAIDUID 这个变量



# TG通知示例

当天第一次成功签到

![image](https://raw.githubusercontent.com/tunecc/DuPan/refs/heads/main/resources/photo/first.jpg)

当天重复签到

![image](https://raw.githubusercontent.com/tunecc/DuPan/refs/heads/main/resources/photo/repeat.jpg)

# 脚本说明

[VE.py](https://raw.githubusercontent.com/tunecc/DuPan/refs/heads/main/VE.py) ：参数写在脚本里面，任意一个能用python的地方都能使用，可以放在你的国内服务器

[du.py](https://raw.githubusercontent.com/tunecc/DuPan/refs/heads/main/du.py)：通过环境变量获取参数的，放在青龙面板上运行





# 注意（[引用自原文](https://www.blueskyxn.com/202410/7228.html)）

基于Python，需要Cookie

建议在本地或固定登录百度网盘的设备（包括Windows服务器、Alist）使用，避免多IP风控。

不建议使用云函数，因为动态IP。

虽然百度的大部分风控不影响签到，但是会影响你下载。



大家要改什么，添加什么通知方式，直接把脚本复制给大模型叫它改就好了



现在百度云有了一个新的签到，与本项目的签到可以共存，大家有时间的话还是可以登录去签到一下，多拿一份奖励