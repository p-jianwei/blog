# BFC规范

## 1、概念

- 格式化上下文（Formatting content）是W3C CSS2中规范的一个概念。页面中的一个渲染区域，有一套渲染规则，决定了其子元素将如何定位，以及和其他元素的关系和相互作用。
- 块级格式化上下文（Block Formatting content），属于上述规范的一种，具有BFC特性的元素可以看作是隔离了的独立容器，容器里面的元素不会在布局上影响到外面的元素，并且具有普通容器所没有的一些特性。

## 2、触发BFC

- **float**：除none以外的值
- **position**：absolute、fixed
- **display**：inline-block、table-cells、flex
- **overflow**：除了visible以外的值（hidden、auto、scroll）

## 3、特性及应用

- 解决margin叠加问题（上下）
- 解决margin传递问题（嵌套）
- 解决float浮动问题（父子元素，子元素浮动脱离文档流，父元素没有撑开）
- 解决覆盖问题（上下，上元素浮动，下元素文字排布受影响）