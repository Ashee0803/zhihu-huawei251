# zhihu-huawei251
自动发布知乎试图打压的内容

## 制作原因
华为员工离职后被诬告羁押251天，事件发酵后在知乎先是被降热度——明明关注量是热榜第一的十多倍，却只能排到十多名——最后直接被删问题了。我也理解知乎说自己收到了律师函。可是第一，相关内容真的侵犯华为的**合法**权益了吗？真的违反法律法规了吗？第二，即使真的华为法务部门太厉害知乎没办法，用户自发以知乎删不过来的速度发布内容，总不是知乎的错了吧，总不会被华为告了吧(是吗?)。

因此，我决定发起这场行为艺术，用技术和人民的汪洋大海对抗资本对言论、信息自由的压制

## 使用方法
该脚本使用非常简单，不需要任何编程基础。只需要复制代码到浏览器的控制台(console)中即可。Chrome为例，点击F12打开，找到console：

![](cons1.png)

将脚本的内容粘贴进去。如果希望匿名发布，只需要删掉匿名部分的注释。

![](cons2.png)

```
/*
	var xhr_an = new XMLHttpRequest();
	var url_an = 'https://www.zhihu.com/api/v4/questions/'+id+'/anonyms';
	xhr_an.open("POST", url_an, true);
	xhr_an.send();
*/
```

改为

```
	var xhr_an = new XMLHttpRequest();
	var url_an = 'https://www.zhihu.com/api/v4/questions/'+id+'/anonyms';
	xhr_an.open("POST", url_an, true);
	xhr_an.send();
```

点回车。

完成上诉步骤后，再输入 ``A()`` 点回车，就会给当前页面下所有问题自动添加回答。可以在首页通过下拉加载自行控制想多发还是少发。
（之所以有这一步，是因为未来还计划写``Q()``函数自动添加问题。）

## 自定义
文字内容、间隔时间等都可以自定义
