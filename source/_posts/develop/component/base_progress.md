---
title: progress 进度条
header: develop
nav: component
sidebar: base_progress
---


**解释**：进度条

**百度APP中扫码体验：**

<img src="https://b.bdstatic.com/miniapp/assets/images/doc_demo/progress.png"  class="demo-qrcode-image" />



## **属性说明**

|属性名 |类型  |默认值  | 必填 |说明|
|---- | ---- | ---- |---- |---- |
| percent | Float  | | 否 |百分比 0~100 |
| show-info | Boolean  | false  | 否 |在进度条右侧显示百分比|
| stroke-width | Number/String | 2 | 否 |进度条线的宽度，单位 px|
| color | Color  | #09BB07 | 否 |进度条颜色 （请使用 activeColor）	|
| activeColor | Color  | #09BB07 | 否 | 已选择的进度条的颜色	|
| backgroundColor |  Color | #E6E6E6 | 否 |未选择的进度条的颜色	|
| active | Boolean  | false  | 否 |进度条从左往右的动画	|
| active-mode | String  | backwards  | 否 |backwards: 动画从头播；forwards：动画从上次结束点接着播	|

## 示例
### **图片示例**

<div class="m-doc-custom-examples">
    <div class="m-doc-custom-examples-correct">
        <img src="https://b.bdstatic.com/miniapp/images/progress.jpeg">
    </div>
    <div class="m-doc-custom-examples-correct">
        <img src=" ">
    </div>
    <div class="m-doc-custom-examples-correct">
        <img src=" ">
    </div>     
</div>

### **代码示例1 - 显示百分比** 

<a href="swanide://fragment/855d7136e81ee2bce14311337a708e141575545470490" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 swan 文件中

```html
<view class="wrap">
    <view class="card-area">
        <view class="top-description border-bottom">
            <view>显示当前百分比</view>
            <view>show-info</view>
        </view>
        <progress class="progress" percent="40" activeColor="#3c76ff" show-info active />
    </view>
</view>
```

**代码示例2 - 自定义样式** 

<a href="swanide://fragment/4d0714c06064cc9e29e668f8295fb59a1575545655098" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 swan 文件中

```html
<view class="wrap">
    <view class="card-area">
        <view class="top-description border-bottom">默认样式</view>
        <progress class="progress" percent="20" activeColor="#3c76ff"/>
    </view>
    <view class="card-area">
        <view class="top-description border-bottom">
            <view>自定义样式</view>
            <view>stroke-width="7" activeColor="#00BC89"</view>
        </view>
        <progress class="progress" percent="60" activeColor="#00BC89" stroke-width="7" active />
    </view>
</view>
```

**代码示例3 - active-mode属性** 

<a href="swanide://fragment/83a75e26865f007b957d51434d562ce91575545714578" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 swan 文件中

```html
<view class="wrap">
    <view class="card-area">
        <view class="top-description border-bottom">显示动画</view>
        <progress class="progress" percent="70" color="#38f" active active-mode='backwards'/>
        <progress class="progress" percent="80" color="#38f" active active-mode='forwards'/>
    </view>
</view>
```


**图片示例**：

<div class="m-doc-custom-examples">
    <div class="m-doc-custom-examples-correct">
        <img src="https://b.bdstatic.com/miniapp/images/process.png">
    </div>
    <div class="m-doc-custom-examples-correct">
        <img src=" ">
    </div>
    <div class="m-doc-custom-examples-correct">
        <img src=" ">
    </div>     
</div>


**代码示例2：设置圆角progress**：

<a href="swanide://fragment/5b39c74d2356ad926786f66d9da753ce1573046087456" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 swan 文件中

```html
<view class="wrap">
    <progress class="progress" percent="60" activeColor="#3c76ff" stroke-width="10" active />
</view>
```

* 在 css 文件中

```css
.wrap {
    padding: 0.3rem 0.15rem;
}
.progress-bar, //外层圆角
.progress-inner-bar {//内层圆角
    border-radius: 30rpx;
}
```
