---
layout: post
title: "MIX・マスタリング入門【2026年版】DAWで始める音楽制作の仕上げ工程"
description: "MIX（ミキシング）とマスタリングの違いをわかりやすく解説。初心者が最初に覚えるべきEQ・コンプ・リバーブの基礎から、無料DAWで実践できる仕上げ手順まで丁寧に説明します。"
date: 2026-05-24
categories: [production]
tags: [MIX, ミキシング, マスタリング, DAW, 音楽制作, 初心者]
image: /assets/images/thumb-mixing.jpg
---

## MIXとマスタリングの違い — まずここを押さえよう

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 180" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="180" fill="#0f172a" rx="10"/><defs><marker id="arh5" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#f97316"/></marker></defs><rect x="20" y="40" width="180" height="100" fill="#1e293b" rx="8" stroke="#3b82f6" stroke-width="1.5"/><text x="110" y="72" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#60a5fa" font-weight="bold">録音</text><text x="110" y="92" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">ボーカル・楽器</text><text x="110" y="110" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">各パートを録音</text><line x1="202" y1="90" x2="232" y2="90" stroke="#f97316" stroke-width="2" marker-end="url(#arh5)"/><rect x="234" y="40" width="180" height="100" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="324" y="72" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#34d399" font-weight="bold">MIX（ミキシング）</text><text x="324" y="92" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#cbd5e1">全パートの音量・音質・定位</text><text x="324" y="110" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#cbd5e1">を調整して1本のステムに</text><line x1="416" y1="90" x2="446" y2="90" stroke="#f97316" stroke-width="2" marker-end="url(#arh5)"/><rect x="448" y="40" width="180" height="100" fill="#1e293b" rx="8" stroke="#ec4899" stroke-width="1.5"/><text x="538" y="72" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#f472b6" font-weight="bold">マスタリング</text><text x="538" y="92" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#cbd5e1">音圧・音量の統一</text><text x="538" y="110" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#cbd5e1">配信プラットフォーム向け最終調整</text><line x1="630" y1="90" x2="660" y2="90" stroke="#f97316" stroke-width="2" marker-end="url(#arh5)"/><rect x="662" y="40" width="118" height="100" fill="#1e293b" rx="8" stroke="#f59e0b" stroke-width="1.5"/><text x="721" y="80" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#fbbf24" font-weight="bold">配信</text><text x="721" y="100" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">Spotify等へ</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：音楽制作の流れ — 録音→MIX→マスタリング→配信</figcaption></figure>

| | MIX（ミキシング） | マスタリング |
|--|-----------------|------------|
| **目的** | 各パートのバランスを整える | 楽曲全体の音圧・音質を整える |
| **対象** | マルチトラック（複数の音源） | ステム（MIX済み1〜2本） |
| **主なツール** | EQ・コンプ・リバーブ・パン | リミッター・マルチバンドコンプ |
| **誰がやるか** | エンジニア or DTMer本人 | 専門エンジニア or 本人 |

**MIXは「各楽器をバランスよく聴こえるようにする作業」、マスタリングは「曲全体を商業音楽のレベルに引き上げる最終仕上げ」**です。初心者はまずMIXをマスターしましょう。

---

## MIXの3大要素 — EQ・コンプ・リバーブ

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 200" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="200" fill="#0f172a" rx="10"/><rect x="20" y="20" width="240" height="160" fill="#1e293b" rx="8" stroke="#3b82f6" stroke-width="2"/><text x="140" y="50" text-anchor="middle" font-family="sans-serif" font-size="15" fill="#60a5fa" font-weight="bold">EQ（イコライザー）</text><text x="40" y="78" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 特定の周波数を上げ下げ</text><text x="40" y="98" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 不要な低域をカット（HPF）</text><text x="40" y="118" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 音の「場所」を作る</text><text x="40" y="145" font-family="sans-serif" font-size="10" fill="#64748b">例: ボーカル100Hz以下カット</text><rect x="280" y="20" width="240" height="160" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="400" y="50" text-anchor="middle" font-family="sans-serif" font-size="15" fill="#34d399" font-weight="bold">コンプレッサー</text><text x="300" y="78" font-family="sans-serif" font-size="11" fill="#cbd5e1">● ダイナミクス（音量差）を圧縮</text><text x="300" y="98" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 音量を安定させる</text><text x="300" y="118" font-family="sans-serif" font-size="11" fill="#cbd5e1">● アタック感を強調</text><text x="300" y="145" font-family="sans-serif" font-size="10" fill="#64748b">例: ドラムのスネアにかけてパンチを出す</text><rect x="540" y="20" width="240" height="160" fill="#1e293b" rx="8" stroke="#ec4899" stroke-width="2"/><text x="660" y="50" text-anchor="middle" font-family="sans-serif" font-size="15" fill="#f472b6" font-weight="bold">リバーブ / ディレイ</text><text x="560" y="78" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 空間・残響を加える</text><text x="560" y="98" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 楽器に奥行きを作る</text><text x="560" y="118" font-family="sans-serif" font-size="11" fill="#cbd5e1">● 「狭い部屋」〜「大ホール」を演出</text><text x="560" y="145" font-family="sans-serif" font-size="10" fill="#64748b">例: ボーカルに短いリバーブで自然な広がり</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：MIXの3大エフェクト — まずこの3つの役割を覚えよう</figcaption></figure>

### EQ（イコライザー）の基本

EQは**音の「周波数」をコントロールするツール**です。初心者が最初に覚えるべき操作は2つ：

| 操作 | 意味 | 典型的な使い方 |
|------|------|-------------|
| **ハイパスフィルター（HPF）** | 低域（ゴロゴロ音）をカット | ボーカル・ギター・シンバルの低域除去 |
| **特定周波数のブースト/カット** | 目立たせたい音域を強調 | ボーカルの「通り」を出す5kHz付近をブースト |

### コンプレッサーの基本パラメーター

| パラメーター | 説明 | 初期値の目安 |
|------------|------|------------|
| **Threshold（スレッショルド）** | コンプが働き始める音量 | -20〜-10dB |
| **Ratio（レシオ）** | 圧縮の強さ | 4:1 が汎用的 |
| **Attack** | コンプがかかる速さ | 20〜50ms（ドラムは遅め） |
| **Release** | コンプが解放される速さ | 100〜300ms |

### リバーブの種類

| タイプ | 特徴 | 向いている楽器 |
|-------|------|-------------|
| **Room** | 小さい部屋の残響。自然な広がり | ボーカル・スネア |
| **Hall** | 大ホール。豊かな残響 | ストリングス・ピアノ |
| **Plate** | 金属板の独特な響き | ボーカル・スネアのクラシック処理 |

---

## MIXの手順 — 初心者向け5ステップ

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 160" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="160" fill="#0f172a" rx="10"/><defs><marker id="arh6" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#f97316"/></marker></defs><rect x="15" y="35" width="130" height="90" fill="#1e293b" rx="6" stroke="#3b82f6" stroke-width="1.5"/><text x="80" y="66" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#60a5fa" font-weight="bold">①ゲイン整理</text><text x="80" y="84" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">各トラックの</text><text x="80" y="100" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">音量を揃える</text><line x1="147" y1="80" x2="165" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh6)"/><rect x="167" y="35" width="130" height="90" fill="#1e293b" rx="6" stroke="#22c55e" stroke-width="1.5"/><text x="232" y="66" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#34d399" font-weight="bold">②EQで整理</text><text x="232" y="84" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">不要な周波数を</text><text x="232" y="100" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">カット</text><line x1="299" y1="80" x2="317" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh6)"/><rect x="319" y="35" width="130" height="90" fill="#1e293b" rx="6" stroke="#ec4899" stroke-width="1.5"/><text x="384" y="66" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#f472b6" font-weight="bold">③コンプで安定</text><text x="384" y="84" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">音量差を圧縮し</text><text x="384" y="100" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">安定させる</text><line x1="451" y1="80" x2="469" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh6)"/><rect x="471" y="35" width="130" height="90" fill="#1e293b" rx="6" stroke="#8b5cf6" stroke-width="1.5"/><text x="536" y="66" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#a78bfa" font-weight="bold">④パン定位</text><text x="536" y="84" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">各パートを左右に</text><text x="536" y="100" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">配置</text><line x1="603" y1="80" x2="621" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh6)"/><rect x="623" y="35" width="158" height="90" fill="#1e293b" rx="6" stroke="#f59e0b" stroke-width="1.5"/><text x="702" y="66" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fbbf24" font-weight="bold">⑤空間処理</text><text x="702" y="84" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">リバーブ・ディレイで</text><text x="702" y="100" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">奥行きを追加</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：MIXの基本5ステップ — この順番で進めることで整ったMIXになる</figcaption></figure>

**Step 1: ゲイン整理（音量の正規化）**  
すべてのトラックの音量を聴きながら揃える。まずはフェーダーだけで全体のバランスを作ることに集中。

**Step 2: EQで不要成分をカット**  
各楽器の不要な低域をHPFでカット。「被り」（ぶつかっている周波数）を整理する。

**Step 3: コンプレッサーで音量を安定化**  
飛び出している音量の波を圧縮。ドラムのパンチ感、ボーカルの安定感を作る。

**Step 4: パン（定位）で左右に配置**  
楽器を左右に配置して「音のステージ」を作る。ドラム・ベース・ボーカルはセンターが基本。

**Step 5: リバーブ・ディレイで空間処理**  
各パートに適切な残響を加えて奥行きを作る。かけすぎると「遠く」なるので注意。

---

## マスタリングの基本 — 初心者はリミッターから始めよう

マスタリングの第一歩は**リミッター（トゥルーピークリミッター）** の使い方を覚えることです。

| パラメーター | 説明 | 推奨値（配信向け） |
|------------|------|---------------|
| **アウトプットゲイン** | 最終的な音量レベル | -1.0〜-0.5dBFS（クリッピング防止） |
| **LUFS（ラウドネス）** | 曲の知覚音量 | -14LUFS（Spotify/Apple基準） |

**配信プラットフォームのラウドネス規格：**
- Spotify: -14 LUFS
- Apple Music: -16 LUFS  
- YouTube: -14 LUFS

---

## 初心者向け無料MIXプラグイン

| プラグイン | 種類 | 配布元 | 特徴 |
|----------|------|-------|------|
| **TDR Nova** | ダイナミックEQ | Tokyo Dawn Records | 高品質・無料・プロも使用 |
| **Digitech DBM Free** | コンプ | Analog Obsession | シンプルで扱いやすい |
| **Valhalla Supermassive** | リバーブ/ディレイ | Valhalla | 無料とは思えないクオリティ |
| **OTT** | マルチバンドコンプ | Xfer Records | EDMで定番。独特のサウンド |
| **Youlean Loudness Meter** | ラウドネス計測 | Youlean | LUFS確認に必須 |

これらはすべて無料でダウンロードでき、DAWのプラグインとして使用できます。

---

## MIXに適したモニタースピーカーとヘッドフォン

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 160" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="160" fill="#0f172a" rx="10"/><rect x="20" y="20" width="370" height="120" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="205" y="50" text-anchor="middle" font-family="sans-serif" font-size="14" fill="#34d399" font-weight="bold">モニタースピーカー（推奨）</text><text x="40" y="78" font-family="sans-serif" font-size="11" fill="#cbd5e1">✅ 空間の広がり・定位を正確に確認</text><text x="40" y="98" font-family="sans-serif" font-size="11" fill="#cbd5e1">✅ 長時間作業で耳が疲れにくい</text><text x="40" y="118" font-family="sans-serif" font-size="11" fill="#94a3b8">△ 部屋の音響環境が音質に影響する</text><rect x="410" y="20" width="370" height="120" fill="#1e293b" rx="8" stroke="#6366f1" stroke-width="1.5"/><text x="595" y="50" text-anchor="middle" font-family="sans-serif" font-size="14" fill="#818cf8" font-weight="bold">モニタリングヘッドフォン</text><text x="430" y="78" font-family="sans-serif" font-size="11" fill="#cbd5e1">✅ 部屋の影響を受けない</text><text x="430" y="98" font-family="sans-serif" font-size="11" fill="#cbd5e1">✅ 細部のノイズ確認に強い</text><text x="430" y="118" font-family="sans-serif" font-size="11" fill="#94a3b8">△ 立体感・定位の把握に限界がある</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：MIX作業での出力機器の比較</figcaption></figure>

MIX作業には**フラットな音響特性（音を色付けしない）**のモニター機器が必須です。リスニング用スピーカーやイヤフォンは、特定の周波数が強調されているため、MIXすると他の環境で聴いたときに偏りが生まれます。

**おすすめモニタースピーカー:**

| モデル | 価格帯 | 特徴 |
|-------|-------|------|
| **YAMAHA HS5**<a href="https://h.accesstrade.net/sp/cc?rk=01001xqc00os63&url=https%3A%2F%2Fwww.soundhouse.co.jp%2Fsearch%2Findex%2F%3Fsearch_all%3DYAMAHA+HS5" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="margin-left:.3em;font-size:.85em;text-decoration:none;" title="サウンドハウスで見る">🛒</a> | ¥35,000〜/本 | スタジオ定番。フラットで正確 |
| **ADAM Audio T5V**<a href="https://h.accesstrade.net/sp/cc?rk=01001xqc00os63&url=https%3A%2F%2Fwww.soundhouse.co.jp%2Fsearch%2Findex%2F%3Fsearch_all%3DADAM+T5V" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="margin-left:.3em;font-size:.85em;text-decoration:none;" title="サウンドハウスで見る">🛒</a> | ¥25,000〜/本 | リボンツイーター搭載。高域が滑らか |
| **KRK Rokit 5 G4**<a href="https://h.accesstrade.net/sp/cc?rk=01001xqc00os63&url=https%3A%2F%2Fwww.soundhouse.co.jp%2Fsearch%2Findex%2F%3Fsearch_all%3DKRK+Rokit+5" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="margin-left:.3em;font-size:.85em;text-decoration:none;" title="サウンドハウスで見る">🛒</a> | ¥30,000〜/本 | 低域が豊か。ヒップホップ・EDM向き |

---

## MIXの参考書・入門書

| 書名 | 著者 | 特徴 |
|------|------|------|
| はじめてのMIXING & MASTERING | 石田ごう | DAWの具体的操作を丁寧に解説。初心者入門書として定番 |
| MIXの教科書 | DURAN | プロが教えるMIXの考え方と手順。ステップ形式で進めやすい |
| DTM音楽制作パーフェクトガイド | 各社 | 録音から配信まで一冊で学べる総合書 |

<!-- AFFILIATE_PLACEHOLDER: Amazon教則本リンク（もしもアフィリエイト Amazon審査通過後に設置予定 site_id=672391） -->

<div style="display:flex;gap:.75rem;margin:2rem 0;">
<div style="flex:1;padding:.8rem 1rem 1rem;background:#e8f4fb;border-radius:10px;border:1px solid rgba(8,145,178,.25);">
<p style="margin:0 0 .5rem;color:#374151;font-size:.82rem;font-weight:bold;">モニタースピーカー をサウンドハウスで探す</p>
<a href="https://h.accesstrade.net/sp/cc?rk=01001xqc00os63&url=https%3A%2F%2Fwww.soundhouse.co.jp%2Fsearch%2Findex%2F%3Fsearch_all%3D%E3%83%A2%E3%83%8B%E3%82%BF%E3%83%BC%E3%82%B9%E3%83%94%E3%83%BC%E3%82%AB%E3%83%BC" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="display:block;text-decoration:none;"><img src="/assets/images/btn-soundhouse.jpg" alt="サウンドハウスで探す" width="240" style="height:auto;border-radius:8px;display:block;"></a>
<img src="https://h.accesstrade.net/sp/rr?rk=01001xqc00os63" width="1" height="1" border="0" alt="" loading="lazy">
</div>
<div style="flex:1;padding:.8rem 1rem 1rem;background:#fdf3ee;border-radius:10px;border:1px solid rgba(234,88,12,.25);">
<p style="margin:0 0 .5rem;color:#374151;font-size:.82rem;font-weight:bold;">モニタースピーカー を楽天市場で探す</p>
<a href="https://hb.afl.rakuten.co.jp/hgc/0b15ddc7.28c5c9ed.0b15ddc8.5d23dd4d/?pc=https%3A%2F%2Fsearch.rakuten.co.jp%2Fsearch%2Fmall%2F%E3%83%A2%E3%83%8B%E3%82%BF%E3%83%BC%E3%82%B9%E3%83%94%E3%83%BC%E3%82%AB%E3%83%BC%2B%E9%8C%B2%E9%9F%B3%2B%E5%88%9D%E5%BF%83%E8%80%85%2F" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="display:block;text-decoration:none;"><img src="/assets/images/btn-rakuten.jpg" alt="楽天市場で探す" width="240" style="height:auto;border-radius:8px;display:block;"></a>
<img src="//i.moshimo.com/af/i/impression?a_id=5565352&amp;p_id=54&amp;pc_id=54&amp;pl_id=616" width="1" height="1" style="border:none;" alt="" loading="lazy">
</div>
</div>