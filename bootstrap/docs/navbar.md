## 导航条

在学习导航条之前要知道的：

1. 导航条使用 `.navbar` 包裹，使用 `.navbar-expand{-sm|-md|-lg|-xl}` 实现导航栏的响应式折叠。比如：`.navbar-expand-md` 表示在 `md` 设备（包括）或以上展开导航栏，在 `md` 设备以下折叠导航栏。
2. 导航条默认占满整个父元素的宽度的，如果要限制宽度的话，需要用到容器类（`.container`）包裹。
3. 使用间距和 flex 工具类控制间距和导航项目的对齐方式。
4. 打印时，导航栏是隐藏的。
5. 如果不是用 `nav.navbar`，而是使用 div 元素表示的，即 `div.navbar`，那么为了设备访问性，需要添加 `role="navigation"` 属性。

```html
<nav class="navbar"></nav>

<!-- 等同于 -->
<div class="navbar" role="navigation"></nav>
```

这是一个简单的例子：

```html
<nav class="navbar navbar-expand-md navbar-light bg-light">
  <div class="container">
    <a href="/" class="navbar-brand">乱炖社区</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="navbar-collapse collapse" id="navbarText" aria-expanded="false">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item">
          <a class="nav-link" href="/features">Features</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/auth/login">Login</a>
        </li>
        <li class="nav-item ml-2">
          <a href="/auth/register">
            <button class="btn" type="button">Start Trial</button>
          </a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

上面的例子里就使用了颜色和间距工具类（`.bg-light`、`ml-2`）。

`.navbar-light` 提供了面包导航的（灰色）图标；点击 `.navbar-toggler`，会展开 `.navbar-collapse`。

`.navbar-collapse` 直接子元素是 `.navbar-nav`，我们给 `.navbar-nav`添加 `ml-auto`，它就能右对齐了。

导航项 `.navbar-item` 也可以是下拉的。

```html
<li class="nav-item dropdown">
  <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Dropdown
  </a>
  <div class="dropdown-menu" aria-labelledby="navbarDropdown">
    <a class="dropdown-item" href="#">Action</a>
    <a class="dropdown-item" href="#">Another action</a>
    <div class="dropdown-divider"></div>
    <a class="dropdown-item" href="#">Something else here</a>
  </div>
</li>
```

`.dropdown-toggle` 的 id 不是必须要写的。

导航项的激活样式 `.active`，可以用在两个地方：`.nav-item` 或者 `.nav-link` 上。

```html
<nav class="navbar navbar-expand-md navbar-light bg-light">
  <div class="container">
    <a href="/" class="navbar-brand">乱炖社区</a>
    <span class="navbar-text">A Laravel Product</span>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="navbar-collapse collapse" id="navbarText" aria-expanded="false">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item">
          <a class="nav-link" href="/features">Features</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/auth/login">Login</a>
        </li>
        <li class="nav-item ml-2">
          <a href="/auth/register">
            <button class="btn" type="button">Start Trial</button>
          </a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

使用 `.row` 实现导航栏效果。

```html
<style>
.bg-faded {
  background-color: #ebebeb !important;
}

.blog-header {
  line-height: 1;
}

.blog-header-logo {
  font-size: 2.25rem;
}

.blog-header-logo:hover {
  text-decoration: none;
}
</style>

<header class="blog-header py-3 bg-faded">
  <div class="container">
    <div class="row flex-nowrap justify-content-between align-items-center">
      <div class="col-4 pt-1">
        <a class="text-muted" href="#">Subscribe</a>
      </div>
      <div class="col-4 text-center">
        <a class="blog-header-logo text-dark" href="#">Large</a>
      </div>
      <div class="col-4 d-flex justify-content-end align-items-center">
        <a class="text-muted" href="#">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="mx-3"><circle cx="10.5" cy="10.5" r="7.5"></circle><line x1="21" y1="21" x2="15.8" y2="15.8"></line></svg>
        </a>
        <a class="btn btn-sm btn-outline-secondary" href="#">Sign up</a>
      </div>
    </div>
  </div>
</header>
```
