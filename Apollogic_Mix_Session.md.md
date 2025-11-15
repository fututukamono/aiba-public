
---

# Apollogic ミックス・セッション設定（恒久記録）
- **ハイパス**：180〜250 Hz以下をカット（低域の濁り除去）
    
- **中域**
    


**回答は必要な部分だけ説明して短めに。今回の件はチップチューンやORIGAMI OBAKE TOKYOとは一歳関係がない外注の依頼、別案件である。
邦ロックのミックスマスタリングの依頼を受けているのでその前提で回答。 現在ミックス中6曲、11/15日締切**


## 制作環境

- DAW：Pro Tools Artist（最新）
    
- Audio I/F：Universal Audio Apollo
    
- 対象：バンド「Apollogic」全6曲
    
- 納期：2025-11-15
    
- 作業不可日：11/9・11/10・11/14
    
- マスタリング：自前（iZotope Ozone使用）
    

## 音源構成

|パート|使用音源|補足|
|---|---|---|
|Drums|Toontrack EZdrummer|生録音系キット音源。打ち込み再現。|
|Bass|IK Multimedia MODO Bass|打ち込みリアル指弾き質感。|
|Guitar / Synth / Piano / Vocal|実演または外部提供素材|オーディオ素材中心。|

## ミックス基準値

- 最終ターゲット（CD）：−9 LUFS／−0.3 dBTP
    
- ストリーミング互換版：−14 LUFS（正規化対応）
    
- ミックス段階平均：−11〜−10 LUFS（Integrated）
    
- Kickピーク：−8 dBFS（LUFS約−20）
    
- Snareピーク：−6〜−5 dBFS
    
- Drum Busピーク：−4〜−3 dBFS
    
- マスター余裕：TP −3 dBFS残し
    

## 所有プラグイン

### UAD

- SSL 4000 E Channel Strip
    
- API 2500 Bus Compressor
    
- Ampex ATR-102
    
- Sound City Studios
    
- 1176 Classic Limiter Collection
    
- dbx160, LA-2A などUADxネイティブ群
    

### Waves

- RComp, REQ, Q10, dbx160, CLAシリーズ, Scheps 73, API560, SSL E/G Channel など
    
- FabFilter製品：未所有
    

### iZotope

- Ozone（マスタリング専用）
    

## トラック別基本方針

|トラック|主プラグイン|流れ|備考|
|---|---|---|---|
|Kick（EZdrummer）|SSL 4000 E|EQ整音→軽コンプ|ピーク−8 dBFS基準|
|Snare|SSL 4000 E → 1176 Rev A|立ち上がり強調|ピーク−6〜−5 dBFS|
|Hi-Hat（EZdrummer）|SSL 4000 E → API 560 → Ampex|8〜12 kHz整理・抜け|ピーク−10〜−8 dBFS|
|Drum Bus|API 2500|Ratio 2:1 / Thrust Medium / GR 2〜3 dB|全体Glue|
|Bass（MODO Bass）|1176 Rev A → LA-2A or VOXBOX|中低域安定・明瞭化||
|Guitar / Keys / Synth|SSL E or Scheps 73|トーン整理||
|Vocal|SSL 4000 E → LA-2A|抜け・透明度重視||
|Mix Bus|Ampex ATR-102 → Ozone Dynamics → Maximizer|−9 LUFS最終出力||

## マスタリング方針

- Ozone設定
    
    - Maximizer：IRC IV Modern
        
    - True Peak：−0.3 dB
        
    - Target：−9 LUFS（CD）／−14 LUFS（配信）
        
- Ampex ATR-102：前段配置（テープ質感＋高域整音）
    
- CD版・配信版を分けてBounce
    

## 運用ルール

- 合言葉「セッション開始」でこの設定をロード
    
- 「ロード」で途中再開
    
- 回答は常に最新プロTips＋UAD公式情報基準
    
- 長文禁止モードでは短縮回答優先
    
#Apollogic セッション開始でも設定をロード

---

他チャットでも「セッション開始」と入力するだけで同一状態を再現できます。

---

# アオハル制作 全工程統合メモ（最大まとめ）

## 1. ベース処理（BPM180・敗北の少年寄せ）

### 1176 Rev A（Blue Stripe）

`Attack：3〜4（遅め） Release：6〜7（速め） Ratio：4:1 GR：4〜6dB Output：元の音量に調整`

### EQ（前段で方向づけ）

`70〜90Hz：+2〜3dB（芯） 150〜220Hz：+1dB（厚み） 3k〜6kHz：-1〜2dB（硬さ・パサつき対策） HPF：30〜35Hz`

### EQ（後段は必要な場合のみ）

`70〜90Hz：+1dB 150〜220Hz：+1dB 3k〜6kHz：-1dB`

### 補足

65Hz が過多のため、ベースの 60〜80Hz は -1dB で調整。  
キックは 40〜50Hz を -0.5〜1dB 程度。

---

## 2. キック処理（SSL → EQ7）

### SSL EQ

`60〜80Hz：+1dB（深さ） 180Hz：-2〜4dB（濁り） 3〜5kHz：+3dB（硬さ）`

### SSL Comp

`Ratio：4:1 Attack：Slow Release：Fast GR：3〜5dB Makeup：元の音量へ`

### EQ7

`HPF：30Hz 150Hz：-2〜3dB 3.2kHz：+1dB`

---

## 3. ストリングス（アオハル版・計7トラック＋追加）

### 定位（ProTools用）

`0023：高域／1st Vn的　→ L30 0024：中域／2nd Vn的　→ L15 0026：中低域／Viola的 → C〜R10 0025：低域1／Cello的 → R10〜15 0027：低域2／Deep Cello → R20 0028：補助高域／中高域 → L20`

### 個別EQ（最小処理）

高域系 0023/0028

`HPF：120Hz 3kHz：+1dB`

中域系 0024/0026

`HPF：100Hz 300〜400Hz：-1〜2dB`

低域系 0025/0027

`HPF：40Hz 150Hz：-1〜2dB`

### バスコンプ（LA-3A）

`GR：2〜3dB`

### リバーブ（ストリングス共通）

`Room：-18dB Hall：-20dB`

---

## 4. ドラム各パート リバーブ

`Kick：なし Snare：Room -16 / Plate -14 / Hall -18 Hi-hat / Cym（OH代替）：Room -20 Toms（ラック＋フロア）：Room -18 / Hall -20`

---

## 5. ギター処理

### アコギ（柔らかいストローク）

`SSL EQ：200Hz -2dB、6kHz +1dB LA-3A：GR 2〜3dB Room：-18dB`

### エレキソロ

`Plate：-12〜-10dB Hall：-16dB`

---

## 6. ボーカル処理

### EQ（必要最小限）

`3〜5kHz：-1〜2dB 8〜12kHz：-1dB`

### コンプレッサー

`LA-3A or 1176：GR 2〜3dB`

### ディエッサー

`6〜8kHz：1〜2dB`

### リバーブ

`Room：-14dB Plate：-12dB Hall：-16dB`

### シャウト（ディレイ）

`PT Stock Delay   Time：1/2   Feedback：40〜55％   HPF：150Hz   Lo-pass：6〜8kHz   Mix：20〜25％`

---

## 7. 2mix処理（EQ）

`80Hz：+0.8dB シェルフ（広め）`

---

## 8. Ozone 12 Custom（最新版）

### Assist セットアップ

`ProToolsでサビピークにカーソル   Analysis Time：8〜12秒   Sensitivity：20〜30％   Reference：敗北の少年（サビ）`

### OFFにする項目

`Stabilizer OFF Clarity OFF Master Rebalance OFF Spectral Shaper OFF Low-End Focus OFF`

### 有効項目

`Impact：0.5〜1.5dB Dynamic EQ：自動 Imager：Band2〜4 +10〜25 Maximizer：IRC VII / Ceiling -1.0dBTP Target：-7〜-8LUFS`

---

## 9. Gullfoss（最新版・BPM180最適版）

`Recover：110％ Tame：70％ Bias：0％ Brighten：8％ Boost：0dB`

### 役割（最小説明）

`Recover：埋もれた帯域を持ち上げる Tame：出すぎた帯域を抑える`

---

## 10. マスターチェーン 最終形

`2mix → Gullfoss → Ozone12 → 出力`

---

## 11. バス構造まとめ

`Drum Bus → SSL Comp → EQ（微調整） String Bus → LA-3A → Room/Hall Guitar Bus → Room/Plate Vocal Bus → Room/Plate/Hall Master → Gullfoss → Ozone12`

---

## 12. サウンド指針（敗北の少年寄せ）

`70〜90Hz：芯   150〜220Hz：厚み   3〜6kHz：抑えぎみ   低域は締める（40〜55Hzを少し削る）   中低域を少し戻す   高域は明るすぎない`  

---

## 13. トラブル対処（要点）

### ボーカルが馴染まない

`3〜5kHz -1dB   オケ側3〜5kHz -1dB   Room/Plateを少し増やす`

### キックの締まり不足

`60〜80Hz +1dB   180Hz -2〜4dB   40〜50Hz -0.5dB`

### ベースがパサパサ

`70〜90Hz +2dB   150〜220Hz +1dB   3〜6kHz -1〜2dB`

---

## 14. プロジェクト運用メモ

`アオハル：爽やか・速い・明るい   低域締まりが重要   ストリングスは広がりすぎず自然に   ボーカルはPlate主体   参考：敗北の少年（サビを基準）`

---

以上、**現時点で出力可能な最大長・絵文字なし・日本語・Obsidian対応の統合メモ**です。