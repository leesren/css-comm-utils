# Usage

> 常用的 CSS 工具类库

** NPM **

```sh

npm install --save css-comm-utils

```

使用 your `.scss` file

```css
@import '~css-comm-utils';
```

如果需要覆盖默认的设置

```css
@import './variable.scss';
@import '~css-comm-utils';
```

your `variable.scss`

```css
$color-primary: #da0ab6;

$lighten-num: 10%;
$darken-num: 10%;
```

## 颜色

颜色区分 `字体颜色` 和 `背景色`

- `primary: #4285f4 !default;`
- `danger: #f04141 !default;`
- `warn: #f85 !default;`
- `success: #51c43f !default;`
- `dark: #262626 !default;`
- `light: #f4f5f8 !default;`
- `white: #fff !default;`

**深色** ， 原来的基础上 `darken($color-primary, $darken-num)`

`$darken-num: 6% !default;`

**浅色**， 原来的基础上 `lighten($color-dark, $lighten-num)`

`$lighten-num: 6% !default;`

字体颜色定义方式:

- `primary`

primary 颜色字体,

- `primary-d`

深色的 primary 字体颜色

- `primary-l`

浅色的 primary 字体颜色

- `primary-bg`

primary 颜色背景色,

- `primary-bgd`

深色的 primary 背景色

- `primary-bgl`

浅色的 primary 背景色

同理 `danger`，`warn`，`success`，`dark`， `light`

唯一区别 `white`

white 只有 `white-bg`, `white-bgd`,`white`, `white-d`

基础字体颜色：

- tx-pc

主要文字颜色

- tx-rc

常规文字 regular

- tx-sc

次要文字 secondary

- tx-hc

占位文字 placeholder

## 布局系统

项目提供了常见的布局 方案 `flex` , `文本布局`, `定位`, `清除浮动`, `滚动`

```scss
/********************** display: flex **********************/
.fbox {
  display: flex;
}
// 垂直方向
.fbox-h {
  display: flex;
  flex-direction: row;
}
// 垂直居中
.fbox-vc {
  display: flex;
  align-items: center;
}
// 水平垂直居中
.fbox-hvc {
  display: flex;
  align-items: center;
  justify-content: center;
}
// 垂直方向
.fbox-v {
  display: flex;
  flex-direction: column;
}

// 垂直 垂直居中
.fbox-v-vc {
  display: flex;
  flex-direction: column;
  align-items: center;
}
// 垂直 垂直水平居中
.fbox-v-vhc {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.flex-vc {
  align-items: center;
}
.flex-hc {
  justify-content: center;
}
.flex-hvc {
  justify-content: center;
  align-items: center;
}

.flex-wrap {
  flex-wrap: wrap;
}
// between
.flex-hb {
  justify-content: space-between;
}
// around
.flex-ha {
  justify-content: space-around;
}
// end
.flex-he {
  justify-content: flex-end;
}

//  align-items: flex-start;
.flex-vs {
  align-items: flex-start;
}
.flex-ve {
  align-items: flex-end;
}
// stretch
.flex-vt {
  align-items: stretch;
}
// align-self
.self-start {
  align-self: flex-start;
}
.self-end {
  align-self: flex-end;
}

.flex {
  flex: 1;
}
@include flex();

/********************** block **********************/
.block-center {
  margin-left: auto;
  margin-right: auto;
}

.inblock {
  display: inline-block;
}
.block {
  display: block;
}

.hide {
  display: none;
}
/********************** 清除浮动 **********************/
.clearfix:after {
  display: table;
  content: ' ';
  clear: both;
  line-height: 0;
}

/********************** overflow **********************/
.over-hi {
  overflow: hidden;
}
.over-hiy {
  overflow-y: hidden;
}
.over-hix {
  overflow-x: hidden;
}
.over-auto {
  overflow: auto;
}
.over-sy {
  overflow-y: auto;
}
.over-sx {
  overflow-x: auto;
}
.over-smooth {
  -webkit-overflow-scrolling: touch;
}

.pointer {
  cursor: pointer;
}

/********************** 定位 **********************/
.posi-re {
  position: relative;
}
// 绝对
.posi-ab {
  position: absolute;
}
// fixed
.posi-fx {
  position: fixed;
}
/*static*/
.posi-st {
  position: static;
}
/*固定定位*/
.posi-sk {
  position: sticky;
}
/********************** 定位居中 **********************/
.posi-hc {
  left: 50%;
  transform: translateX(-50%);
}
.posi-vc {
  top: 50%;
  transform: translateY(-50%);
}
.posi-hvc {
  top: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

/********************** background-size **********************/
.bg-sico {
  background-size: cover;
}
.bg-sict {
  background-size: contain;
}
/********************** visibility **********************/
.visi-hide,
.invisi {
  visibility: hidden;
}
.visi {
  visibility: visible;
}
/********************** 响应式 **********************/
@include col-list();
```

定义方式

`v` 前缀的代表垂直方向, `h` 表示水平方向

## 字体大小

项目提供了 `font-size` 从

```scss
$font-size-start: 8;
$font-size-end: 30;
```

会生成 fs8, fs9, fs10 , ... , fs30 的 `font-size` 类

如果要设置 css `font-size:10px` 只需 `fs10`

## border

## 间距

项目提供了 padding 和 margin 两个常用间距设置

```scss
@include gap('50', 50px);
@include gap('45', 45px);
@include gap('40', 40px);
@include gap('35', 35px);
@include gap('32', 32px);
@include gap('30', 30px);
@include gap('28', 28px);
@include gap('25', 25px);
@include gap('23', 23px);
@include gap('20', 20px);
@include gap('18', 18px);
@include gap('15', 15px);
@include gap('12', 12px);
@include gap('10', 10px);
@include gap('8', 8px);
@include gap('5', 5px);
@include gap('4', 4px);
@include gap('3', 3px);
@include gap('2', 2px);
@include gap('0', 0);
```

上面的会生成 如 `@include gap('2', 2px);`

```css
.p2 {
  padding: 0;
}
.pt2 {
  padding-top: 2px;
}
.pr2 {
  padding-top: 2px;
}
.pb2 {
  padding-bottom: 2px;
}
.pl2 {
  padding-left: 2px;
}

.m2 {
  margin: 0;
}
.mt2 {
  margin-top: 2px;
}
.mr2 {
  margin-top: 2px;
}
.mb2 {
  margin-bottom: 2px;
}
.ml2 {
  margin-left: 2px;
}
```
