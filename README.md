## 一、简介

- 选色器 `colorpicker.js` 源码，支持取得 `hex`、`rgb` 色值。

- [效果查看](https://blog.csdn.net/zz00008888/article/details/136261939)

# 二、使用方法

- 导入

  ```js
  <script src="./colorpicker.js"></script>
  ```

- `html` 中将个一个 `div` 作为容器 `id` 设置为 `color-picker`

  ```html
  <div id="color-picker"></div>
  ```

- `js` 调用插件

  ```js
  Colorpicker.create({
    // 容器标签
    el: "color-picker",
    // 默认颜色
    color: "#000fff",
    // 颜色切换
    change: function (el, hex, rgb) {
      // 修改容器标签颜色，如果需要透明度可以自行调整
      el.style.backgroundColor = hex;
      // el.style.backgroundColor = `rgba(${rgb.r}, ${rgb.g}, ${rgb.b}, ${rgb.a})`;
      console.log(elem, hex, rgb);
    },
  });
  ```

  或

  ```js
  new Colorpicker({
    // 容器标签
    el: "color-picker",
    // 默认颜色
    color: "#000fff",
    // 颜色切换
    change: function (el, hex, rgb) {
      // 修改容器标签颜色，如果需要透明度可以自行调整
      el.style.backgroundColor = hex;
      // el.style.backgroundColor = `rgba(${rgb.r}, ${rgb.g}, ${rgb.b}, ${rgb.a})`;
      console.log(el, hex, rgb);
    },
  });
  ```
