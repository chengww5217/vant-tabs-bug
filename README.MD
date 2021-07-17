# vant-tabs-bug

## 问题描述
vant-weapp tabs bug

当在 `van-tabs` 中使用 animated 属性时会因为 `van-tab` 
中 `shouldShow` 属性判断错误导致前一个 tab 页面还能显示在 下一个 tab 页面中。

错误代码：
https://github.com/youzan/vant-weapp/blob/dev/packages/tab/index.ts#L53

`shouldShow` 中应该修改为：`shouldShow: active || !parentData.animated,`

