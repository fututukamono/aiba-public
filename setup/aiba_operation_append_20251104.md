# AIBA Operation Append 2025-11  
更新日：2025-11

---

## 🔹 追加ルールおよび恒久設定

### 1. 出力ルール補足（git_sync_status.md 追記）
- 「最新情報で確認しました」という文言は出力に含めない。  
- 確認は常時行うが、文面としては非表示。  
- 「結論」という語を本文内で使用しない。  

---

### 2. YouTubeボタン仕様（ui_component_rules.md 新規 or 追記）
#### YouTubeボタン運用
- 文言：**「YouTubeへ」**  
- リンク先：  
  `https://www.youtube.com/@OrigamiObakeTokyo?sub_confirmation=1`  
- 即時登録は不可（YouTubeポリシー上）。  
- 設置箇所：  
  1. New Releases右カラム下（おすすめ動画ブロック内）  
  2. NEWSセクション下（origami-followブロック内）  
- デザイン：控えめな背景グラデーション可。

---

### 3. Neveテーマ + LiteSpeed Cache 不具合対策  
（troubleshoot_ui_behavior.md 新規）

#### モバイルメニューが開かない場合
- 症状：iPhoneでクリック反応はあるがメニュー非表示。  
- 原因：LiteSpeed CacheのJS圧縮／遅延。  
- 対処：
  1. LiteSpeed Cache → ページ最適化 →  
     「JS圧縮（Minify）」「JS結合（Combine）」「JS遅延（Delay Load）」を全てオフ。  
  2. 「ツール → パージ → すべてのキャッシュをパージ」。  
  3. 再読み込み後、メニュー開閉確認。  
- この設定を恒久維持し、再有効化しない。  
- CSS圧縮はオン可。

---

### 4. トップページ構成（page_structure_reference.md 追記）

#### 現行構成（2025-11時点）
1. **chtml1** — ヘッダー強制表示スクリプト  
2. **chtml2** — ページ見出し・HERO・CTA  
3. **chtml2_releases** — New Releases＋YouTube＋説明＋YouTubeへボタン  
4. **NEWS heading**  
5. **ニュースフィールド**  
6. **origami-news-list-style**  
7. **JSON-LD構造化データ**

---

### 5. LiteSpeed Cache 安全設定（litespeed_safe_config.md 新規）

#### 恒久設定（Neve推奨構成）
- JS圧縮：**オフ**  
- JS結合：**オフ**  
- JS遅延：**オフ**  
- CSS圧縮：オン可  
- ページキャッシュ：オン推奨  
- 画像最適化：オン推奨  
- キャッシュ異常時：「ツール → すべてのキャッシュをパージ」  
- 上記設定を恒久化し、再有効化しない。

---

### 6. デバッグ共通手順（debug_checklist.md 新規）

#### UI不具合発生時の確認順序
1. シークレットタブで再現確認。  
2. 固定ページスクリプトを一時停止。  
3. テーマJS読み込み確認（Networkタブで`frontend.js` 200確認）。  
4. pointer-events / z-index 競合を確認。  
5. LiteSpeed Cache の最適化設定を一時停止。  
6. キャッシュ全削除（全パージ）。  
7. 再読み込み後に動作確認。  
8. 恒久対応を反映し、Vaultに記録。  

---

### 備考
- すべての設定は ORIGAMI OBAKE TOKYO トップページ運用を基準に策定。  
- 出力ルールおよびコード出力許可ルールは既存Vault内に統合済み。  
- 本ファイルは 2025-11以降の標準補足運用レイヤーとして扱う。  

---
