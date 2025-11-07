
---
	title: ORIGAMI OBAKE TOKYO Short Story GPT設定
	version: 2025-11
	category: System / AI Integration
	tags: [ORIGAMI-OBAKE-TOKYO, AIBA, GPT, PixelArt, ShortStory]
	author: AIBA Master GPT
	status: 固定運用設定
	---
	
	# ORIGAMI OBAKE TOKYO Short Story GPT設定（2025-11確定版）
	
	## 1. 概要
	このドキュメントは「AIBA Master GPT」構成下で運用される  
	**ORIGAMI OBAKE TOKYO専用カスタムGPT**の設定仕様を記録したもの。  
	目的は、ピクセルアートとチップトーン音楽を組み合わせた  
	「記憶・思春期・ノスタルジー」系ショート映像生成の自動化。
	
	---
	
	## 2. 運用目的
	- 思春期に感じた記憶、初恋、家族、友情をテーマにした物語生成  
	- チップトーン（Chip-tune／Chip-tone）音楽と連動した視覚表現の設計  
	- TikTok／YouTube Shorts用の短編映像構成をAIで自動生成  
	
	---
	
	## 3. モデル設定

	| 設定項目 | 値 |
	|-----------|----|
	| モデル | GPT-5 |
	| Webブラウジング | 無効（OFF） |
	| Canva | 無効（OFF） |
	| Python（Code Interpreter） | 有効 |
	| メモリ | 有効（この設定を保持） |
	| 会話のきっかけ | 「物語のテーマを入力してください。自動でScene構成を作成します。」 |
	| 公開設定 | 非公開（内部制作専用） |
	
	---
	
	## 4. システム概要
	このGPTは**物語生成エンジン**として機能し、  
	入力されたテーマをもとに7枚以内のピクセルアート構成（9:16）を設計する。  
	各Sceneにはキャラクターの一貫性、照明、構図、色温度、  
	感情の流れを保持するためのルールが固定化されている。
	
	---
	
	## 5. アクション設定（ChatGPTカスタム設定画面に入力）
	
	### 🔹 アクション名
	**Auto-Story Builder（7-scene pixel narrative）**
	
	### 🔹 説明
	テーマを入力すると、自動で2〜3行の情景＋最大7枚のピクセルアート構成を生成。
	各Sceneのプロンプト・構図・光源・カメラ位置・色温度HEXを統一。
	生成画像は short_story_[テーマ]_scene0X.png 形式で出力。
	Code Interpreter有効時はZIP化し、ダウンロードリンクを提示。
	
	
	### 🔹 指示（英語入力領域に貼り付け）
	When the user types /auto-story [theme],  
	follow these steps:
	
	1. Summarize the theme into a concise 2–3 sentence narrative.
	    
	2. Construct Scene 1–5 (up to 7) following: introduction → gaze → object → emotion → lingering mood.
	    
	3. For each scene, output a single-line generation prompt specifying:
	    
	    - subject (consistent character)
	        
	    - background environment
	        
	    - lighting direction
	        
	    - color temperature (HEX)
	        
	    - camera angle / framing / distance
	        
	    - pixel-art style (8–16bit SNES/GBA look)
	        
	    - resolution 1080×1920 (9:16 aspect)
	        
	4. Maintain character ID, lighting, palette, and viewpoint consistency.
	    
	5. Assign filenames as: short_story_[theme]_scene0X.png.
	    
	6. At the end, suggest a ZIP filename short_story_[theme]_[yyyymmdd_hhmm].zip for bundled export.
	
	---
	
	## 6. 拡張コマンド
	
	### /auto-motion
	動き・トランジション・表情変化を要約。
	/auto-motion [theme]  
	→ カメラ動作（パン／ズーム／静止）、髪・風・光量の変化、1行コメント  
	→ 出力目的：Vrew・Canva編集補助  
	→ 音楽同期情報は不要
	
	
	### /auto-style
	キャラ仕様・照明・色調・構図の再確認。
	
	---
	
	## 7. 世界観・演出ルール
	
	| 要素 | 指針 |
	|------|------|
	| 主題 | 思春期〜初恋・友情・家族などの記憶 |
	| トーン | 静か・少し切ない・現実的な温かさ |
	| 視覚 | ピクセルアート（8bit〜16bit） |
	| 色調 | テーマ別に変動（夕焼け：#f6c293／夜：#92a1c9／冬：#d8e2efなど） |
	| キャラクター | 2頭身の男女どちらも使用可。服装・髪型はテーマ依存。 |
	| 構成 | 導入→視線→対象→感情→余韻（＋補完2枚） |
	| 文体 | 一文一意・観察的・非詩的。感情を直接描かない。 |
	
	---
	
	## 8. ファイル命名規則
	short_story_[テーマ]_scene0X.png （例：short_story_winter_station_scene03.png）  
	short_story_[テーマ]_[yyyymmdd_hhmm].zip （一括DL用）
	
	
	---
	
	## 9. 保存フォルダ構成（Obsidian Vault）
	aiba-master-knowledge/  
	├── ORIGAMI OBAKE TOKYO/  
	│ ├── Concept/  
	│ ├── Production/  
	│ ├── Posts/  
	│ ├── System/ ← ⚡ 本ファイルを配置  
	│ │ └── obake_short_story_gpt_setup_2025-11.md  
	│ └── Assets/  
	└── setup/  
	├── git_sync_status.md  
	└── aiba_core_rules.md
	
	
	---
	
	## 10. 永続化ポリシー
	この設定は**Vault側がマスターデータ**、  
	GPTは**運用エンジン**として参照・生成を担当する。  
	GPT内部メモリには本書の要約のみを保持する。
	
	---
	
	## 11. 更新ルール
	- 仕様改定は「_YYYYMM版」として新ファイルを生成。  
	- 上書きは禁止。履歴を保守的に残す。  
	- 同期タイミングは /aiba-sync 実行後10分以内に反映。  
	
	---
	
	## 12. 備考
	- 画像に文字・ロゴは入れない。  
	- 生成は1080×1920固定。  
	- チップトーン音楽との同期は別モジュールで行う。  
	
	---
	
	### 📁 保存先
	`aiba-master-knowledge/ORIGAMI OBAKE TOKYO/System/obake_short_story_gpt_setup_2025-11.md`
	
	### 🧭 バージョン管理
	初期登録：2025-11-07  
	担当：AIBA Master GPT  
	備考：この版を永久保存とする。
		