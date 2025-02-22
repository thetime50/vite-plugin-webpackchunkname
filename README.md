## Features

Use `webpackChunkName` config in vite project as well as `webpack` do.

> ℹ️ **Only support for Vite 2.**

## Install

fork by https://github.com/CaptainLiao/vite-plugin-webpackchunkname
- [ ] 删除nodemodule处理代码 // nodemodule模块无法使用webpackChunkName 会报错
- [x] 添加json文件的的处理

发布  
npm run build  
npm publish --access=public 

Install the package from npm (or yarn, or pnpm).

```bash
npm install --save-dev vite-plugin-webpackchunkname
```

### Basic usage

Add it to `vite.config.ts`

```ts
// vite.config.ts
import { manualChunksPlugin } from 'vite-plugin-webpackchunkname'
// Other dependencies...

export default defineConfig({
  plugins: [
    manualChunksPlugin(),
  ]
})
```

then add `webpackChunkName` comments to the import:
````js
import(/* webpackChunkName: "detail" */ "@/detail/somepage.vue")
````

## License

Copyright [CaptainLiao](https://github.com/CaptainLiao)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License. 
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.