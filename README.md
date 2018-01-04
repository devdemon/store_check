The current code is for EE3/EE4. For the EE2 sample, [go here](https://github.com/devdemon/store_check/releases/tag/EE2). 

---

# Store Check Extension

This is an example payment gateway extension for Expresso Store. It adds a new payment
method which can be configured from the Store control panel settings.

By default, it simply extends the existing Omnipay "Manual" payment gateway, which can
be used to process off-line transactions. This allows you to have multiple off-line
payment gateways with different names.

The same package layout can be used to add support for any payment gateway, without
having to modify core Store files. This makes future upgrades of Store much easier.

### addon.setup.php

All ExpressionEngine addons [require this](https://docs.expressionengine.com/latest/development/addon_setup_php_file.html). It provides the name, version, and other metadata for the add-on.

### ext.store_check.php

This is the main extension file. It uses the `store_payment_gateways` hook available in
Store 2.1+ to register a new payment gateway.

### Omnipay folder

This is where the gateway lives. It follows the standard conventions and layout of an
Omnipay payment gateway.

For further information about developing Omnipay-compatible payment gateways,
please see the [Omnipay project](https://github.com/omnipay/omnipay).

### License

This gateway is distributed under the terms of the [MIT license](https://github.com/devdemon/store_check/blob/master/LICENSE).
