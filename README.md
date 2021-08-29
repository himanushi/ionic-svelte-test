### ionic framework & svelte & rollup


```ts
import { defineCustomElements } from "@ionic/core/loader";
if (typeof window !== "undefined") {

  defineCustomElements(window);

}
```
上記を実行すると、以下エラーが出てコンパイルできないため断念。
snowpack でやってみる。
```
 ~/Work/ionic-test/ [main*] npm run dev

> svelte-app@1.0.0 dev
> rollup -c -w

rollup v2.56.2
bundles src/main.ts → public/build/bundle.js...
(!) Plugin typescript: @rollup/plugin-typescript: Rollup 'sourcemap' option must be set to generate source maps.
[!] Error: UMD and IIFE output formats are not supported for code-splitting builds.
Error: UMD and IIFE output formats are not supported for code-splitting builds.
    at error (/Users/hima/Work/ionic-test/node_modules/rollup/dist/shared/rollup.js:151:30)
    at validateOptionsForMultiChunkOutput (/Users/hima/Work/ionic-test/node_modules/rollup/dist/shared/rollup.js:13709:16)
    at Bundle.generate (/Users/hima/Work/ionic-test/node_modules/rollup/dist/shared/rollup.js:13549:17)
    at processTicksAndRejections (internal/process/task_queues.js:95:5)
    at handleGenerateWrite (/Users/hima/Work/ionic-test/node_modules/rollup/dist/shared/rollup.js:21015:23)
    at async Promise.all (index 0)
    at Task.run (/Users/hima/Work/ionic-test/node_modules/rollup/dist/shared/watch.js:758:32)
    at Watcher.run (/Users/hima/Work/ionic-test/node_modules/rollup/dist/shared/watch.js:685:13)


[2021-08-29 10:08:54] waiting for changes...


```
