---
layout: post
title: "コンプレッサー・リバーブ・ゲートの使い方 - 音楽制作エフェクター入門"
description: "音楽制作で欠かせないコンプレッサー・リバーブ・ゲートの基本的な使い方を解説。各エフェクターの役割とパラメーターを初心者向けにわかりやすく紹介します。"
date: 2026-05-11
categories: [effects]
tags: [コンプレッサー, リバーブ, ゲート, エフェクター, MIX]
---

本記事にはプロモーション・広告が含まれる場合があります。
<figure style="margin: 2rem 0; text-align: center;">
  <img src="https://images.unsplash.com/photo-1681876478920?w=800&q=75&auto=format&fit=crop"
       alt="エフェクトプロセッサーと音響機材"
       style="width: 100%; max-width: 720px; border-radius: 10px; box-shadow: 0 2px 12px rgba(0,0,0,0.12);">
  <figcaption style="font-size: 0.8rem; color: #888; margin-top: 0.5rem;">Photo: <a href="https://unsplash.com" target="_blank" rel="noopener">Unsplash</a></figcaption>
</figure>

## エフェクターとは — 音に「処理」を加えるツール

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><defs><marker id="ah" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#3b82f6"/></marker></defs><rect x="95" y="68" width="130" height="64" fill="#3b82f6" rx="8"/><text x="160" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">課題・ニーズ</text><line x1="227" y1="100" x2="251" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="255" y="68" width="130" height="64" fill="#6366f1" rx="8"/><text x="320" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">ツール活用</text><line x1="387" y1="100" x2="411" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="415" y="68" width="130" height="64" fill="#ec4899" rx="8"/><text x="480" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">効率化・改善</text><line x1="547" y1="100" x2="571" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="575" y="68" width="130" height="64" fill="#14b8a6" rx="8"/><text x="640" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">成果・価値</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：このツール/サービスが提供する価値の流れ</figcaption></figure>


録音した音をそのまま使うのではなく、より良い音に整えるために使うのが**エフェクター（エフェクトプラグイン）**です。

音楽制作において最もよく使われる3つのエフェクトが「コンプレッサー・リバーブ・ゲート」です。これらの使い方を理解するだけで、録音したサウンドのクオリティが大きく変わります。

---

## コンプレッサー — 音量の「でこぼこ」を平らにする

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 340" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="340" fill="#0f172a" rx="10"/><defs><marker id="arh" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#94a3b8"/></marker></defs><text x="400" y="22" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#f1f5f9" font-weight="bold">コンプレッサー — Threshold / Attack / Release / Ratio</text><text x="400" y="330" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">時間 →</text><text x="18" y="170" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">振幅</text><line x1="70" y1="170" x2="720" y2="170" stroke="#334155" stroke-width="1" stroke-dasharray="3,5"/><text x="60" y="174" text-anchor="end" font-family="sans-serif" font-size="10" fill="#94a3b8">0</text><line x1="70" y1="105" x2="720" y2="105" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="8,4"/><line x1="70" y1="235" x2="720" y2="235" stroke="#f59e0b" stroke-width="1" stroke-dasharray="4,4"/><text x="728" y="109" text-anchor="start" font-family="sans-serif" font-size="10" fill="#f59e0b">Threshold</text><text x="728" y="174" text-anchor="start" font-family="sans-serif" font-size="10" fill="#94a3b8">0 dB</text><polyline points="75,170 90,158 105,180 120,156 135,179 150,159 170,170" stroke="#3b82f6" stroke-width="1.5" fill="none"/><polyline points="170,170 195,52 340,52 365,170 720,170" stroke="#3b82f6" stroke-width="2.5" fill="none"/><polygon points="195,105 195,52 340,52 340,105" fill="#3b82f6" opacity="0.12"/><polyline points="170,170 195,52 225,90 340,90 373,184 400,170 720,170" stroke="#22c55e" stroke-width="2.5" fill="none"/><polygon points="225,105 225,90 340,90 340,105" fill="#22c55e" opacity="0.12"/><polygon points="225,52 340,52 340,90 225,90" fill="#f59e0b" opacity="0.3"/><text x="282" y="76" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#f59e0b" font-weight="bold">Gain Reduction</text><line x1="195" y1="34" x2="225" y2="34" stroke="#ec4899" stroke-width="1.5"/><line x1="195" y1="39" x2="195" y2="29" stroke="#ec4899" stroke-width="1.5"/><line x1="225" y1="39" x2="225" y2="29" stroke="#ec4899" stroke-width="1.5"/><text x="210" y="27" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#ec4899">Attack Time</text><line x1="195" y1="38" x2="195" y2="52" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="225" y1="38" x2="225" y2="90" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="365" y1="34" x2="400" y2="34" stroke="#a855f7" stroke-width="1.5"/><line x1="365" y1="39" x2="365" y2="29" stroke="#a855f7" stroke-width="1.5"/><line x1="400" y1="39" x2="400" y2="29" stroke="#a855f7" stroke-width="1.5"/><text x="382" y="27" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#a855f7">Release Time</text><line x1="365" y1="38" x2="365" y2="170" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><line x1="400" y1="38" x2="400" y2="170" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><line x1="360" y1="52" x2="400" y2="52" stroke="#3b82f6" stroke-width="1.5"/><line x1="360" y1="90" x2="400" y2="90" stroke="#22c55e" stroke-width="1.5"/><line x1="380" y1="52" x2="380" y2="90" stroke="#94a3b8" stroke-width="1" stroke-dasharray="3,3"/><text x="410" y="71" text-anchor="start" font-family="sans-serif" font-size="10" fill="#f1f5f9">Ratio</text><text x="410" y="85" text-anchor="start" font-family="sans-serif" font-size="12" fill="#22c55e" font-weight="bold">4:1</text><line x1="500" y1="268" x2="536" y2="268" stroke="#3b82f6" stroke-width="2.5"/><text x="542" y="272" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Input (原音)</text><line x1="500" y1="286" x2="536" y2="286" stroke="#22c55e" stroke-width="2.5"/><text x="542" y="290" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Output (圧縮後)</text><line x1="500" y1="304" x2="536" y2="304" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="6,3"/><text x="542" y="308" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f59e0b">Threshold</text><rect x="500" y="316" width="36" height="10" fill="#f59e0b" rx="2"/><text x="542" y="325" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f59e0b">Gain Reduction</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：コンプレッサーの動作 — Thresholdを超えた信号がAttack時間後にRatioで圧縮され、Releaseで解放される</figcaption></figure>


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

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><defs><marker id="ah" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#3b82f6"/></marker></defs><rect x="40" y="68" width="120" height="64" fill="#3b82f6" rx="8"/><text x="100" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">原音 (Dry)</text><line x1="162" y1="100" x2="186" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="190" y="68" width="120" height="64" fill="#6366f1" rx="8"/><text x="250" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">リバーブ</text><text x="250" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">ユニット</text><line x1="312" y1="100" x2="336" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="340" y="68" width="120" height="64" fill="#ec4899" rx="8"/><text x="400" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">残響音生成</text><line x1="462" y1="100" x2="486" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="490" y="68" width="120" height="64" fill="#14b8a6" rx="8"/><text x="550" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">Dry/Wet</text><text x="550" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">ブレンド</text><line x1="612" y1="100" x2="636" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="640" y="68" width="120" height="64" fill="#22c55e" rx="8"/><text x="700" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">出力</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：リバーブのシグナルフロー</figcaption></figure>


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

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 320" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="320" fill="#0f172a" rx="10"/><defs><marker id="arh" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#94a3b8"/></marker></defs><text x="400" y="22" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#f1f5f9" font-weight="bold">ノイズゲート — Threshold / Attack / Release 動作原理</text><text x="400" y="310" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">時間 →</text><text x="18" y="155" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">振幅</text><line x1="70" y1="155" x2="720" y2="155" stroke="#334155" stroke-width="1" stroke-dasharray="3,5"/><line x1="70" y1="95" x2="720" y2="95" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="8,4"/><line x1="70" y1="215" x2="720" y2="215" stroke="#f59e0b" stroke-width="1" stroke-dasharray="4,4"/><text x="728" y="99" text-anchor="start" font-family="sans-serif" font-size="10" fill="#f59e0b">Threshold</text><rect x="70" y="28" width="125" height="14" fill="#7f1d1d" rx="3"/><text x="132" y="38" text-anchor="middle" font-family="sans-serif" font-size="9" fill="#fca5a5" font-weight="bold">CLOSED</text><rect x="195" y="28" width="260" height="14" fill="#14532d" rx="3"/><text x="325" y="38" text-anchor="middle" font-family="sans-serif" font-size="9" fill="#86efac" font-weight="bold">OPEN</text><rect x="455" y="28" width="265" height="14" fill="#7f1d1d" rx="3"/><text x="587" y="38" text-anchor="middle" font-family="sans-serif" font-size="9" fill="#fca5a5" font-weight="bold">CLOSED</text><polyline points="70,155 85,137 100,170 115,135 130,171 145,138 160,169 175,136 190,165 195,155" stroke="#3b82f6" stroke-width="1.5" fill="none"/><polyline points="195,155 205,55 240,40 370,40 415,65 445,155 455,155" stroke="#3b82f6" stroke-width="2.5" fill="none"/><polygon points="205,95 205,40 240,40 370,40 415,65 445,95 445,95" fill="#3b82f6" opacity="0.12"/><polyline points="455,155 470,139 485,173 500,136 515,168 530,138 545,170 560,137 575,167 590,139 605,165 620,141 635,167 650,145 665,163 680,143 720,155" stroke="#3b82f6" stroke-width="1.5" fill="none"/><polyline points="70,155 205,155" stroke="#22c55e" stroke-width="2.5" fill="none"/><polyline points="205,155 218,55" stroke="#22c55e" stroke-width="2.5" fill="none"/><polyline points="218,55 240,40 370,40 415,65 445,155" stroke="#22c55e" stroke-width="2.5" fill="none"/><polyline points="445,155 465,155" stroke="#22c55e" stroke-width="2.5" fill="none"/><polyline points="465,155 720,155" stroke="#22c55e" stroke-width="2.5" fill="none"/><line x1="205" y1="52" x2="218" y2="52" stroke="#ec4899" stroke-width="1.5"/><line x1="205" y1="57" x2="205" y2="47" stroke="#ec4899" stroke-width="1.5"/><line x1="218" y1="57" x2="218" y2="47" stroke="#ec4899" stroke-width="1.5"/><text x="211" y="45" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#ec4899">Attack</text><line x1="205" y1="56" x2="205" y2="155" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="218" y1="56" x2="218" y2="55" stroke="#ec4899" stroke-width="1" stroke-dasharray="3,4"/><line x1="445" y1="52" x2="465" y2="52" stroke="#a855f7" stroke-width="1.5"/><line x1="445" y1="57" x2="445" y2="47" stroke="#a855f7" stroke-width="1.5"/><line x1="465" y1="57" x2="465" y2="47" stroke="#a855f7" stroke-width="1.5"/><text x="455" y="45" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#a855f7">Release</text><line x1="445" y1="56" x2="445" y2="155" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><line x1="465" y1="56" x2="465" y2="155" stroke="#a855f7" stroke-width="1" stroke-dasharray="3,4"/><text x="132" y="123" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#fca5a5">ノイズ除去</text><text x="587" y="123" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#fca5a5">ノイズ除去</text><line x1="505" y1="248" x2="541" y2="248" stroke="#3b82f6" stroke-width="2.5"/><text x="547" y="252" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Input (原音+ノイズ)</text><line x1="505" y1="266" x2="541" y2="266" stroke="#22c55e" stroke-width="2.5"/><text x="547" y="270" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f1f5f9">Output (ゲート処理後)</text><line x1="505" y1="284" x2="541" y2="284" stroke="#f59e0b" stroke-width="1.5" stroke-dasharray="6,3"/><text x="547" y="288" text-anchor="start" font-family="sans-serif" font-size="11" fill="#f59e0b">Threshold</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：ノイズゲートの動作 — Threshold以下の信号は遮断、以上はAttack時間でゲートが開きReleaseで閉じる</figcaption></figure>


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

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><defs><marker id="ah" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#3b82f6"/></marker></defs><rect x="40" y="68" width="120" height="64" fill="#3b82f6" rx="8"/><text x="100" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">音源の準備</text><text x="100" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(楽器/マイク)</text><line x1="162" y1="100" x2="186" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="190" y="68" width="120" height="64" fill="#6366f1" rx="8"/><text x="250" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">録音</text><text x="250" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(Audioトラック)</text><line x1="312" y1="100" x2="336" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="340" y="68" width="120" height="64" fill="#ec4899" rx="8"/><text x="400" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">編集</text><text x="400" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(カット/修正)</text><line x1="462" y1="100" x2="486" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="490" y="68" width="120" height="64" fill="#14b8a6" rx="8"/><text x="550" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">ミックス</text><text x="550" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(EQ/FX)</text><line x1="612" y1="100" x2="636" y2="100" stroke="#3b82f6" stroke-width="2" marker-end="url(#ah)"/><rect x="640" y="68" width="120" height="64" fill="#22c55e" rx="8"/><text x="700" y="96" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9" font-weight="bold">書き出し</text><text x="700" y="114" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#f1f5f9">(WAV/MP3)</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：DAWによる音楽制作の基本ワークフロー</figcaption></figure>


最初から高価なサードパーティプラグインを購入する必要はありません。

GarageBand・Logic Pro・Cubase・Ableton Liveなど、主要なDAWにはコンプレッサー・リバーブ・ゲートが標準搭載されています。まず付属プラグインで操作に慣れてから、必要に応じてサードパーティ製を検討しましょう。

---

## まとめ

エフェクターの役割を覚えておけば、録音後の「音作り」が一気に変わります。

- **コンプレッサー**：音量のばらつきを整える
- **リバーブ**：空間と奥行きを演出する
- **ゲート**：不要なノイズを自動除去する

この3つを使いこなすだけで、宅録サウンドはプロクオリティに近づきます。