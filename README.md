# 🤍 1000人から1万円集める (DREAM KILLER KILLER)

> 涼晴に1万円払った1000人だけが入れる、優しいコミュニティ。
> 1000人 × ¥10,000 = ¥10,000,000 で涼晴の借金を完済。
> その日から、本当の経済が回り始める。

---

## 🌐 公開URL

| | |
|---|---|
| **LP本体** | https://imai-design.github.io/dream-killer-killer/ |
| **名簿ページ** | https://imai-design.github.io/dream-killer-killer/killers.html |
| **GitHubリポジトリ** | https://github.com/imai-design/dream-killer-killer |

---

## 📊 現状

| 項目 | 数値 |
|------|------|
| **KILLERS** | **3 / 1000** |
| 累計 | ¥30,000 |
| 借金完済まで残り | 997人 / ¥9,970,000 |
| 次の集会(第1回・10人)まで | あと7人 |
| 公開開始 | 2026-05-26 |

---

## 🎯 マイルストーン進捗

- [ ] **第1回集会** — 10人 (¥100,000)
- [ ] **第2回集会** — 20人 (¥200,000) · 二桁の壁
- [ ] **第3回集会** — 50人 (¥500,000) · 五十人
- [ ] **第4回集会** — 200人 (¥2,000,000) · 借金の1/5
- [ ] **第5回集会** — 500人 (¥5,000,000) · 半数到達
- [ ] **FINAL集会** — 1000人 (¥10,000,000) · 借金完済 · 人生リセット宣言

---

## 📂 プロジェクト構造

```
夢/2026-05-26 1000人から1万円集める (DREAM KILLER KILLER)/
├── README.md                       ← この索引
│
├── 📄 公開物（GitHub Pages）
│   ├── index.html                  ← LP本体（ふわふわ優しい1000人版）
│   ├── killers.html                ← 1000マス名簿ページ
│   ├── data/killers.json           ← メンバー名簿（公開可な最小情報）
│   └── audio/                      ← BGM（AAC 128kbps）
│       ├── 01.m4a                  ← 1曲目（ダーク版）
│       └── 02.m4a                  ← 2曲目（ダーク版）
│
├── 🎵 音楽プロンプト（ルート維持・[[音楽/README]] から横断索引）
│   ├── suno-prompt.md              ← Dark Trap版（既存BGM 1〜2曲目の元）
│   └── suno-prompt-gentle.md       ← The Kind 1000版（優しいlo-fi、3曲目候補）
│
├── 📁 管理/                        ← プロジェクト管理ドキュメント
│   ├── community-description.md    ← コミュニティ説明文 8形式
│   ├── voice-recording-guide.md    ← 殿の声をSuno Personaに学習させる手順
│   ├── 音楽プロンプト/             ← ルート音楽プロンプトへのシンボリックリンク
│   ├── 集会記録/                   ← 各マイルストーン集会の記録（将来）
│   └── メンバー名簿/               ← 機密扱いメンバー詳細（公開せず）
│
└── _wav_originals/                 ← 圧縮前wav退避（git無視）
```

---

## ⚙️ 編集ポイント（`index.html` 冒頭 CONFIG）

```js
const CONFIG = {
  PAYPAY_URL: "",                // ← PayPay請求リンク貼り込み
  LINE_INVITE_URL: "",           // ← LINEオプチャ招待URL貼り込み
  CURRENT_KILLERS: 3,            // ← 確定KILLER数（手動更新→push）
  MAX_KILLERS: 1000,
  PLEDGE_AMOUNT_JPY: 10000,
  MILESTONES: [10, 20, 50, 200, 500, 1000],
  AUDIO_PLAYLIST: ["audio/01.m4a","audio/02.m4a"],
  AUDIO_LOOP_PLAYLIST: true,
};
```

---

## 🔄 オペレーション

### 新メンバー追加時
1. `data/killers.json` の `killers` 配列に `{id, name, msg, date}` 追記
2. `index.html` の `CONFIG.CURRENT_KILLERS` を +1
3. `git add . && git commit -m "killers: N→N+1" && git push`
4. 30秒で本番反映 → 訪問者全員のLPでカウンタ・グリッド・マイルストーン更新
5. マイルストーン到達なら全訪問者に紙吹雪＋トースト発火（自動）

### 集会開催時
1. `管理/集会記録/第N回-YYYY-MM-DD-人数.md` 作成（写真・参加者・メッセージ）
2. このREADMEのマイルストーン進捗にチェック

### 新曲追加時
1. `音楽/YYYY-MM-DD タイトル.md` 作成（[[音楽/README]] テンプレ）
2. Sunoで生成、mp3を `audio/03.m4a` に配置
3. `CONFIG.AUDIO_PLAYLIST` に追記してpush

---

## 📋 教祖様お手元待ち

- [ ] **PayPay請求リンク**発行 → `CONFIG.PAYPAY_URL` に貼り込み
- [ ] **LINEオプチャ**「DREAM KILLER KILLER · 優しい1000人」作成 → `CONFIG.LINE_INVITE_URL` に貼り込み
- [ ] **Sunoでゲントル版生成**（[[管理/音楽プロンプト/suno-prompt-gentle]]、クリップボードに即貼れる状態）→ `audio/03.m4a` 配置
- [ ] **殿の声でPersona作成**したい場合 → [[管理/voice-recording-guide]]

---

## 🔗 関連

- [[音楽/README|🎵 音楽フォルダ全索引]]
- [[アイデア日記/INBOX/clipboard-history]] — 家来pbcopy履歴
- [[日記/2026-05-26]] / [[日記/2026-05-27]] — 構築履歴

---

## 📝 思想の核

> 信用もない、お金もない、今井涼晴を、
> それでも信じて¥10,000払ってくれた、いい人しかいない1000人。
> ここは、その人たちが集まる、優しい場所です。

- ブランド名「DREAM KILLER KILLER」は維持（外敵=夢を笑う声への姿勢）
- 内側のコミュニティは**ふわふわ・優しい・感謝**基調
- 「KILL」は外向、内側は「ありがとう」
- 借金完済を**正面から物語化**、隠さず・盛らず・事実で勝負

**EST. 2026-05-26 · TOKYO ↔ EVERYWHERE · 🤍 THE KIND 1000**
