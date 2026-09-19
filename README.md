# Orange-Kitchen 橙香厨房无线接单大屏

餐饮点餐系统的**厨房接单端**：通过 MQTT 实时接收点餐端发来的订单，在厨房大屏上滚动展示，并播放提示音，供后厨高效出餐。

## 功能

- 实时接单：通过 MQTT 订阅点餐端订单主题，新订单即时弹出
- 订单卡片展示：菜品、数量、图片清晰呈现
- 新订单动画 + 提示音提醒
- 出餐完成：一键标记订单完成，卡片移除
- 防重验证：相同订单不重复显示

## 技术栈

- HTML / CSS / JavaScript（原生，单文件，无构建）
- MQTT（mqtt.js，WebSocket 连接）

## 如何运行

直接用浏览器打开 `index.html` 即可（需联网，用于连接 MQTT Broker 和加载提示音）。

配合 [orange-order](https://github.com/chengpeixiang279/orange-order) 点餐端一起使用：点餐端下单后，订单会实时出现在厨房大屏上。

## 说明

本项目为纯前端原型，MQTT 使用公共 Broker（broker.emqx.io）演示，生产环境可替换为自己的 Broker。
