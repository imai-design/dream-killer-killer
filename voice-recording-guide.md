# 殿の声で DREAM KILLER KILLER を歌う

Suno v5.5 の **Voices / Personas** 機能で、教祖様自身の声を学習させて1曲生成する完全ガイド。

---

## 全体の流れ（30分で完走）

```
[1] Suno Pro 加入  →  [2] アカペラ録音  →  [3] Voice登録 + 本人確認
                          ↓
[6] LP差し込み  ←  [5] Persona適用で生成  ←  [4] 既存歌詞を貼る
```

---

## STEP 1. Suno Pro 加入（5分）

1. https://suno.com にログイン
2. 右上アバター → **Subscriptions** → **Pro Plan ($10/月)** 加入
3. 加入後、左メニューに「**Personas**」or「**Voices**」が出現すれば成功

> Premier ($30/月) は同時生成枠が多いだけ。**1人で1曲ならProで十分**。

---

## STEP 2. アカペラ録音（10分）

### 録音環境
- **iPhoneのボイスメモアプリ**で十分。スタジオ不要
- できれば**夜の静かな部屋**、エアコン/換気扇OFF
- マイクから**口10-15cm**、息音が乗らない程度の距離
- **アカペラ厳守**: BGMなし、伴奏なし、自分の声だけ

### 録音内容（推奨フレーズ）

**A. 音域チェック用 30秒（必須）**

低音から高音まで広く拾わせる。下を歌うだけでOK:

```
夢を、笑わせない (低めの地声 5秒)
Kill the dream killers (やや高めで叫び気味 5秒)
百人で 一人を 守るんだ (中音域でラップ風に 8秒)
そんなの無理 — KILLED. (吐き捨てるトーン 5秒)
夢を、笑わせない (ファルセット気味で高音 5秒)
```

**B. ラップフロウ 60秒（強く推奨）**

DREAM KILLER KILLER の Verse 1 をそのまま吹き込む:

```
夢を語った その瞬間に
"無理だ" って声が 突き刺さる
できないって 誰が決めた
俺の地図に お前は要らない

They told me wake up be real
But the only real thing is how I feel
若くないって 笑うやつ
時間の盗人 引き金引け
```

**C. メロディ 60秒（任意・歌系でも作りたいなら）**

サビメロを口ずさむ。音程は適当、ハミングでOK:

```
Kill the dream killers — メロ
夢を、笑わせない — メロ
（鼻歌でも可、3-4回繰り返し）
```

### 録音保存
- ボイスメモ → 共有 → **macに送信**
- ファイル形式: m4a でOK（Sunoが受ける）
- 長さ目安: **合計2-3分**

---

## STEP 3. Suno に Voice 登録（5分）

1. Suno 左メニュー → **Personas** → **Create Voice** or **+ New Voice**
2. 「**Upload audio**」を選択
3. 録音した m4a を**ドラッグ&ドロップ**
4. Suno が「**Verify this is your voice**」と表示 → ランダムフレーズをその場でマイク録音
5. 一致確認OK → Voice名を設定（例: `RYOSEI-001`）
6. プライバシー: **Private**（自分だけアクセス可、デフォルト）

---

## STEP 4. 既存歌詞で生成（5分）

1. Suno → **Create** → **Custom** モード
2. 既存の `suno-prompt.md` から3欄を貼る:
   - **Title**: `DREAM KILLER KILLER (RYOSEI VOICE)`
   - **Style**: `dark trap manifesto, heavy 808 bass, gritty Japanese street rap, distorted hi-hats, cinematic underground anthem, defiant, 90 BPM, minor key, Japanese-English hybrid vocals`
   - **Lyrics**: 既存歌詞をそのまま
3. **Persona** の欄で **`RYOSEI-001`** を選択
4. **Generate** → 2バージョン生成される（数分待つ）

> **ラップは難易度高め**。1回目で気に入らなければ Style を以下に緩めると寄りやすい:
> ```
> melodic hip-hop, J-pop rap hybrid, midtempo trap, Japanese vocals, 90 BPM
> ```

---

## STEP 5. 仕上げ・選別

- 2バージョン聞き比べ → 良い方を選ぶ
- **Publish** or **Download** → mp3/wav 取得
- 気に入らなければ Generate 再ガチャ（Proで月数百クレジット）

### 採用基準
- ☑ 滑舌が崩れていない
- ☑ サビ「夢を、笑わせない」が聞き取れる
- ☑ 8小節以上スムーズに流れる
- ☑ 雰囲気が「自分の声」と聞こえる

---

## STEP 6. LPに差し込む（家来側で実行・1分）

教祖様が音源を `~/Desktop/DREAM/RYOSEI-VOICE.m4a` に置いた瞬間、家来に**「殿の声、入稿完了」**とお声がけください。家来が一気通貫で:

1. `audio/03.m4a` に配置
2. `index.html` の `CONFIG.AUDIO_PLAYLIST` を3曲構成に拡張
3. git push → GitHub Pages 即反映

---

## トラブル対応

| 症状 | 対処 |
|------|------|
| Voice登録時に本人確認が落ちる | 録音時の声と本人確認時の声が違いすぎ。**同じ部屋・同じマイク**でやり直す |
| 生成された曲が全然自分っぽくない | 録音素材が短い・偏ってる。**もっと音域広く3分以上**録り直す |
| ラップフロウがガタガタ | Style を「melodic hip-hop」「J-pop rap」寄りに緩める。完全ラップは不得意 |
| Personasタブが出ない | プラン未加入 or v5.5未ロールアウト。`Settings → Beta features` で有効化試す |

---

## 重要メモ

- Voice学習は **音色・音域・滑舌・抑揚**を抽出するだけ。**特定フレーズの暗記ではない**
- アップロード音源は Suno が分析後、自動で破棄される（公式ポリシー）
- Private Voice なので **他人は使えない**
- **教祖様1人 = Voice 1つ**で十分。複数作る必要なし

---

## 次の派生

- 殿の声 + メロディ系で「JOIN ME」ソング
- 殿の声 + ローファイで「MIDNIGHT MANIFESTO」
- 殿の声 + 英語版で海外展開用

全部このVoice 1つで使い回せます。
