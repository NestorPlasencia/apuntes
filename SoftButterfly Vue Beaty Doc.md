# Vue Beauty

## Develpment Guide

### Start

# view-beauty

Vue-beauty is a set of PC-side UI component library based on vue.js and ant-design styles designed to help developers improve product experience and development efficiency and reduce maintenance costs.

## [¶](https://fe-driver.github.io/vue-beauty/#te-xing) properties

- Rich components, covering common scenes
- Based on vue component development, data-driven view
- Packaging complexity, providing a simple and friendly api
- Based on ant design style optimization

## [¶](https://fe-driver.github.io/vue-beauty/#yin-ru) introduced

Use npm or yarn

```javascript
    npm install vue-beauty -S 
    //OR
    yarn add vue-beauty

    import Vue from 'vue'

    //import css
    import 'vue-beauty/package/style/vue-beauty.min.css'

    //import components
    import vueBeauty from 'vue-beauty'
    Vue.use(vueBeauty)

    //OR
    import {alert} from 'vue-beauty'
    Vue.use(alert)
```

Or use a <script> global reference

```
    <link rel="stylesheet" href="vue-beauty.min.css"> 
    <script type="text/javascript" src="vue-beauty.min.js"></script> 
```

Example

```
    <template>
        <v-button>按钮</v-button>
    </template>
```

effect
Buttons

## [¶](https://fe-driver.github.io/vue-beauty/#ban-ben) version

 

![img](http://img.shields.io/npm/v/vue-beauty.svg)

 

 

 

## [¶](https://fe-driver.github.io/vue-beauty/#liu-lan-qi-zhi-chi) Browser Support

Chrome, firefox, IE is not supported (planned to support IE11+)

## [¶](https://fe-driver.github.io/vue-beauty/#xiang-guan-lian-jie) Related Links

- [Vue official website](http://cn.vuejs.org/)
- [awesome vue](https://github.com/vuejs/awesome-vue)
- [Getting Started with ES2015](http://es6.ruanyifeng.com/)
- [webpack](https://doc.webpack-china.org/)

## [¶](https://fe-driver.github.io/vue-beauty/#xiang-guan-kai-yuan-xiang-mu) related open source projects

The vue-beauty part code refers to the following items:

- [Ant Design](https://github.com/ant-design/ant-design/)
- [Element](https://github.com/ElemeFE/element)
- [view-ANTD](https://github.com/okoala/vue-antd)
- [iview](https://github.com/iview/iview)

## [¶](https://fe-driver.github.io/vue-beauty/#shui-zai-shi-yong) Who uses

- [Huitong world](http://www.g7.com.cn/)





## When to Use

- Need to indicate switching state/switching between two states;
- And `checkbox`the difference is switched `switch`directly trigger state changes, and `checkbox`are generally used for status flags, and commit operations require complex.

## [¶](https://fe-driver.github.io/vue-beauty/#dai-ma-yan-shi) code demonstrates

#### simple

The simplest usage.

Toggle disabled

#### unavailable

Switch failure state.

turn off 

#### Text and icons

With text and icons.

#### Two sizes

`size='small'` Said small switch

 Get status code

#### Custom status value

Property Name: The `true-value` `false-value`
following example defines: 1 when checked, 0 if not 
selected