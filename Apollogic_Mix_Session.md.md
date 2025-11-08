
---

# Apollogic ミックス・セッション設定（恒久記録）

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