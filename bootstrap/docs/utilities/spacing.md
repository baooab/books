## 间距

设置 `margin` 和 `padding` 值，从 `.25rem` 到 `3rem`。

一、写法

```
.mr-2
.mb-md-0
.p-3
```

二、语法

- `xs` 断点下：`{property}{sides}-{size}`。
- `sm`、`md`、`lg` 和 `xl` 断点下：`{property}{sides}-{breakpoint}-{size}`。

三、取值

`property` 取下列值之一：

- `m`: 表示外边距 `margin`。
- `p`: 表示内边距 `padding`。

`sides` 取下列值之一：

- `t`: 设置 `margin-top` 或者 `padding-top`。
- `b`: 设置 `margin-bottom` 或者 `padding-bottom`。
- `l`: 设置 `margin-left` 或者 `padding-left`。
- `r`: 设置 `margin-right` 或者 `padding-right`。
- `x`: 同时设置 `*-left` 和 `*-right`。
- `y`: 同时设置 `*-top` 和 `*-bottom`。
- 无值：同时设置 `*-left`、`*-right`、`*-top` 和 `*-bottom` 四个方向的值。

`size` 取下列值之一：

- `0`: `margin` 或 `padding` 设置为 `0`.
- `1`: `margin` 或 `padding` 设置为 `$spacer * .25`.
- `2`: `margin` 或 `padding` 设置为 `$spacer * .5`.
- `3`: `margin` 或 `padding` 设置为 `$spacer`.
- `4`: `margin` 或 `padding` 设置为 `$spacer * 1.5`.
- `5`: `margin` 或 `padding` 设置为 `$spacer * 3`.
- `auto`: `margin` 或 `padding` 设置为 `auto`.

`$spacer` 默认是 `1rem`。
