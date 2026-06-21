---
layout: post
title: "Higgsfield MCP × Claude Codeでミュージックビデオを作る方法【2026年版】入門者でも完結するAI動画制作ガイド"
description: "Higgsfield MCPをClaude Codeに接続してAIミュージックビデオを作る方法を徹底解説。セットアップから楽曲生成・映像制作・字幕編集まで、AI連携だけで完結するフルワークフローを入門者向けにわかりやすく説明します。"
date: 2026-06-21
categories: [production]
tags: [Higgsfield, MCP, Claude Code, AI動画, ミュージックビデオ, Suno AI, 初心者, AI連携]
image: /assets/images/thumb-higgsfield-mcp-music-video.jpg
---

## Higgsfield MCPとは？ — AIエージェントから直接動画を生成できる仕組み

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 180" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="180" fill="#0f172a" rx="10"/><defs><marker id="arh1" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#f97316"/></marker></defs><rect x="20" y="50" width="160" height="80" fill="#1e293b" rx="8" stroke="#6366f1" stroke-width="2"/><text x="100" y="85" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#818cf8" font-weight="bold">Claude Code</text><text x="100" y="105" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">プロンプトを入力</text><line x1="182" y1="90" x2="210" y2="90" stroke="#f97316" stroke-width="2" marker-end="url(#arh1)"/><rect x="212" y="50" width="180" height="80" fill="#7c3aed" rx="8"/><text x="302" y="82" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#f1f5f9" font-weight="bold">Higgsfield MCP</text><text x="302" y="100" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#ddd6fe">30以上の動画・画像AIモデル</text><text x="302" y="116" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#c4b5fd">Sora / Kling / Veo / Seedance</text><line x1="394" y1="90" x2="422" y2="90" stroke="#f97316" stroke-width="2" marker-end="url(#arh1)"/><rect x="424" y="50" width="340" height="80" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="594" y="78" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#34d399" font-weight="bold">AI生成動画（最大4K・15秒）</text><text x="594" y="98" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#cbd5e1">リアル風キャラクター・シネマティック映像</text><text x="594" y="116" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">APIキー不要・OAuthで即接続</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：Higgsfield MCPの仕組み — Claude CodeからAIモデルを直接呼び出して動画を生成</figcaption></figure>

**Higgsfield MCP**は、2026年4月にリリースされたAI動画・画像生成プラットフォーム「Higgsfield AI」の公式MCPサーバーです。

MCP（Model Context Protocol）とは、AIエージェント（Claude Codeなど）が外部ツールを呼び出すための規格です。Higgsfield MCPを使うと、**Claude Codeに話しかけるだけで**Sora・Kling・Veo・Seedance 2.0といった最新AI動画モデルを呼び出し、映像を生成できます。

**Higgsfield MCPの主な特徴：**
- 30以上のAI動画・画像生成モデルに1つの接続で対応
- 最大4K解像度・1クリップ15秒まで生成可能
- APIキー不要（Higgsfield アカウントで OAuth認証）
- Seedance 2.0はオーディオ入力対応（音楽に合わせた映像生成が可能）
- リアル風キャラクターの一貫性維持（同一キャラクターを複数シーンに配置）

---

## ミュージックビデオをAIで作る — 全体の流れ

このガイドでは、以下のフルワークフローをAI連携だけで完結させます。

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 220" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="220" fill="#0f172a" rx="10"/><defs><marker id="arh2" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#f97316"/></marker></defs><rect x="20" y="30" width="130" height="70" fill="#1e293b" rx="8" stroke="#6366f1" stroke-width="2"/><text x="85" y="60" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#818cf8" font-weight="bold">STEP 1</text><text x="85" y="78" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">Suno AIで</text><text x="85" y="94" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">楽曲を生成</text><line x1="152" y1="65" x2="172" y2="65" stroke="#f97316" stroke-width="2" marker-end="url(#arh2)"/><rect x="174" y="30" width="130" height="70" fill="#1e293b" rx="8" stroke="#7c3aed" stroke-width="2"/><text x="239" y="60" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#c084fc" font-weight="bold">STEP 2</text><text x="239" y="78" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">Claude Codeで</text><text x="239" y="94" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">歌詞・構成を整理</text><line x1="306" y1="65" x2="326" y2="65" stroke="#f97316" stroke-width="2" marker-end="url(#arh2)"/><rect x="328" y="30" width="130" height="70" fill="#1e293b" rx="8" stroke="#0ea5e9" stroke-width="2"/><text x="393" y="60" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#38bdf8" font-weight="bold">STEP 3</text><text x="393" y="78" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">Higgsfield MCPで</text><text x="393" y="94" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">映像シーンを生成</text><line x1="460" y1="65" x2="480" y2="65" stroke="#f97316" stroke-width="2" marker-end="url(#arh2)"/><rect x="482" y="30" width="130" height="70" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="547" y="60" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#34d399" font-weight="bold">STEP 4</text><text x="547" y="78" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">CapCutで</text><text x="547" y="94" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">字幕・編集・書き出し</text><line x1="614" y1="65" x2="634" y2="65" stroke="#f97316" stroke-width="2" marker-end="url(#arh2)"/><rect x="636" y="30" width="130" height="70" fill="#f97316" rx="8"/><text x="701" y="60" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#fff" font-weight="bold">STEP 5</text><text x="701" y="78" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fed7aa">YouTubeへ</text><text x="701" y="94" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fed7aa">投稿</text><text x="400" y="155" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#94a3b8">使用ツール：Suno AI（楽曲）→ Claude Code + Higgsfield MCP（映像）→ CapCut（編集）</text><text x="400" y="178" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#64748b">すべてAI連携で完結・物理作業ゼロ</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：AIミュージックビデオ制作のフルワークフロー</figcaption></figure>

| ステップ | ツール | 作業内容 | 所要時間 |
|--------|------|---------|---------|
| **STEP 1** 楽曲生成 | Suno AI | ジャンル・歌詞を指定して楽曲を出力 | 5〜10分 |
| **STEP 2** 構成整理 | Claude Code | 楽曲を区間に分けてシーン設計 | 5分 |
| **STEP 3** 映像生成 | Higgsfield MCP | 各シーンの動画クリップを生成 | 30〜60分 |
| **STEP 4** 編集・字幕 | CapCut（無料） | クリップ結合・歌詞字幕・書き出し | 20〜30分 |
| **STEP 5** 投稿 | YouTube | アップロード・説明文・タグ設定 | 10分 |

---

## 始める前に — 必要なサービスと費用の目安

このワークフローで使うサービスは4つです。それぞれの最低限のプランと、月にどのくらい作れるかをまとめました。

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 260" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="260" fill="#0f172a" rx="10"/><text x="400" y="30" text-anchor="middle" font-family="sans-serif" font-size="14" fill="#94a3b8" font-weight="bold">月1本MVを作るための最低コスト試算</text><rect x="20" y="48" width="175" height="190" fill="#1e293b" rx="8" stroke="#6366f1" stroke-width="2"/><text x="107" y="74" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#818cf8" font-weight="bold">Claude Code</text><text x="107" y="96" text-anchor="middle" font-family="sans-serif" font-size="20" fill="#f1f5f9" font-weight="bold">$20/月</text><text x="107" y="116" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">Proプラン</text><text x="107" y="140" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">AIエージェント本体</text><text x="107" y="158" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">MCP接続・映像指示</text><text x="107" y="176" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">シーン設計・歌詞作成</text><text x="107" y="218" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#34d399">✓ 無制限で使用可</text><rect x="207" y="48" width="175" height="190" fill="#1e293b" rx="8" stroke="#7c3aed" stroke-width="2"/><text x="294" y="74" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#c084fc" font-weight="bold">Higgsfield AI</text><text x="294" y="96" text-anchor="middle" font-family="sans-serif" font-size="20" fill="#f1f5f9" font-weight="bold">$15/月〜</text><text x="294" y="116" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">Starterプラン（年払い）</text><text x="294" y="140" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">映像生成 200cr/月</text><text x="294" y="158" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">Kling: 約33本/月</text><text x="294" y="176" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">Veo/Sora: 約3〜5本/月</text><text x="294" y="218" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fbbf24">△ 月1本MVなら足りる</text><rect x="394" y="48" width="175" height="190" fill="#1e293b" rx="8" stroke="#0ea5e9" stroke-width="2"/><text x="481" y="74" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#38bdf8" font-weight="bold">Suno AI</text><text x="481" y="96" text-anchor="middle" font-family="sans-serif" font-size="20" fill="#f1f5f9" font-weight="bold">$10/月</text><text x="481" y="116" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">Proプラン</text><text x="481" y="140" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">楽曲生成 2,500cr/月</text><text x="481" y="158" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">約500曲/月</text><text x="481" y="176" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">商業利用・配信OK</text><text x="481" y="218" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#34d399">✓ 十分すぎる量</text><rect x="581" y="48" width="200" height="190" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="681" y="74" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#34d399" font-weight="bold">CapCut</text><text x="681" y="96" text-anchor="middle" font-family="sans-serif" font-size="20" fill="#f1f5f9" font-weight="bold">無料</text><text x="681" y="116" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#94a3b8">フリープラン</text><text x="681" y="140" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">動画編集・字幕追加</text><text x="681" y="158" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">1080p書き出しOK</text><text x="681" y="176" text-anchor="middle" font-family="sans-serif" font-size="10" fill="#64748b">ウォーターマークなし</text><text x="681" y="218" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#34d399">✓ 無料で十分</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：月1本MVを作るための最低コスト — 合計$45/月（約¥6,700）から始められる</figcaption></figure>

### サービス別 詳細

| サービス | 役割 | 最低プラン | 月額 | 月にどのくらい作れるか |
|---------|------|----------|------|----------------------|
| **Claude Code** | AIエージェント本体。シーン設計・プロンプト生成・MCP操作 | Proプラン | $20（約¥3,000） | 制限なし。日常的に使い放題 |
| **Higgsfield AI** | AI映像生成（Kling・Veo・Seedance等） | Starterプラン（年払い） | $15（約¥2,200） | 200クレジット/月。Kling使用で約33クリップ、Veo/Soraで5〜8クリップ |
| **Suno AI** | 楽曲・ボーカル生成 | Proプラン | $10（約¥1,500） | 2,500クレジット/月 = 約500曲。商業利用・YouTube収益化OK |
| **CapCut** | 動画編集・歌詞字幕・書き出し | **無料プラン** | ¥0 | 月15分以内の動画を無制限で書き出し。1080p・ウォーターマークなし |
| **合計** | | | **$45/月（約¥6,700）** | **月1〜2本のMVを制作可能** |

### Higgsfieldのクレジット消費の目安

映像1クリップ（8〜10秒）あたりのクレジット消費数です。

| モデル | クレジット消費 | Starterプラン(200cr)で作れる本数 | 映像の特徴 |
|------|-------------|-------------------------------|---------|
| **Kling 3.0** | 約6cr | 約33クリップ | 人物動作・表情が自然。歌唱シーンに最適 |
| **Seedance 2.0** | 約15〜20cr | 約10〜13クリップ | 音楽同期対応・多入力。MV全体の柱に |
| **Veo 3.1** | 約40〜50cr | 約4〜5クリップ | 映画的な映像品質。風景・アクションに |
| **Sora 2** | 約60〜70cr | 約3クリップ | 複雑なカメラワーク・物理表現 |

**実践的な使い方のコツ：** MV1本あたり6〜8クリップ必要です。Starterプランでは**Kling中心（1クリップ6cr）でシーンを生成し、サビだけVeo/Soraに切り替える**のがコスパの良い構成です（合計80〜100cr程度）。

### まず無料で試す方法

いきなり課金せずに動作確認したい場合：

1. **Higgsfield AI** — 無料アカウントで毎日10クレジット付与（Kling換算で約1クリップ/日）
2. **Suno AI** — 無料プランで毎日50クレジット付与（約10曲/日、非商業利用）
3. **Claude Code** — 無料プランでもMCP接続・映像指示は可能（ただし使用量に上限あり）
4. **CapCut** — 完全無料で使い続けられる

無料枠で一連の流れを体験してから、必要に応じて有料プランに移行するのがおすすめです。

---

## STEP 0：Higgsfield MCPをClaude Codeに接続する（セットアップ）

### 1. Higgsfield AIのアカウントを作成する

1. [higgsfield.ai](https://higgsfield.ai) にアクセス
2. 「Sign Up」からGoogleアカウントまたはメールで登録
3. 無料プランで登録完了（クレジットが付与される）

**料金について：** Higgsfield AIはクレジット制です。動画生成はモデル・解像度によって数十〜数百クレジット消費します。まず無料クレジットで試してから、必要に応じてプランを選んでください。

### 2. Claude Codeの `.mcp.json` にHiggsfield MCPを追加する

プロジェクトのルートにある `.mcp.json`（なければ新規作成）を開き、以下を追加します。

```json
{
  "mcpServers": {
    "higgsfield": {
      "type": "http",
      "url": "https://mcp.higgsfield.ai/mcp"
    }
  }
}
```

**ターミナルから一発でセットアップする場合：**

```bash
claude mcp add --transport http --scope user higgsfield https://mcp.higgsfield.ai/mcp
```

`--scope user` を指定すると `~/.claude/mcp.json` に書き込まれ、すべてのプロジェクトで使えるようになります。

### 3. OAuth認証を完了させる

Claude Codeを再起動すると、初回利用時にブラウザが自動で開きます。

1. Higgsfield AIのアカウントでログイン
2. 「Allow Access」をクリック
3. ターミナルに戻ると接続完了

認証の確認は次のコマンドで：

```bash
claude mcp list
```

`higgsfield` が表示されれば接続成功です。

---

## STEP 1：Suno AIでオリジナル楽曲を生成する

### 楽曲プロンプトの書き方

Suno AI（[suno.com](https://suno.com)）で楽曲を生成します。ジャンル・テンポ・雰囲気を英語で具体的に書くのがコツです。

**ファンク×ロック系J-POP（ボーカルあり）のプロンプト例：**

```
japanese pop song, funk groove, rock guitar, male vocals,
upbeat tempo, city night vibe, catchy chorus, 
synthesizer bass, electric guitar riff, 120bpm
```

**Custom Mode（歌詞を自分で書く）の使い方：**

Custom Modeでは `[Verse]`・`[Chorus]` タグを使って構成を指定できます。

```
[Verse 1]
夜明けの街を走り抜けて
あの頃の夢を追いかけてた

[Chorus]
ここから始まる 新しい朝
諦めない限り 終わらない旅

[Verse 2]
傷だらけの手のひら握って
もう一度だけ立ち上がる

[Chorus]
ここから始まる 新しい朝
諦めない限り 終わらない旅
```

### 生成した楽曲のダウンロード

1. 気に入ったバージョンを選ぶ
2. 「...」→「Download」→「Audio」でMP3をダウンロード
3. ファイル名を `mv-track-01.mp3` など分かりやすく変更して保存

**注意：** 無料プランの楽曲は商業利用不可。YouTubeへの収益化投稿にはProプラン（$8/月）が必要です。

---

## STEP 2：Claude Codeでシーン構成を設計する

楽曲の区間を区切り、各シーンに映像のイメージを割り当てます。Claude Codeに以下のように依頼するだけで設計できます。

**Claude Codeへの依頼例：**

```
楽曲の構成は Verse1(0:00-0:30) / Chorus(0:30-1:00) / Verse2(1:00-1:30) / Chorus(1:30-2:00) です。
夜の東京の街中を歩く若い男性キャラクターが主人公のミュージックビデオを作ります。
各セクションに合う映像シーンを5〜6本提案してください。
Higgsfield MCPで生成するための英語プロンプトも一緒に書いてください。
```

**出力例（Claude Codeが提案するシーン設計）：**

| シーン | 区間 | 映像内容 | Higgsfield プロンプト |
|------|------|---------|---------------------|
| Scene 1 | Verse 1 | 渋谷交差点を歩くシーン | young Japanese man walking through Shibuya crossing at night, neon lights, cinematic |
| Scene 2 | Chorus | 路地裏でカメラを見て歌うシーン | young man singing in Tokyo alley, dynamic camera, music video style |
| Scene 3 | Verse 2 | 夜景を見下ろすビル屋上シーン | rooftop view of Tokyo city lights at night, atmospheric, moody |
| Scene 4 | Chorus（ラスト） | スローモーションで振り返るシーン | slow motion, man turns to camera, street lights blur, emotional |

---

## STEP 3：Higgsfield MCPで映像を生成する

シーン設計ができたら、Claude Codeから直接 Higgsfield MCPを呼び出して動画を生成します。

### Claude Codeへの基本的な指示の書き方

```
Higgsfield MCPで以下のシーンの動画を生成してください。

Scene 1:
- モデル: Seedance 2.0（または Kling）
- プロンプト: young Japanese man walking through Shibuya crossing at night, 
  neon lights reflecting on wet pavement, cinematic, 4K, realistic
- アスペクト比: 16:9
- 尺: 8秒

生成が完了したらダウンロードリンクを教えてください。
```

### Higgsfield MCPで使えるモデルの特徴

| モデル | 得意なシーン | 特徴 |
|------|------------|------|
| **Seedance 2.0** | 音楽に合わせた映像・多入力 | テキスト・画像・音声を同時入力可能。音楽と動画を同期させるのに最適 |
| **Kling 3.0** | リアルな人物動作 | 人間の動き・表情の自然さが高い。歌唱シーンに向く |
| **Veo 3.1** | 映画的な映像品質 | シネマティックな質感。風景・アクションシーンに強い |
| **Sora 2** | 物理的な動きの正確さ | 複雑なカメラワーク・物理シミュレーションが得意 |

### キャラクターの一貫性を保つ（Soul機能）

複数シーンに同じキャラクターを登場させたい場合、Higgsfieldの**Soul機能**でキャラクターを事前にトレーニングできます。

Claude Codeへの指示：

```
Higgsfield MCPのcreate_character機能を使って、
以下の説明でキャラクターを作成してください：
- 20代の日本人男性
- 黒いジャケット、ジーンズ
- 短髪、シンプルなスタイル
キャラクターIDを教えてください。以降のシーン生成に使います。
```

一度作成したキャラクターIDを各シーンの生成プロンプトに含めることで、外見が統一されたミュージックビデオが完成します。

### 生成ステータスの確認

動画生成には数分かかります。Claude Codeに確認を依頼できます：

```
先ほど生成を依頼した動画のステータスを確認してください。
完了していたらダウンロードURLを教えてください。
```

---

## STEP 4：CapCutで字幕・編集・書き出しをする

生成した動画クリップを無料の動画編集アプリ「CapCut」で仕上げます。

<figure style="text-align:center;margin:2rem auto;max-width:800px;"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 160" style="max-width:100%;height:auto;border-radius:10px;display:block;"><rect width="800" height="160" fill="#0f172a" rx="10"/><defs><marker id="arh3" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto"><path d="M0,0 L0,6 L8,3 z" fill="#f97316"/></marker></defs><rect x="20" y="40" width="140" height="80" fill="#1e293b" rx="8" stroke="#7c3aed" stroke-width="2"/><text x="90" y="72" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#c084fc" font-weight="bold">動画クリップ</text><text x="90" y="90" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">Higgsfieldで生成</text><text x="90" y="108" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">6〜8本のMP4</text><line x1="162" y1="80" x2="182" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh3)"/><rect x="184" y="40" width="140" height="80" fill="#1e293b" rx="8" stroke="#0ea5e9" stroke-width="2"/><text x="254" y="72" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#38bdf8" font-weight="bold">音楽トラック</text><text x="254" y="90" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">Sunoで生成</text><text x="254" y="108" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">MP3ファイル</text><line x1="326" y1="80" x2="346" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh3)"/><rect x="348" y="35" width="140" height="90" fill="#f97316" rx="8"/><text x="418" y="68" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#fff" font-weight="bold">CapCut</text><text x="418" y="86" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fed7aa">クリップ結合</text><text x="418" y="102" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fed7aa">歌詞字幕追加</text><text x="418" y="118" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#fed7aa">カラーグレーディング</text><line x1="490" y1="80" x2="510" y2="80" stroke="#f97316" stroke-width="2" marker-end="url(#arh3)"/><rect x="512" y="40" width="270" height="80" fill="#1e293b" rx="8" stroke="#22c55e" stroke-width="2"/><text x="647" y="68" text-anchor="middle" font-family="sans-serif" font-size="13" fill="#34d399" font-weight="bold">完成MV（MP4）</text><text x="647" y="88" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#cbd5e1">1920×1080 / YouTube最適化</text><text x="647" y="106" text-anchor="middle" font-family="sans-serif" font-size="11" fill="#94a3b8">歌詞字幕・音楽シンク済み</text></svg><figcaption style="font-size:.82em;color:#64748b;margin-top:.4em;font-family:sans-serif;">図：CapCutでの最終仕上げフロー</figcaption></figure>

### CapCutでの基本作業手順

1. **新規プロジェクトを作成**（16:9 / 1920×1080で設定）
2. **音楽ファイルをインポート**（Sunoで生成したMP3）
3. **動画クリップをタイムラインに並べる**（Higgsfieldで生成したMP4を楽曲の区間に合わせて配置）
4. **字幕を追加する**
   - CapCutの「テキスト」→「自動字幕」機能で歌詞を自動生成
   - または「テキスト追加」で手動入力し、歌詞に合わせてタイミングを調整
5. **カラーグレーディング**（「フィルター」でシネマティックなトーンを加える）
6. **書き出し**（1080p / 60fps推奨。YouTubeアップロード用）

---

## STEP 5：YouTubeに投稿する

完成したMVをYouTubeにアップロードします。

**効果的な説明文の例（Claude Codeに作成を依頼できます）：**

```
このミュージックビデオは完全にAIツールで制作しました。

🎵 楽曲生成：Suno AI
🎬 映像生成：Higgsfield MCP（Seedance 2.0 / Kling 3.0）
✂️ 編集・字幕：CapCut
🤖 制作ディレクション：Claude Code

#AIミュージックビデオ #HiggsFieldAI #SunoAI #AI音楽 #DTM
```

---

## よくある質問

**Q. Higgsfield MCPは無料で使えますか？**

Higgsfield AIのアカウント作成は無料で、初回クレジットも付与されます。ただし動画生成にはクレジットが消費されます。本格的に使う場合は有料プランの検討が必要です。

**Q. 生成した動画・楽曲の著作権はどうなりますか？**

Higgsfield AIで生成した映像の権利は利用規約に準じます。商業利用の前に必ず各サービスの規約を確認してください。Suno AIは有料プランであれば商業利用・収益化が可能です。

**Q. 生成に失敗したり、思った通りの映像にならない場合は？**

プロンプトをより具体的に書き直すことで精度が上がります。Claude Codeに「このプロンプトを改善してください」と依頼すれば、修正案を提案してもらえます。

**Q. 1本のミュージックビデオを完成させるのにどれくらいかかりますか？**

慣れてくれば全工程で2〜3時間程度です。初回は設定・試行錯誤を含めて半日ほど見ておくと安心です。

---

<div style="margin:2rem 0;padding:1.2rem 1.5rem;background:#f5f3ff;border-left:4px solid #7c3aed;border-radius:8px;">
<p style="margin:0 0 .6rem;font-weight:bold;font-size:1rem;">&#x1F3AC; Higgsfield AI — AI動画生成プラットフォーム</p>
<p style="margin:0 0 .8rem;font-size:.92rem;color:#374151;">30以上のAIモデルをひとつのプラットフォームで利用可能。Sora・Kling・Veo・Seedance 2.0に対応。</p>
<a href="https://higgsfield.ai" rel="nofollow" target="_blank" referrerpolicy="no-referrer-when-downgrade" style="display:inline-block;background:#7c3aed;color:#fff;padding:.45rem 1.1rem;border-radius:4px;text-decoration:none;font-weight:bold;font-size:.95rem;">Higgsfield AIを試す →</a>
</div>

<div style="margin:2rem 0;padding:1.2rem 1.5rem;background:#fff7ed;border-left:4px solid #f97316;border-radius:8px;">
<p style="margin:0 0 .6rem;font-weight:bold;font-size:1rem;">&#x1F3B5; 楽天市場でDTM・録音機材をチェック</p>
<a href="https://search.rakuten.co.jp/search/mall/DTM+音楽制作/" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="display:inline-block;background:#bf0000;color:#fff;padding:.45rem 1.1rem;border-radius:4px;text-decoration:none;font-weight:bold;font-size:.95rem;">楽天市場でDTM機材を探す →</a>
</div>

<div style="margin:2rem 0;padding:1.2rem 1.5rem;background:#f0f9ff;border-left:4px solid #0ea5e9;border-radius:8px;">
<p style="margin:0 0 .6rem;font-weight:bold;font-size:1rem;">&#x1F3B8; サウンドハウスで音楽機材をチェック（国内最大の音楽機材専門店）</p>
<a href="https://h.accesstrade.net/sp/cc?rk=01001xqc00os63&url=https%3A%2F%2Fwww.soundhouse.co.jp%2Fsearch%2Findex%2F%3Fsearch_all%3DDTM" rel="nofollow" referrerpolicy="no-referrer-when-downgrade" style="display:inline-block;background:#0369a1;color:#fff;padding:.45rem 1.1rem;border-radius:4px;text-decoration:none;font-weight:bold;font-size:.95rem;">サウンドハウスで探す →</a>
<img src="https://h.accesstrade.net/sp/rr?rk=01001xqc00os63" width="1" height="1" border="0" alt="" loading="lazy">
</div>
