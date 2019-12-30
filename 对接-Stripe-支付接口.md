目前 Stripe 支持支付宝和微信支付。

在 Stripe 管理平台的侧边栏里找到 开发者 -> API密钥，获取到密钥（格式为sk_xxxxxxxxxxxxxx），填入 `.config.php` 里的 `stripe_key`。

然后打开 开发者 -> Webhook，选择添加端点，端点 URL 写 `https://你的域名/payment/notify` (如果你用的是Malio聚合支付接口要写 `https://你的域名/payment/notify/stripe`)，要发送的事件选择 `source.chargeable`，最后点击添加端点。

然后点击进去看刚刚添加的 Webhook 详情，找到密钥签名（格式为whsec_xxxxxxxxxxxx），填入 `.config.php` 里的 `stripe_webhook_endpoint_secret`。

在 `.malio_config.php` 里可以设置 Stripe 支付接口可充值的最低金额。
