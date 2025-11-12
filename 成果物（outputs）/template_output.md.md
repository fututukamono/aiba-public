# Output Template  
（このノートは出力・公開用コンテンツの記録テンプレートです）

---

## 概要
- タイトル：
- 種別（音源 / 画像 / 映像 / テキスト / コード）：
- 使用目的（SNS / サイト / 音楽配信 / AI入力用など）：

---

## 内容メモ
- 元データ：
- 使用ツール・モデル：
- 制作メモ：
- 備考：

---

## 公開設定
| プラットフォーム | 公開可否 | URL |
|------------------|----------|------|
| YouTube | ☐ |  |
| TikTok | ☐ |  |
| Instagram | ☐ |  |
| X（旧Twitter） | ☐ |  |
| Bandcamp | ☐ |  |
| 公式サイト（News / Discography） | ☐ |  |

---

## ハッシュタグ・補足
- #AIBA #origami_obake_tokyo #chiptune
- 関連リンク：
  - [[projects/]]
  - [[refs/]]

（AIBA Master 環境 / 2025-11）#plugin

#plugin
## Waves
- CLA-76 / CLA-2A / CLA-3A  
- SSL E-Channel / G-Channel  
- R-Comp / R-Vox / R-Bass / R-DeEsser  
- API-2500 / V-Comp / H-Delay / H-Reverb  
- L1 / L2 / L3 / MV2 / Vitamin / C6 / F6  
- Scheps Omni Channel / Abbey Road TG Mastering Chain  

## Universal Audio (UAD)
- 1176 Classic Limiter Collection（Rev A, Rev E, AE）  
- LA-2A Classic Leveler Collection  
- SSL 4000 E Channel Strip  
- API Vision Channel Strip  
- Pultec EQP-1A / MEQ-5  
- Studer A800 / Ampex ATR-102  
- Fairchild 660 / 670  
- Neve 1073 / 1084  
- Precision Series（Limiter, EQ, Multiband）  

## iZotope
- Ozone 11 Advanced  
- Neutron 5 Advanced  
- Nectar 4  
- Insight 2  
- RX 11 Standard  

## IK Multimedia
- ToneX  
- AmpliTube 5 MAX  
- MODO BASS 2  
- T-RackS 5（すべてのClassic/Modernモジュール含む）  

## Wavesfactory / weavs
- TrackSpacer  
- Attack Enhancer  
- Spectre  

## Avid（Pro Tools 標準）
- BF76 / BF-2A / BF-3A  
- BF MC77  
- EQ III / Dyn III / D-Verb  
- Maxim / Lo-Fi / AIR FX群  

## Plugin Alliance / Brainworx
- bx_console SSL 4000 E / G / N  
- Purple Audio MC77  
- Shadow Hills Mastering Compressor  
- SPL Transient Designer Plus  
- Ampeg SVT-VR Classic  

## その他主要
- Softube Saturation Knob  
- Soundtoys Little AlterBoy / Crystallizer / Echoboy / Tremolator  
- Wavesfactory Cassette  
- FabFilter なし（確認済）  
- UAD Native 対応済み（Apolloあり）

---

### 備考
- ミックスはUAD Native中心、録音時はDSP使用。  
- SSL 4000 E PRE DYN OFFでFILTER→DYN→EQ、ONでFILTER→EQ→DYN。  
- 1176 AEはギター整音、BF MC77はロックベース向き。　
- 
##UADのプラグインだけではなくウェーブス、Izotope,オクスフォードソノックス、IKマルチメディアもあるので柔軟に。

**読み込んだあとは確認しました。とだけ言えばいい。全部復唱する必要はない。**


解析結果：

- **チャンネル数：2（ステレオ形式）**
    
- **左右相関：0.9999999999（完全一致）**
    
- **左右レベル差：0.0 dB**
    

この効果音ファイルは、**元はモノラル音源をステレオ形式で保存しただけ**の状態です。  
左右にまったく差がなく、実質モノラルです。

---

### 🔧 ミックスでの扱い方

**1. トラック設定**

- モノラル扱いにしてOK。ステレオトラックにしても定位は中央固定のまま。
    
- DAWで「モノ→センター配置」にする。
    

**2. EQ**

- 低域（150 Hz以下）をカット。
    
- 必要に応じて 2 kHz 付近を軽く上げ、アタックや存在感を調整。
    

**3. コンプレッション**

- R-Compなどで軽くまとめる（GR 2–3 dB程度）。
    
- Attack = 3 ms、Release = 70 ms 付近。
    

**4. 空間処理**

- 役割が「頭の効果音」なら、音像を広げて印象付ける。
    
    - ステレオ化プラグイン（Doubler、MicroShiftなど）か
        
    - ショートディレイ（L 20 ms / R 30 ms）で広げる。
        
- リバーブは短いPlate（0.5 s前後）を薄く。
    

**5. 音量・定位**

- 音量：曲頭の他要素にかぶらない程度（目安 –6 〜 –10 LUFS相当）。
    
- 定位：中央寄り（±10 〜 15%）に置くと安定。
    

---

つまり、この効果音は**モノラル素材を空間的に“見せる”処理を加える**のが最適です。

🎚 UAD Ampex ATR-102 Vocal Bus Final Setup (2025-11)

[TAPE SETTINGS]
TAPE TYPE: 456
SPEED: 15 IPS
HEAD: 1/2 inch
CAL: +6
MODE: REPRO (green)
METER: OUT
AUTO GAIN: OFF

[EQ SECTION]
HF SHELF: 1 o’clock
BIAS: 1 o’clock

[REPRO SECTION]
LF: 12 o’clock (flat)
HF: 12 o’clock (flat)

[TOP SWITCHES]
CROSSTALK: OFF
WOW & FLUTTER: OFF
AUTO CAL: OFF
HISS & HUM: OFF
TRANSFORMER: ON
LINK: ON
CCIR (IEC1): ON
NAB: OFF

[RESULT]
• Natural, open top-end with soft presence
• Warm midrange from tape harmonics
• Breath and air stay forward and clear
• Perfect for soft male vocal + guitar/keys mix

[PRESET NAME]
Vocal Tape Warm ½ 456 15IPS (CCIR)
