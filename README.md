# 说明文档

## XML格式

地形的XML文件由用户提供，描述了一个地形的名字、大小和形状，其中value标签中的数字表示了该点的高度。格式为：

	<graph>
		<size></size>
		<name></name>
		<map type="array">
			<values type="array">
				<value></value>
			</values>
		</map>
	</graph>

## 绘制方法

我们在前台完成所有的工作，并使用了Javascript和Three.js。

1. 首先读取XML并对其进行解析
2. 然后使用Three.js根据XML中的map绘制出三维网格
3. 最后为三维网格添加旋转动画来更好地展示它
