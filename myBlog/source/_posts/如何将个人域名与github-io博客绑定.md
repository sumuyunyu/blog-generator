---
title: 如何将个人域名与github.io博客绑定
date: 2020-12-01 10:04:03
banner_img: /img/banner_1.jpg
categories:
- Hexo博客搭建
tags:
- 博客
- hexo
typora-root-url: ../../source
---

1. 首先到[NameSilo](https://www.namesilo.com/) 购买域名，可以使用支付宝，相对比较便宜，后面假设你买的域名叫 yoursite.com

   ![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201120911933-6795879.png)

   

2. 到你的github博客仓库下（username.github.io），点击Settings，还不知道如何搭建博客的，建议搜索hexo+github，我也可能会出一个教程 

   ![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201121519275.png)

 在GitHub Pages下有个Custom domain，写下你的域名（如 yoursite.com），注意不需要写www、http，域名就行，然后点击Save

![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201121948167.png)

3. 使用[Dnspod](https://www.dnspod.cn/) 免费进行域名解析，先注册一下，首页下面会有一个DNS域名解析（域名解析需要实名登记，整一下就行）

   ![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201122413723-6800032.png)

进入控制台，有一个添加域名，把你要绑的域名填上

![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201122552755-6796793.png)

添加后提示DNS错误，如下，没关系

![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-error.png)

到域名注册的地方，也就是[Namesilo](https://www.namesilo.com/account_home.php) 那里点击Manage My Domains 

![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201124241196.png)

点击你的域名，进入Domain Console，点击Change修改DNS服务器，把刚才DNS错误提示中的两个网址填进去，默认的网址去掉就行

![image-20201201124759108](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201124759108.png)

然后回到Dnspod，点击已经添加好的这个域名，进行添加记录，注意185.199.108.153是ping username.github.io 得到的，把username换成你的github用户名

![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/image-20201201122849966-6796963.png)

```
@ A 185.199.108.153
@ A 185.199.109.153
www CNAME username.github.io
```

如下

![](/images/%E5%A6%82%E4%BD%95%E5%B0%86%E4%B8%AA%E4%BA%BA%E5%9F%9F%E5%90%8D%E4%B8%8Egithub-io%E5%8D%9A%E5%AE%A2%E7%BB%91%E5%AE%9A/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-12-01%20%E4%B8%8B%E5%8D%8812.53.07.png)

4. 好了，大功告成，耐心等待，域名在网络上解析还需要一定的时间，不出半天就能稳定访问了🎉🎉🎉