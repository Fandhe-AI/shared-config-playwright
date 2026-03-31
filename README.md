# @fandhe-ai/shared-config-playwright

Playwright（E2E テスト）の共有設定。

## エクスポート

| パス | 説明 |
|------|------|
| `@fandhe-ai/shared-config-playwright/base` | `createBaseConfig` ファクトリ関数（CI 対応、リトライ・レポーター設定済み） |

## 使用方法

`playwright.config.ts` で `createBaseConfig` を import して使用する:

```ts
import { createBaseConfig } from "@fandhe-ai/shared-config-playwright/base";

export default createBaseConfig({
  testDir: "./src",
  baseURL: "http://localhost:3000",
});
```

## 開発

### セットアップ

```bash
pnpm install
```

### コミット規約

[Conventional Commits](https://www.conventionalcommits.org/ja/) を採用。
[commitlint](https://commitlint.js.org/) + [lefthook](https://github.com/evilmartians/lefthook) により自動検証。

```
<type>: <description>

# 例
feat: 新しいルールを追加
fix: 設定の不具合を修正
chore: 依存関係を更新
```

## ライセンス

Copyright © Fandhe Inc.
