# 📦 Coffee Stock（RCS 在庫管理）

立命館珈琲研究会（RCS）の在庫管理アプリです。スマホで在庫を増減でき、不足時は Discord に通知します。

## ✨ 機能
- ＋／－ボタンでの在庫入力（スマホ向け）
- お気に入り・最近使った項目の上部表示
- ひらがな／カタカナ区別なしの検索
- 複数項目の一括保存
- Discord 通知
- 変更履歴の表示と CSV 出力（直近30件）

## 🛠 構成
- HTML / CSS / Vanilla JavaScript
- Supabase（データベース）
- GitHub Pages（公開）
- Discord 通知（Cloudflare Workers 経由）

## ⚙️ 設定
`js/config.js` に Supabase の URL と公開キー、Discord 中継先、アクセスコードを設定します。
- `service_role` キーは書かないでください。
- このリポジトリは公開されているため、設定値は外部から見えるものとして扱ってください。
- Supabase で **RLS を必ず有効にしてください**。

## 🗄 テーブル
- `inventory`：id, category, item_name, current_stock, min_stock, unit
- `inventory_logs`：id, created_at, item_name, before_qty, after_qty, diff_qty, note

## 🔧 引き継ぎ
- 無料プランの Supabase は7日間アクセスがないと一時停止します。
- Supabase のアカウントはサークル用アカウントで管理しています。
- テスト時は Discord 通知をオフにしてください。

## 👤 Author
Hyeonsik Kim（ヒョンシク）
