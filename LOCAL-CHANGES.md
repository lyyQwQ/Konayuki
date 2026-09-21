# 定制主题维护说明

维护仓库：https://github.com/lyyQwQ/Konayuki

## 安装

将 `konayuki-dark.css` 和 `konayuki-light.css` 复制到 Typora 主题文件夹，重新加载主题。请先安装 `Maple Mono NF CN`；主题仅引用字体名称，不内嵌或下载字体。

可以分别改名为 `konayuki-dark-fixed-maple.css` 和 `konayuki-light-fixed-maple.css`，与其他主题并存。替换旧主题前请保留备份。

## 设计与修复

- 深色采用柔灰石墨，浅色采用暖白；大圆角、柔和悬浮与选中背景。
- 基于上游 issue #5 的 Windows 修复，同时适配浅色版本。
- 文件树、文件列表和大纲左对齐，固定缩进与选中几何尺寸，移除选中竖线。
- 搜索框、弹窗按钮统一圆角及文字对比；侧栏滚动条在悬浮或键盘焦点进入时显示。
- 固定任务复选框位置，统一代码块与图表容器样式。
- 普通引用使用留白与引号；提示框保留语义色和圆角底板；行内代码使用低饱和绿色。
- 高亮参考官方 Rider Dark/Light：关键字蓝、字符串棕橙、数字粉、注释绿、明确类型紫、属性青、普通变量中性灰。Python 内置标识符和明确 callee 类别使用方法绿。
- Mermaid D：雾蓝节点、灰绿数据库、暖杏判断节点、加深分组背景和柔和连线；补充类图、甘特图、旅程图、饼图样式。
- Mermaid 兼容编辑器和导出时的 mermaid-svg 结构，打印使用暖白色板。
- PDF 目录取消多级文字透明度，保留字号与缩进。

## 验证与限制

这是纯 CSS 主题，不修改输入、撤销逻辑或文档内容，不需要额外插件。CodeMirror 词法分类不能完整复刻 Rider 语义识别；普通属性与方法可能使用相同类别。滚动条不是停止滚动后计时隐藏。

Mermaid 保留源图形状与布局。异常节点可显式使用 `class nodeId error`；主题不根据文字推测语义。不同 Mermaid 版本、图形类型和文档自定义样式可能产生差异。

已检查深浅色 CSS 计算样式、圆角、打印模式及饼图图例对应关系。用户已确认当前 Mermaid 外观及 PDF 导出修复。未宣称所有图形、平台和导出格式均验证通过，也未确认所有 PDF 查看器下的目录缩放模糊均已解决。

## 来源

- 原主题：https://github.com/aerandirsf/Konayuki
- Windows 修复：https://github.com/aerandirsf/Konayuki/issues/5
- Rider 色板：https://github.com/JetBrains/rider-theme-pack/tree/master/src/main/resources/colorSchemes

保留原项目许可证与署名。实验插件、任务日志和本机备份不属于发布内容。
