# Vue3、TypeScript和ArcGIS Api搭建地图应用

## vite搭建项目

1. 安装vite:

    `yarn create @vitejs/app`

2. vite使用vue3和ts预设模板创建项目

    `yarn create @vitejs/app my-vue-app --template vue-ts`

3. 安装arcgis api模块库

    `yarn add @arcgis/core`

## demo开发

1. 引入样式

    在`App.vue`中`style`下引入:

    ` @import "https://js.arcgis.com/4.19/@arcgis/core/assets/esri/themes/light/main.css"; `

2. 引入模块

    `components`目录下创建`BaseMap.vue`组件，使用`ESM`引入各个模块：

    ` import TileLayer from '@arcgis/core/layers/TileLayer' `

    具体引入路径可参考Arcgis api 官方文档

## 预览打包

    `yarn dev`

    `yarn build`
