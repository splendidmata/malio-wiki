# 开始使用
在 `.config.php` 里，把 `$_ENV['payment_system']` 的值设置为 `malio`

然后你就可以在 `.malio_config.php` 里分别设置支付宝、微信支付所用的支付系统

# 番茄云支付
如果你使用番茄云支付的话，需要到番茄的后台设置 notify url (通知地址) 为 `https://你的网站/payment/notify/tomatopay`