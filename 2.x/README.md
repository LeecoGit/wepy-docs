## WePY 2 (alpha)

[![npm version](https://badge.fury.io/js/%40wepy%2Fcore.svg)](https://badge.fury.io/js/%40wepy%2Fcore)
[![travis-ci](https://travis-ci.org/Tencent/wepy.svg?branch=2.0.x)](https://travis-ci.org/Tencent/wepy)
[![Coverage Status](https://coveralls.io/repos/github/Tencent/wepy/badge.svg?branch=2.0.x)](https://coveralls.io/github/Tencent/wepy?branch=2.0.x)
[![Dependency Status](https://david-dm.org/Tencent/wepy.svg)](https://david-dm.org/Tencent/wepy)

### 介绍

WePY资源汇总：[awesome-wepy](https://github.com/aben1188/awesome-wepy)

WePY (发音: /'wepi/) 项目启动于 2016 年 11 月份， 是小程序最早的框架之一，是一款让小程序支持组件化开发的框架，通过预编译的手段让开发者可以选择自己喜欢的开发风格去开发小程序。框架的细节优化，Promise，Async Functions的引入都是为了能让开发小程序项目变得更加简单，高效。

### 特性：

* 使用 Vue Observer 实现数据绑定
* 支持 Vue watch/computed/mixin 等特性
* 基于原生组件实现组件化开发
* 支持 TypeScript


### Demo

```html
<style lang="less">
    @color: #4D926F;
    .userinfo {
        color: @color;
    }
</style>
<template lang="pug">
    div(class='container')
        div(class='userinfo' @tap='tap')
            mycom(:prop='myprop' @fn='myevent')
            text {{now}}
</template>
<script>
    import wepy from '@wepy/core';

    wepy.page({
        data: {
            myprop: {}
        },
        computed: {
            now () { return new Date().getTime(); }
        },
        async onLoad() {
            await sleep(3);
            console.log('Hello World');
        },
        sleep(time) {
            return new Promise((resolve, reject) => setTimeout(resolve, time * 1000));
        },
    }
</script>
<config>
{
  usingComponents: {
    mycom: "~@/components/some-component"
  }
}
</config>
```



### 安装使用

#### 安装（更新） wepy 命令行工具。

```console
npm install @wepy/cli -g
```

#### 生成开发示例

```console
wepy init standard myproject
```

#### 安装依赖

```console
cd myproject
npm install
```

#### 开发实时编译

```console
npm run dev
```

#### 开发者工具导入项目

使用`微信开发者工具`新建项目，本地开发选择项目根目录，会自动导入项目配置。

### 哪些小程序是用 WePY 开发的

腾讯疫苗查询小程序、
腾讯翻译君小程序、
腾讯地图小程序、
玩转故宫小程序、
手机充值+、
手机余额查询、
手机流量充值优惠、
[友福图书馆](https://library.ufutx.com)[（开源）](https://github.com/glore/library)、
[素洁商城](https://github.com/dyq086/wxYuHanStore)[（开源）](https://github.com/dyq086/wxYuHanStore)、
[NewsLite](https://github.com/yshkk/shanbay-mina)[（开源）](https://github.com/yshkk/shanbay-mina)、
[西安找拼车](https://github.com/chenqingspring)[（开源）](https://github.com/chenqingspring)、
[深大的树洞](https://github.com/jas0ncn/szushudong)[（开源）](https://github.com/jas0ncn/szushudong)、
[求知微阅读](https://github.com/KingJeason/wepy-books)[（开源）](https://github.com/KingJeason/wepy-books)、
[给你的 iPhone X 换个发型](https://bangs.baran.wang/)、
[天天跟我买](http://www.xiaohongchun.com.cn/index)、
[坚橙](https://zhanart.com/wepy.html)、
群脱单、
米淘联盟、
帮助圈、
众安保险福利、
阅邻二手书、
趣店招聘、
[满熊阅读（开源：](https://github.com/Thunf/wepy-demo-bookmall) [微信小程序](https://github.com/Thunf/wepy-demo-bookmall)、[支付宝小程序）](https://github.com/Thunf/wepy-demo-bookmall/tree/alipay)、
育儿柚道、
平行进口报价内参、
GitHub掘金版、
班级群管、
鲜花说小店、
逛人备忘、
英语助手君、
花花百科、
独角兽公司、
爱羽客羽毛球、
斑马小店、
小小羽球、
培恩医学、
农资优选、
公务员朝夕刷题、
七弦琴小助手、
七弦琴大数据、
爽到家小程序、
[应用全球排行](https://github.com/szpnygo/wepy_ios_top)[（开源）](https://github.com/szpnygo/wepy_ios_top)、
[we川大](https://github.com/mohuishou/scuplus-wechat)[（开源）](https://github.com/mohuishou/scuplus-wechat)、
聊会儿、
[诗词墨客](https://github.com/huangjianke/weapp-poem)[（开源）](https://github.com/huangjianke/weapp-poem)、
[南京邮电大学](https://github.com/GreenPomelo/Undergraduate)[（开源）](https://github.com/GreenPomelo/Undergraduate)

...

### 交流群
 
 WePY 交流群已满500人，请加 gcaufy_helper 好友或者扫码加好友，验证回复 `wepy` 按照指引进群。

 ![wepy_qr_code](https://user-images.githubusercontent.com/2182004/32309877-8bded674-bfc9-11e7-9daa-9ba4012690fb.png)
             
### 参与贡献

如果你有好的意见或建议，欢迎给我们提 Issues 或 Pull Requests，为提升微信小程序开发体验贡献力量。<br>详见：[CONTRIBUTING.md](https://github.com/Tencent/wepy/blob/2.0.x/CONTRIBUTING.md)

[腾讯开源激励计划](https://opensource.tencent.com/contribution) 鼓励开发者的参与和贡献，期待你的加入。

### Links

[Documentation](https://tencent.github.io/wepy/)

[Changelog](https://tencent.github.io/wepy/document.html#/changelog)

[Contributing](https://github.com/Tencent/wepy/blob/2.0.x/CONTRIBUTING.md)

[License MIT](https://github.com/Tencent/wepy/blob/2.0.x/LICENSE)
