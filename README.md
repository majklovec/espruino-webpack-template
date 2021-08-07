# Espruino webpack template

For easier JS module management and es6 usage in Espruino projects

# Install dependencies

`yarn`

# Code

Put yours app in the src. Use `import` to import local modules, `require` for
Espruino modules

## example

```js
import PCF8574 from "./PCF8574";

var i2c = new I2C();
i2c.setup({ sda: 21, scl: 22 });

var PCF = new PCF8574(i2c, { addr: 0x20 });
var BME = require("BME680").connectI2C(i2c, { addr: 0x77 });
```

# Build and minimize JavaScript

`yarn build`

# Build and upload

`yarn upload`
