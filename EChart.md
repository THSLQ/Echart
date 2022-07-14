## Echarts Study  
快速上手：https://echarts.apache.org/handbook/zh/basics/download  


## ECharts API

一、	全局echarts对象，在script标签引入echarts.js文件后获得，或者在AMD环境中通过require(‘echarts’)
1?:	echarts.init()方法 初始化ECharts实例
	创建一个ECharts实例，返回echartInstance，不能在单个容器上初始化多个ECharts实例(Instance)。
	语法：
		var <name> = echart.init( dom: HTMLDivElement | HTMLCanvasElement, 
theme?: Object | string,
opts?:{
devicePixelRatio?: number,
renderer?: string,
useDirtyRect?: Boolean,
width?: number | string,
height?: number | string,
locale?: string
});
		参数说明：
			①dom：实例容器，一般是一个具有高宽的div元素。
ECharts 3支持直接使用canvas元素作为容器，这样绘制完图标可以直接将canvas作为图片应用到其他地方，例如在WebGL中作为贴图，这跟使用echartsInstance.getDataURL生成图片链接相比可以支持图标的实时刷新。
②theme：应用的主题。可以是一个主题的配置对象，也可以是使用已经通过echarts.registerTheme注册的主题名称.
③
