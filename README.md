# 抖音协议 X-Gorgon 0408 和8408 算法定位查找过程笔记，抖音爬虫必看


### **介绍：**

# **本次分析抖音版本：13.3    **

# **X-Gorgon版本：0408  和 8408  可测试**
**本次直接开始讲解分析0408和8408的区别。至于逆向记录可以参考我之前的文章！**<br>小编自恋一下,逆向大神 属于逆向爱好者，如需要交流技术或者算法请在评论区留言<br>
<br>**如果最近更新了新版抖音的app的人应该已经发现了，抖音安卓版的xg算法开头也变成了8408开头，因为84开头之前都是ios平台上的xg算法，到目前为止，IOS平台的xg还是8404开头。**<br>![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607476459483-4c47b95b-46ce-4cbe-9b2d-1ac5fbcbb018.png#align=left&display=inline&height=149&margin=%5Bobject%20Object%5D&name=image.png&originHeight=298&originWidth=1229&size=53126&status=done&style=none&width=614.5)<br>**<br>**最近抖音更新到13.x版本以后，抓包会发现，xg变成了8408开头。我一开始是惊讶，怎么现在安卓端也开始跟ios端的xg算法一样了？于是我下功夫研究了一下。发现了猫腻所在。**如下图<br>![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607476471756-94bb9949-b021-4853-8323-625bb81d533a.png#align=left&display=inline&height=302&margin=%5Bobject%20Object%5D&name=image.png&originHeight=603&originWidth=841&size=45866&status=done&style=none&width=420.5)<br> <br> <br> <br> <br>抖音app先是检测了你的手机cpu架构，是x86还是armeabi，通过cpu架构的不同来调用so内不同的xg方法，所以导致现在最新版抖音app的xg算法有0408和8408两种。<br>两种都是最新版，因为我发现当我使用oppo手机安装最新版抖音抓包的xg是8408，而当我用小米或者华为安装最新版抖音，抓包以后发现xg是0408。<br>下图是X-Gorgon具体的校验逻辑。<br>
<br>![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607476488273-70666e0d-e3a4-4264-a1e1-695a99b9d290.png#align=left&display=inline&height=464&margin=%5Bobject%20Object%5D&name=image.png&originHeight=928&originWidth=1331&size=100281&status=done&style=none&width=665.5)<br> 

## 总结
        以上就是对抖音对一个简单的x-gorgon的分析笔记过程，希望能够有所帮助，也能够对自身的产品安全方面进行一个参考借鉴。<br>
<br>

> TiToData：专业的短视频、直播数据接口服务平台。

> 更多信息请联系： [TiToData](https://www.titodata.com?from=douyinarticle)
> 覆盖主流平台：抖音，快手，小红书，TikTok，YouTube

