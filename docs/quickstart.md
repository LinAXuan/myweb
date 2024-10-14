# 诗歌

以下是代码
```bash
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>古代诗歌五首</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div class="header">
            <span class="poetry-title">古代诗歌<img src="shige.png" alt=""></span>
            <hr>
        </div>
        <h1>古代诗歌五首</h1>
        <ul>
            <li><span class="title">《竹里馆》</span> <span class="text">独坐幽篁里，</span><span class="special-text">弹琴复长啸</span>。<span class="text">深林人不知，明月来相照。</span></li>
            <li><span class="title">《春夜洛城闻笛》</span> <span class="text">谁家玉笛暗飞声，</span><span class="special-text">散入春风满洛城</span>。<span class="text">此夜曲中闻折柳，何人不起故园情。</span></li>
            <li><span class="title">《逢入京使》</span> <span class="text">故园东望路漫漫，双袖龙钟泪不干。马上相逢无纸笔，凭君传语报平安。</span></li>
            <li><span class="title">《晚春》</span> <span class="text">草树知春不久归，百般红紫斗芳菲。杨花榆荚无才思，惟解漫天作雪飞。</span></li>
            <li><span class="title">《登飞来峰》</span> <span class="text">飞来山上千寻塔，闻说鸡鸣见日升。不畏浮云遮望眼，自缘身在最高层。</span></li>
        </ul>
    </div>
</body>
</html>
```
最终效果

<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>古代诗歌五首</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <div class="header">
            <span class="poetry-title">古代诗歌<img src="images/shige.png" alt=""></span>
            <hr>
        </div>
        <h1>古代诗歌五首</h1>
        <ul>
            <li><span class="title">《竹里馆》</span> <span class="text">独坐幽篁里，</span><span class="special-text">弹琴复长啸</span>。<span class="text">深林人不知，明月来相照。</span></li>
            <li><span class="title">《春夜洛城闻笛》</span> <span class="text">谁家玉笛暗飞声，</span><span class="special-text">散入春风满洛城</span>。<span class="text">此夜曲中闻折柳，何人不起故园情。</span></li>
            <li><span class="title">《逢入京使》</span> <span class="text">故园东望路漫漫，双袖龙钟泪不干。马上相逢无纸笔，凭君传语报平安。</span></li>
            <li><span class="title">《晚春》</span> <span class="text">草树知春不久归，百般红紫斗芳菲。杨花榆荚无才思，惟解漫天作雪飞。</span></li>
            <li><span class="title">《登飞来峰》</span> <span class="text">飞来山上千寻塔，闻说鸡鸣见日升。不畏浮云遮望眼，自缘身在最高层。</span></li>
        </ul>
    </div>
</body>
</html>


## Initialize

If you want to write the documentation in the `./docs` subdirectory, you can use the `init` command.

```bash
docsify init ./docs
```

## Writing content

After the `init` is complete, you can see the file list in the `./docs` subdirectory.

- `index.html` as the entry file
- `README.md` as the home page
- `.nojekyll` prevents GitHub Pages from ignoring files that begin with an underscore

You can easily update the documentation in `./docs/README.md`, of course you can add [more pages](more-pages.md).

## Preview your site

Run the local server with `docsify serve`. You can preview your site in your browser on `http://localhost:3000`.

```bash
docsify serve docs
```

?> For more use cases of `docsify-cli`, head over to the [docsify-cli documentation](https://github.com/docsifyjs/docsify-cli).

## Manual initialization

If you don't like `npm` or have trouble installing the tool, you can manually create `index.html`:

```html
<!-- index.html -->

<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <meta charset="UTF-8" />
    <link
      rel="stylesheet"
      href="//cdn.jsdelivr.net/npm/docsify@4/themes/vue.css"
    />
  </head>
  <body>
    <div id="app"></div>
    <script>
      window.$docsify = {
        //...
      };
    </script>
    <script src="//cdn.jsdelivr.net/npm/docsify@4"></script>
  </body>
</html>
```

### Specifying docsify versions

?> Note that in both of the examples below, docsify URLs will need to be manually updated when a new major version of docsify is released (e.g. `v4.x.x` => `v5.x.x`). Check the docsify website periodically to see if a new major version has been released.

Specifying a major version in the URL (`@4`) will allow your site will receive non-breaking enhancements (i.e. "minor" updates) and bug fixes (i.e. "patch" updates) automatically. This is the recommended way to load docsify resources.

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify@4/themes/vue.css" />
<script src="//cdn.jsdelivr.net/npm/docsify@4"></script>
```

If you prefer to lock docsify to a specific version, specify the full version after the `@` symbol in the URL. This is the safest way to ensure your site will look and behave the same way regardless of any changes made to future versions of docsify.

```html
<link
  rel="stylesheet"
  href="//cdn.jsdelivr.net/npm/docsify@4.11.4/themes/vue.css"
/>
<script src="//cdn.jsdelivr.net/npm/docsify@4.11.4"></script>
```

### Manually preview your site

If you have Python installed on your system, you can easily use it to run a static server to preview your site.

```python2
cd docs && python -m SimpleHTTPServer 3000
```

```python3
cd docs && python -m http.server 3000
```

## Loading dialog

If you want, you can show a loading dialog before docsify starts to render your documentation:

```html
<!-- index.html -->

<div id="app">Please wait...</div>
```

You should set the `data-app` attribute if you changed `el`:

```html
<!-- index.html -->

<div data-app id="main">Please wait...</div>

<script>
  window.$docsify = {
    el: '#main',
  };
</script>
```

Compare [el configuration](configuration.md#el).
