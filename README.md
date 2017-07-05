# Weex-总结
- Android gif图无法使用（不会动）
- 页面布局按750px标准
- 绑定class只能使用数组形式。即  :class=[]
- 使用v-if控制元素显示与隐藏的bug。Android下v-if控制元素消失可能不会不会消失（可能的原因 使用fix定位，可以参考的解决方案 使用timeout延时处理控制v-if的表达式）;Android与IOS使用v-if显示元素，如果要显示的元素DOM结构太复杂嵌套太多可能会引起严重的性能问题。
- 高度宽度无法使用百分比
- 一些文档中没有说明的样式问题。居中margin:0 auto不可用
- image load事件官方文档demo出错。<image onload='onload'></image>  正确写法<image @load='onload'></image> 如需要参数 @load='onload($event, pa ram1, param2 )'
- weex -v v1.0.5
