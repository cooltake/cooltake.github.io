---
layout: post
title: "コンプレッサー・リバーブ・ゲートの使い方 - 音楽制作エフェクター入門"
description: "音楽制作で欠かせないコンプレッサー・リバーブ・ゲートの基本的な使い方を解説。各エフェクターの役割とパラメーターを初心者向けにわかりやすく紹介します。"
date: 2026-05-11
image: /assets/images/thumb-effects.jpg
categories: [gear]
tags: [コンプレッサー, リバーブ, ゲート, エフェクター, MIX]
---



## エフェクターとは — 音に「処理」を加えるツール

<figure style="margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><defs><marker id="ah2" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#3b82f6"/></marker></defs><rect x="20" y="68" width="110" height="64" fill="#334155" rx="8"/><text x="75" y="97" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#94a3b8" font-weight="bold">Raw Audio</text><text x="75" y="114" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#64748b">（録音音源）</text><line x1="132" y1="100" x2="156" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah2)"/><rect x="160" y="68" width="120" height="64" fill="#7c3aed" rx="8"/><text x="220" y="97" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">コンプレッサー</text><text x="220" y="114" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#ddd6fe">音量を均一化</text><line x1="282" y1="100" x2="306" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah2)"/><rect x="310" y="68" width="120" height="64" fill="#2563eb" rx="8"/><text x="370" y="97" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">リバーブ</text><text x="370" y="114" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#bfdbfe">空間・残響付加</text><line x1="432" y1="100" x2="456" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah2)"/><rect x="460" y="68" width="120" height="64" fill="#059669" rx="8"/><text x="520" y="97" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">ゲート</text><text x="520" y="114" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#a7f3d0">ノイズ除去</text><line x1="582" y1="100" x2="606" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah2)"/><rect x="610" y="68" width="170" height="64" fill="#0f766e" rx="8"/><text x="695" y="97" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">完成音源</text><text x="695" y="114" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#99f6e4">プロ品質の仕上がり</text></svg></figure>


録音した音をそのまま使うのではなく、より良い音に整えるために使うのが**エフェクター（エフェクトプラグイン）**です。

音楽制作において最もよく使われる3つのエフェクトが「コンプレッサー・リバーブ・ゲート」です。これらの使い方を理解するだけで、録音したサウンドのクオリティが大きく変わります。

---

## コンプレッサー — 音量の「でこぼこ」を平らにする

<figure style="margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 340" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="340" fill="#0f172a" rx="10"/><defs><marker id="arh" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#94a3b8"/></marker></defs><text x="400" y="22" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#f1f5f9" font-weight="bold">コンプレッサー — Threshold / Attack / Release / Ratio</text><text x="400" y="330" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">時間 →</text><text x="18" y="170" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">振幅</text><line x1="70" y1="170" x2="720" y2="170" stroke="#334155" stroke-width="1" stroke-dasharray="3,5"/><text x="60" y="174" text-anchor="end" font-family="sans-serif" font-size="10" fill="#94a3b8">0</text><line x1="70" y1="105" x2="720" y2="105" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="8,4"/><line x1="70" y1="235" x2="720" y2="235" stroke="#f59e0b" stroke-width="1" stroke-dasharray="4,4"/><text x="728" y="109" text-anchor="start" font-family="sans-serif" font-size="10" fill="#f59e0b">Threshold</text><text x="728" y="174" text-anchor="start" font-family="sans-serif" font-size="10" fill="#94a3b8">0 dB</text><polyline points="75,170 90,158 105,180 120,156 135,179 150,159 170,170" stroke="#3b82f6" stroke-width="1.5" fill="none"/><polyline points="170,170 195,52 340,52 365,170 720,170" stroke="#3b82f6" stroke-width="2.5" fill="none"/><polygon points="195,105 195,52 340,52 340,105" fill="#3b82f6" opacity="0.12"/><polyline points="170,170 195,52 225,90 340,90 373,184 400,170 720,170" stroke="#22c55e" stroke-width="2.5" fill="none"/><polygon points="225,105 225,90 340,90 340,105" fill="#22c55e" opacity="0.12"/><polygon points="225,52 340,52 340,90 225,90" fill="#f59e0b" opacity="0.3"/><text x="282" y="76" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#f59e0b" font-weight="bold">Gain Reduction</text><line x1="195" y1="34" x2="225" y2="34" stroke="#ec4899" stroke-width="1.5"/><line x1="195" y1="39" x2="195" y2="29" stroke="#ec4899" stroke-width="1.5"/><line x1="225" y1="39" x2="225" y2="29" stroke="#ec4899" stroke-width="1.5"/><text x="210" y="27" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#ec4899">Attack Time</text><line x1="195" y1="38" x2="195" y2="52" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="225" y1="38" x2="225" y2="90" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="365" y1="34" x2="400" y2="34" stroke="#a855f7" stroke-width="1.5"/><line x1="365" y1="39" x2="365" y2="29" stroke="#a855f7" stroke-width="1.5"/><line x1="400" y1="39" x2="400" y2="29" stroke="#a855f7" stroke-width="1.5"/><text x="382" y="27" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#a855f7">Release Time</text><line x1="365" y1="38" x2="365" y2="170" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><line x1="400" y1="38" x2="400" y2="170" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><line x1="360" y1="52" x2="400" y2="52" stroke="#3b82f6" stroke-width="1.5"/><line x1="360" y1="90" x2="400" y2="90" stroke="#22c55e" stroke-width="1.5"/><line x1="380" y1="52" x2="380" y2="90" stroke="#94a3b8" stroke-width="1" stroke-dasharray="3,3"/><text x="410" y="71" text-anchor="start" font-family="sans-serif" font-size="10" fill="#f1f5f9">Ratio</text><text x="410" y="85" text-anchor="start" font-family="sans-serif" font-size="12" fill="#22c55e" font-weight="bold">4:1</text><line x1="500" y1="268" x2="536" y2="268" stroke="#3b82f6" stroke-width="2.5"/><text x="542" y="272" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Input (原音)</text><line x1="500" y1="286" x2="536" y2="286" stroke="#22c55e" stroke-width="2.5"/><text x="542" y="290" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Output (圧縮後)</text><line x1="500" y1="304" x2="536" y2="304" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="6,3"/><text x="542" y="308" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f59e0b">Threshold</text><rect x="500" y="316" width="36" height="10" fill="#f59e0b" rx="2"/><text x="542" y="325" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f59e0b">Gain Reduction</text></svg></figure>


### コンプレッサーとは

コンプレッサーは**音量の大きい部分を圧縮**して、音量のばらつきを均一にするエフェクトです。

たとえばボーカル録音では、フレーズによって声の強弱が変わります。そのまま使うと「大きすぎる部分」と「小さすぎる部分」が混在して聴きにくくなります。コンプレッサーを使うと、自動的にこのばらつきを整えてくれます。

### 主なパラメーター

| パラメーター | 役割 | 目安 |
|------------|------|------|
| **Threshold（スレッショルド）** | 圧縮が始まる音量レベル | -20〜-10dB |
| **Ratio（レシオ）** | 圧縮の強さ | ボーカル:3:1〜5:1 |
| **Attack（アタック）** | 圧縮が始まるまでの時間 | 20〜50ms |
| **Release（リリース）** | 圧縮が終わるまでの時間 | 80〜200ms |
| **Makeup Gain** | 圧縮で下がった音量を補正 | 圧縮量に合わせて |

### ボーカルへのコンプレッサー設定例

- Threshold：-18dB
- Ratio：4:1
- Attack：30ms（アタック感を残すため速すぎないように）
- Release：100ms
- Makeup Gain：+3〜4dB

---

## リバーブ — 空間・距離感を演出する

<figure style="margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><defs><marker id="ah" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#3b82f6"/></marker></defs><rect x="40" y="68" width="120" height="64" fill="#3b82f6" rx="8"/><text x="100" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">原音 (Dry)</text><line x1="162" y1="100" x2="186" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="190" y="68" width="120" height="64" fill="#6366f1" rx="8"/><text x="250" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">リバーブ</text><text x="250" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">ユニット</text><line x1="312" y1="100" x2="336" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="340" y="68" width="120" height="64" fill="#ec4899" rx="8"/><text x="400" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">残響音生成</text><line x1="462" y1="100" x2="486" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="490" y="68" width="120" height="64" fill="#14b8a6" rx="8"/><text x="550" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">Dry/Wet</text><text x="550" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">ブレンド</text><line x1="612" y1="100" x2="636" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="640" y="68" width="120" height="64" fill="#22c55e" rx="8"/><text x="700" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">出力</text></svg></figure>


### リバーブとは

録音した音に**空間の響き**を加えるエフェクトです。ドライ（響きのない）な録音音源を、まるでスタジオや大ホールで録ったように変換できます。

ボーカルや楽器に適度なリバーブを加えることで、音に「奥行き」と「自然さ」が生まれます。

### リバーブの種類

| 種類 | 特徴 | 向いている用途 |
|------|------|-------------|
| **Room（ルーム）** | 小さな部屋の自然な響き | ドラム・ボーカル全般 |
| **Hall（ホール）** | コンサートホールの残響 | オーケストラ・ピアノ |
| **Plate（プレート）** | 金属板を使った滑らかな響き | ボーカル・スネア |
| **Spring（スプリング）** | バネを使った独特の響き | ギター・ビンテージ感 |

### 主なパラメーター

- **Decay Time（ディケイタイム）**: 残響が消えるまでの時間。短いほどタイト、長いほど広がり感が増す
- **Pre-delay**: 残響が始まるまでの遅延。適度なPre-delayでボーカルの明瞭度が上がる
- **Dry/Wet（Mix）**: 原音とリバーブ音のバランス。ボーカルは30〜40%が目安

---

## ゲート — 不要なノイズを自動でカット

<figure style="margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 340" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="340" fill="#0f172a" rx="10"/><text x="400" y="22" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#f1f5f9" font-weight="bold">ノイズゲート — Threshold / Attack / Release 動作原理</text><rect x="70" y="30" width="130" height="14" fill="#7f1d1d" rx="3"/><text x="135" y="40" text-anchor="middle" font-family="sans-serif" font-size="9" fill="#fca5a5" font-weight="bold">CLOSED</text><rect x="200" y="30" width="260" height="14" fill="#14532d" rx="3"/><text x="330" y="40" text-anchor="middle" font-family="sans-serif" font-size="9" fill="#86efac" font-weight="bold">OPEN</text><rect x="460" y="30" width="260" height="14" fill="#7f1d1d" rx="3"/><text x="590" y="40" text-anchor="middle" font-family="sans-serif" font-size="9" fill="#fca5a5" font-weight="bold">CLOSED</text><text x="16" y="155" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">音量</text><text x="400" y="272" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">時間 →</text><line x1="70" y1="250" x2="720" y2="250" stroke="#1e293b" stroke-width="1.5"/><text x="60" y="254" text-anchor="end" font-family="sans-serif" font-size="9" fill="#64748b">−∞</text><line x1="70" y1="178" x2="720" y2="178" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="8,4"/><text x="728" y="182" text-anchor="start" font-family="sans-serif" font-size="10" fill="#f59e0b">Threshold</text><polyline points="70,228 78,210 86,230 94,211 102,229 110,212 118,228 126,213 134,230 142,211 150,229 158,213 166,228 174,212 182,230 190,211 198,229" stroke="#3b82f6" stroke-width="2" fill="none"/><line x1="198" y1="229" x2="200" y2="80" stroke="#3b82f6" stroke-width="2"/><polyline points="200,80 220,75 245,82 270,77 295,80 320,76 345,82 370,78 395,80 420,76 445,82 458,78 460,80" stroke="#3b82f6" stroke-width="2.5" fill="none"/><line x1="460" y1="80" x2="462" y2="228" stroke="#3b82f6" stroke-width="2"/><polyline points="462,228 470,210 478,230 486,211 494,229 502,212 510,228 518,213 526,230 534,211 542,229 550,213 558,228 566,212 574,230 582,211 590,229 598,213 606,228 614,212 622,230 630,211 638,229 646,213 654,228 662,212 670,230 678,211 686,229 694,213 702,228 710,212 718,229 720,225" stroke="#3b82f6" stroke-width="2" fill="none"/><line x1="70" y1="250" x2="200" y2="250" stroke="#22c55e" stroke-width="2.5"/><line x1="200" y1="250" x2="216" y2="80" stroke="#22c55e" stroke-width="2.5"/><polyline points="216,76 245,82 270,77 295,80 320,76 345,82 370,78 395,80 420,76 445,82 458,78 460,80" stroke="#22c55e" stroke-width="2.5" fill="none"/><line x1="460" y1="80" x2="476" y2="250" stroke="#22c55e" stroke-width="2.5"/><line x1="476" y1="250" x2="720" y2="250" stroke="#22c55e" stroke-width="2.5"/><line x1="200" y1="58" x2="216" y2="58" stroke="#ec4899" stroke-width="1.5"/><line x1="200" y1="63" x2="200" y2="53" stroke="#ec4899" stroke-width="1.5"/><line x1="216" y1="63" x2="216" y2="53" stroke="#ec4899" stroke-width="1.5"/><text x="208" y="51" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#ec4899">Attack</text><line x1="200" y1="62" x2="200" y2="80" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="216" y1="62" x2="216" y2="76" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="460" y1="58" x2="476" y2="58" stroke="#a855f7" stroke-width="1.5"/><line x1="460" y1="63" x2="460" y2="53" stroke="#a855f7" stroke-width="1.5"/><line x1="476" y1="63" x2="476" y2="53" stroke="#a855f7" stroke-width="1.5"/><text x="468" y="51" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#a855f7">Release</text><line x1="460" y1="62" x2="460" y2="80" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><line x1="476" y1="62" x2="476" y2="250" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><text x="135" y="200" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#fca5a5">ノイズ除去</text><text x="590" y="200" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#fca5a5">ノイズ除去</text><line x1="490" y1="288" x2="526" y2="288" stroke="#3b82f6" stroke-width="2.5"/><text x="532" y="292" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Input (原音+ノイズ)</text><line x1="490" y1="305" x2="526" y2="305" stroke="#22c55e" stroke-width="2.5"/><text x="532" y="309" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Output (ゲート処理後)</text><line x1="490" y1="322" x2="526" y2="322" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="6,3"/><text x="532" y="326" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f59e0b">Threshold</text></svg></figure>


### ゲートとは

**一定の音量以下の信号を自動的にカット**するエフェクトです。正式にはノイズゲートと呼ばれます。

たとえばドラムのスネアを録音するとき、演奏していない時間帯にマイクがルームノイズや他の楽器の漏れ音を拾ってしまうことがあります。ゲートを使うと、スネアの音が鳴っている時だけ信号を通し、それ以外はカットすることができます。

### 主なパラメーター

| パラメーター | 役割 |
|------------|------|
| **Threshold（スレッショルド）** | ゲートが開く（音を通す）音量レベル |
| **Attack** | ゲートが開くまでの時間 |
| **Hold** | ゲートが開いている最低時間 |
| **Release** | ゲートが閉まるまでの時間 |

### ゲート設定のポイント

- Threshold は「ノイズは通さず、必要な音は通す」レベルに設定
- Attackは速め（1〜5ms）にしてアタック感を損なわないようにする
- Releaseを長くしすぎると、音の消え際に不自然なカットが起きる

---

## 3つのエフェクトの組み合わせ方

プロのボーカルトラックでの一般的な順序：

1. **ゲート** → ノイズを除去
2. **コンプレッサー** → 音量を均一化
3. **EQ** → 音質を整える
4. **リバーブ（センドリターンで）** → 空間感を追加

この順序が基本ですが、目的に応じて変更することもあります。

---

## DAW付属のプラグインから始める

<figure style="margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><defs><marker id="ah" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#3b82f6"/></marker></defs><rect x="40" y="68" width="120" height="64" fill="#3b82f6" rx="8"/><text x="100" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">音源の準備</text><text x="100" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(楽器/マイク)</text><line x1="162" y1="100" x2="186" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="190" y="68" width="120" height="64" fill="#6366f1" rx="8"/><text x="250" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">録音</text><text x="250" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(Audioトラック)</text><line x1="312" y1="100" x2="336" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="340" y="68" width="120" height="64" fill="#ec4899" rx="8"/><text x="400" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">編集</text><text x="400" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(カット/修正)</text><line x1="462" y1="100" x2="486" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="490" y="68" width="120" height="64" fill="#14b8a6" rx="8"/><text x="550" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">ミックス</text><text x="550" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(EQ/FX)</text><line x1="612" y1="100" x2="636" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="640" y="68" width="120" height="64" fill="#22c55e" rx="8"/><text x="700" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">書き出し</text><text x="700" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(WAV/MP3)</text></svg></figure>


最初から高価なサードパーティプラグインを購入する必要はありません。

GarageBand・Logic Pro・Cubase・Ableton Liveなど、主要なDAWにはコンプレッサー・リバーブ・ゲートが標準搭載されています。まず付属プラグインで操作に慣れてから、必要に応じてサードパーティ製を検討しましょう。

---

## まとめ

エフェクターの役割を覚えておけば、録音後の「音作り」が一気に変わります。

- **コンプレッサー**：音量のばらつきを整える
- **リバーブ**：空間と奥行きを演出する
- **ゲート**：不要なノイズを自動除去する

この3つを使いこなすだけで、宅録サウンドはプロクオリティに近づきます。
<div style="display:flex;gap:.75rem;margin:2rem 0;"><div style="flex:1;padding:.8rem 1rem 1rem;background:#e8f4fb;border-radius:10px;border:1px solid rgba(8,145,178,.25);"><span style="display:block;margin:0 0 .5rem;color:#374151;font-size:.82rem;font-weight:bold;">エフェクター をサウンドハウスで探す</span><a href="https://h.accesstrade.net/sp/cc?rk=01001xqc00os63&url=https%3A%2F%2Fwww.soundhouse.co.jp%2Fsearch%2Findex%2F%3Fsearch_all%3D%25E3%2582%25A8%25E3%2583%2595%25E3%2582%25A7%25E3%2582%25AF%25E3%2582%25BF%25E3%2583%25BC" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="display:block;text-decoration:none;text-align:center;"><img src="/assets/images/btn-soundhouse.jpg" alt="サウンドハウスで探す" width="240" style="height:auto;border-radius:8px;display:inline-block;"></a><img src="https://h.accesstrade.net/sp/rr?rk=01001xqc00os63" width="1" height="1" border="0" alt="" loading="lazy"></div><div style="flex:1;padding:.8rem 1rem 1rem;background:#fdf3ee;border-radius:10px;border:1px solid rgba(234,88,12,.25);"><span style="display:block;margin:0 0 .5rem;color:#374151;font-size:.82rem;font-weight:bold;">エフェクター を楽天市場で探す</span><a href="https://search.rakuten.co.jp/search/mall/%E3%82%A8%E3%83%95%E3%82%A7%E3%82%AF%E3%82%BF%E3%83%BC%20DTM/" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="display:block;text-decoration:none;text-align:center;"><img src="/assets/images/btn-rakuten.jpg" alt="楽天市場で探す" width="240" style="height:auto;border-radius:8px;display:inline-block;"></a></div></div>