# 自发货下单智能体 GitHub Pages 版

这是一个纯静态网页版本，可以放到 GitHub Pages 上运行。订单表和下单模板都只在浏览器本地读取、生成，不上传到服务器。

## 使用方法

1. 打开网页。
2. 选择当天的 dewell、3soil、Shein、越山丘订单文件，哪些有就选哪些。
3. 如果有 Shopify 手动订单，把订单信息粘贴到 Shopify 输入框。
4. 选择 `自发货下单模板.xlsx`。
5. 点击生成，下单表会直接下载到浏览器。

## 发布到 GitHub Pages

1. 在 GitHub 新建一个公开仓库，比如 `order-agent`。
2. 上传本文件夹里的全部文件：`index.html`、`.nojekyll`、`vendor/exceljs.min.js`。
3. 打开仓库的 `Settings` -> `Pages`。
4. `Build and deployment` 选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/root`，保存。
6. 等待一两分钟，GitHub 会给出网址，类似：
   `https://你的用户名.github.io/order-agent/`

## 已包含规则

- dewell、3soil、Shein、越山丘和 Shopify 手动订单。
- 组合 SKU 自动拆成多行。
- 不同店铺之间自动空一行并标注店铺。
- 只有上一行和当前行的 `收件人地址1`、`收件人地址2` 都相同时，才套用相同地址的简化规则。
