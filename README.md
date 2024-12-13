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
		// 默认颜色，固定透明度为 1 ，但不可修改
		// color: "#000fff",
		// 默认颜色，固定透明度为 1 ，但不可修改
		// color: "rgb(0, 255, 0)",
		// 默认颜色，透明度也会生效，但不可修改
		color: "rgba(0, 255, 0, 0.5)",
    // 颜色切换
    change: function (el, hex, rgba) {
      // 修改容器标签颜色，透明度是传入的透明度，不可修改，默认为 1
			el.style.backgroundColor = `rgba(${rgba.r}, ${rgba.g}, ${rgba.b}, ${rgba.a})`;
			// el.style.backgroundColor = hex;
			// console.log(el, hex, rgba);
			console.log(hex, rgba);
    },
  });
  ```
