# Weex-总结
- Android gif图无法使用（不会动）
- 页面布局按750px宽度标准，换算关系：300px宽度的元素在(1920 * 1080)分辨率实际显示宽度为 300px * (1080/750)
- 绑定class只能使用数组形式。即  :class=[]
- 使用v-if控制元素显示与隐藏的bug。Android下v-if控制元素消失可能不会不会消失（可能的原因 使用fix定位，可以参考的解决方案 使用timeout延时处理控制v-if的表达式）;Android与IOS使用v-if显示元素，如果要显示的元素DOM结构太复杂嵌套太多可能会引起严重的性能问题。
- 高度宽度无法使用百分比
- 一些文档中没有说明的样式问题。居中margin:0 auto不可用
- image load事件官方文档demo出错。image onload='onload'  正确写法 image @load='onload' 如需要参数 @load='onload($event, param1, param2 )'
- Android情况下要考虑虚拟键和状态栏对页面布局的影响。如2k分辨率下实际上可显示的高度为2560px减去虚拟键和状态栏的高度（不同机型不一样）
- weex -version v1.0.5
