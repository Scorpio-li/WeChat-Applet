<!--
 * @Author: Li Zhiliang
 * @Date: 2020-10-29 09:54:54
 * @LastEditors: Li Zhiliang
 * @LastEditTime: 2020-12-14 23:15:20
 * @FilePath: /WeChat-Applet/README.md
-->
# WeChat-Applet
微信小程序学习及实例

## framework(TypeScript + uniApp + uView 搭建微信小程序项目框架)

### 1、创建uniapp项目

```shell
vue create -p dcloudio/uni-preset-vue ts-uni-mini(这里是项目名称）
```

选择 默认模版（TypeScript)

创建完进入项目

cd ts-uni-mini

### 2、在新项目的vue文件中使用内联ts

按需引入vue装饰器(App.vue)

```js
import { Component,Vue ,Watch} from "vue-property-decorator";
```

不管干啥先把下面这句话加上。

@Component({}) //必须

```shell
启动项目 npm run dev:mp-weixin
```

### 3、打开微信开发者工具，导入项目

### 4、引入uView

1. 安装uView

npm install uview-ui

2. 在 sfc.d.ts 文件添加声明

declare module 'uview-ui'

3. 引入uView主JS库

在项目根目录中的main.ts中，引入并使用uView的JS库，注意这两行要放在import Vue之后。

```js
import uView from "uview-ui"; Vue.use(uView);
```

4. 在引入uView的全局SCSS主题文件

在项目根目录的uni.scss中引入此文件。 /* uni.scss */ @import 'uview-ui/theme.scss';

5. 在 App.vue 引入uView基础样式

/* 注意要写在第一行，同时给style标签加入lang="scss"属性 */ @import "uview-ui/index.scss";

6. 配置easycom组件模式

此配置需要在项目根目录的pages.json中进行。

uni-app为了调试性能的原因，修改easycom规则不会实时生效，配置完后，您需要重启HX或者重新编译项目才能正常使用uView的功能。

请确保您的pages.json中只有一个easycom字段，否则请自行合并多个引入规则。

```js
// pages.json { "easycom": { "^u-(.*)": "uview-ui/components/u-1/u-1/u−1.vue" } }
```

[项目地址](https://github.com/ysm27/TypeScript-uniApp-uView-wechat)