# ランディングページ引き継ぎドキュメント

作成日: 2024-12-21

---

## 概要

NeoN VJ アプリのランディングページ（8言語対応）の開発状況と残タスクの引き継ぎ。

---

## プロジェクト情報

| 項目 | 内容 |
|------|------|
| リポジトリ | `/Users/h.h/保存/develop/app/NeoN/neon-website` |
| フレームワーク | Astro |
| 開発サーバー | `npm run dev` → http://localhost:4321 |
| 本番URL | https://neondjneon.com/app/{lang} |

---

## ファイル構成

```
neon-website/
├── src/
│   ├── components/
│   │   └── AppLanding.astro    # メインコンポーネント
│   ├── layouts/
│   │   └── Layout.astro        # 共通レイアウト
│   └── pages/
│       └── app/
│           ├── ja.astro        # 日本語
│           ├── en.astro        # 英語
│           ├── es.astro        # スペイン語
│           ├── fr.astro        # フランス語
│           ├── ko.astro        # 韓国語
│           ├── th.astro        # タイ語
│           ├── zh-Hans.astro   # 簡体字中国語
│           └── zh-Hant.astro   # 繁体字中国語
└── public/
    └── images/
        └── app/
            ├── neon-vj-icon.png      # アプリアイコン
            ├── neon-vj-ogp.png       # OGP画像
            └── screenshot-*.png      # スクリーンショット
```

---

## 検証環境URL

| 言語 | URL |
|------|-----|
| 日本語 | http://localhost:4321/app/ja |
| 英語 | http://localhost:4321/app/en |
| スペイン語 | http://localhost:4321/app/es |
| フランス語 | http://localhost:4321/app/fr |
| 韓国語 | http://localhost:4321/app/ko |
| タイ語 | http://localhost:4321/app/th |
| 簡体字中国語 | http://localhost:4321/app/zh-Hans |
| 繁体字中国語 | http://localhost:4321/app/zh-Hant |

---

## 完了項目

- [x] 8言語のページ作成
- [x] AppLanding.astro コンポーネント作成
- [x] アプリアイコン設置
- [x] 言語切り替え機能
- [x] 機能紹介セクション（4項目）
- [x] 利用シーンセクション（4項目）
- [x] システム要件セクション
- [x] リンクセクション（ユーザーガイド、プライバシーポリシー、利用規約、サポート）
- [x] Shazam技術使用の注記

---

## 残タスク

### 優先度：高

| タスク | 詳細 | 備考 |
|--------|------|------|
| App Storeバッジのリンク設定 | Coming Soonを実際のストアURLに変更 | リリース後に対応 |
| 価格の最終決定 | 各言語の価格表記確認 | 現在: ¥4,900の30%OFF |

### 優先度：中

| タスク | 詳細 | 備考 |
|--------|------|------|
| スクリーンショットセクション | 現在1枚のプレースホルダー | 複数枚のカルーセル化検討 |
| OGP画像の確認 | SNSシェア時の表示確認 | `/images/app/neon-vj-ogp.png` |

### 優先度：低

| タスク | 詳細 | 備考 |
|--------|------|------|
| アニメーション調整 | フェードインのタイミング等 | 任意 |

---

## 価格設定（現在）

| 言語 | 価格表記 |
|------|----------|
| ja | ¥4,900（リリース記念：30%OFF） |
| en | $29.99 (Launch offer: 30% off) |
| es | €29.99 (Oferta de lanzamiento: 30% de descuento) |
| fr | 29,99€ (Offre de lancement : -30%) |
| ko | ₩39,000 (출시 기념: 30% 할인) |
| th | ฿990 (โปรโมชั่นเปิดตัว: ลด 30%) |
| zh-Hans | 198元（上线优惠：7折） |
| zh-Hant | NT$990（上市優惠：7折） |

---

## 外部リンク先

すべて neondjneon.com を参照（本番環境では動作予定）:

| リンク | URL |
|--------|-----|
| ユーザーガイド | /manual-{lang}.html |
| プライバシーポリシー | /privacy-policy-{lang}.html |
| 利用規約 | /terms-{lang}.html |
| サポート | mailto:neondjneon@gmail.com |

---

## デプロイ手順

1. 最終確認後、neon-website リポジトリをコミット
2. neon-vj-privacy リポジトリと同時にプッシュ（リンク先を先に公開）
3. Vercel/Netlify等でデプロイ（設定による）

---

## 注意事項

- ローカル開発サーバーでは外部リンク（プライバシーポリシー等）は404になる（想定内）
- 本番環境では neondjneon.com にすべてのファイルが配置される前提
- Apple申請直前に全リソースを同時公開予定

---

## 関連ドキュメント

- リリース計画: `/Users/h.h/Library/Mobile Documents/com~apple~CloudDocs/ipad/app/neonvj/docs/release_plan.md`
- App Store説明文: `/Users/h.h/Library/Mobile Documents/com~apple~CloudDocs/ipad/app/neonvj/ShazamVJ2/APP_STORE_DESCRIPTION.md`

---

## 開発サーバー起動方法

```bash
cd "/Users/h.h/保存/develop/app/NeoN/neon-website"
npm run dev
```

または

```bash
NODE_PATH="/Users/h.h/保存/develop/app/NeoN/neon-website/node_modules" \
/Users/h.h/保存/develop/app/NeoN/neon-website/node_modules/.bin/astro dev \
--root "/Users/h.h/保存/develop/app/NeoN/neon-website"
```

---

## 現在のステータス

**ランディングページ**: 作業中（残タスクあり）

主な残作業:
1. App Storeリンクの設定（リリース後）
2. スクリーンショットの追加・カルーセル化
3. 最終確認後のデプロイ
