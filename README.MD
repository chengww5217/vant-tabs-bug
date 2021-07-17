# vant-tabs-bug

## 问题描述
vant-weapp tabs bug

当在 `van-tabs` 中使用 animated 属性时会因为 `van-tab` 
中 `shouldShow` 属性判断错误导致前一个 tab 页面还能显示在 下一个 tab 页面中。

错误代码：
https://github.com/youzan/vant-weapp/blob/dev/packages/tab/index.ts#L53

`shouldShow` 中应该修改为：`shouldShow: active || !parentData.animated,`

## 运行
1. clone 项目到本地

```bash
git clone https://github.com/chengww5217/vant-tabs-bug.git
```

2. 执行 npm install

```bash
cd vant-tabs-bug
npm install
```

3. 构建微信 npm 
   3.1 使用微信开发者工具打开本项目
   3.2 使用`工具` --> `构建 npm`
   3.2 编译运行即可
