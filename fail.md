https://dash.deno.com/projects/blog-sqlite/logs

```
TypeError: Deno.openSync is not a function
    at js_open (https://deno.land/x/sqlite@v3.7.0/build/vfs.js:29:24)
    at <anonymous> (wasm://wasm/00274a8a:1:3702)
    at <anonymous> (wasm://wasm/00274a8a:1:142867)
    at <anonymous> (wasm://wasm/00274a8a:1:138770)
    at <anonymous> (wasm://wasm/00274a8a:1:144940)
    at <anonymous> (wasm://wasm/00274a8a:1:4589)
    at <anonymous> (wasm://wasm/00274a8a:1:594290)
    at https://deno.land/x/sqlite@v3.7.0/src/db.ts:72:67
    at setStr (https://deno.land/x/sqlite@v3.7.0/src/wasm.ts:13:24)
    at new DB (https://deno.land/x/sqlite@v3.7.0/src/db.ts:72:24)
```

請參考 -- https://github.com/denoland/deploy_feedback/issues/136

Deno Deploy 不支援 opensync，所以 fail !

然後有人提出了解決方法，但要修改程式

* https://github.com/ayame113/mock-file/blob/main/example/main.ts

不過比較正統的解決方法，可能是採用雲端資料庫，像是 Supabase 的 Postgresql, FaunaDB, DynamoDB 或 Firebase

* https://deno.com/deploy/docs/tutorial-postgres
 
Supabase 的免費方案額度還不錯

* https://supabase.com/pricing
