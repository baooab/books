## 自定义

```
$ npm install bootstrap
```

新建文件 `Custom.scss`。

1. 包含所有 Bootstrap 代码。

```scss
// Custom.scss
// Option A: Include all of Bootstrap

@import "node_modules/bootstrap/scss/bootstrap";
```

2. 包含部分 Bootstrap 代码。

```sass
// Custom.scss
// Option B: Include parts of Bootstrap

// Required
@import "node_modules/bootstrap/scss/functions";
@import "node_modules/bootstrap/scss/variables";
@import "node_modules/bootstrap/scss/mixins";

// Optional
@import "node_modules/bootstrap/scss/reboot";
@import "node_modules/bootstrap/scss/type";
@import "node_modules/bootstrap/scss/images";
@import "node_modules/bootstrap/scss/code";
@import "node_modules/bootstrap/scss/grid";
```

下面定制化

```scss
// Custom.scss
// Option A: Include all of Bootstrap

$enable-gradients: true;

@import "node_modules/bootstrap/scss/bootstrap";
```

文档链接：https://getbootstrap.com/docs/4.0/getting-started/theming/#sass-options
