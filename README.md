# ToDo-List

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Vue CLI
```sh
npm create vue@latest
```

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

<hr/>

### Vue learning
```
 ref() -> đối tượng dùng để khởi tạo giá trị của biến
 vd: const number = ref(0)
 nội suy: giá trị của biến được xác định bằng thuộc tính value
 number.value //-> 0
```

```
directive
@ == v-on:   -> giữ thuộc tính của element
: == v-bind: -> lắng nghe DOM events
```

```
modifier

ví dụ:
<form @submit.prevent="onSubmit">...</form>  -> Modifier này đảm bảo rằng khi sự kiện submit xảy ra, event.preventDefault() sẽ được gọi ngay lập tức, ngăn chặn hành vi mặc định của trình duyệt trong việc reload trang khi form được submit.
<a @click.stop="onClick">Click me</a>        ->  Ngừng sự kiện lan truyền (gọi event.stopPropagation())
```

