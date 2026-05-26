# Suno プロンプト — DREAM KILLER KILLER

Suno V4 Custom Mode で **上から順にコピペ** するだけ。生成後の mp3 URL を `index.html` 冒頭 `CONFIG.AUDIO_TRACK_URL` に差し込めば、LP本番BGMが即差し替わる。

---

## ▼ Title（タイトル欄）

```
DREAM KILLER KILLER
```

---

## ▼ Style of Music（スタイル欄 / Style of Music）

```
dark trap manifesto, heavy 808 bass, gritty Japanese street rap, distorted hi-hats, cinematic underground anthem, defiant, raw, Tokyo midnight, minor key, 90 BPM, glitchy intro, aggressive yet melodic, English-Japanese hybrid vocals, crowd chant outro
```

---

## ▼ Lyrics（歌詞欄）

```
[Intro - distorted whisper, sub bass swell]
夢を、笑わせない
Kill the dream killers
KILLED. KILLED. KILLED.

[Verse 1]
夢を語った その瞬間に
"無理だ" って声が 突き刺さる
できないって 誰が決めた
俺の地図に お前は要らない

They told me "wake up, be real"
But the only real thing is how I feel
若くないって 笑うやつ
時間の盗人 引き金引け

[Pre-Chorus - build, hi-hats roll]
Hands up, mic up, the dream is loaded
夢を笑う口を、塞げ

[Chorus - hard 808 drop]
Kill the dream killers
夢を、笑わせない
Kill the dream killers
百人で 一人を 守るんだ
KILLED. KILLED. KILLED.
夢を、笑わせない

[Verse 2]
百人 集めた あの夜から
分け合った金で 夢を回す
"千人" って盛りたい夜もある
でも 嘘はつかない 中身で殴る

We fund each other, we ride together
経済を 回せば 夢は続く
普通になれって? Nah, never
"普通" って言葉で 命を削るな

[Pre-Chorus]
Hands up, mic up, the dream is loaded
夢を笑う口を、塞げ

[Chorus]
Kill the dream killers
夢を、笑わせない
Kill the dream killers
百人で 一人を 守るんだ
KILLED. KILLED. KILLED.
夢を、笑わせない

[Bridge - quiet, almost spoken, beat strips back]
そんなの無理 — KILLED.
できるわけない — KILLED.
現実を見ろ — KILLED.
もう若くない — KILLED.
(beat drops, full band)

[Outro - crowd chant, fade]
Kill the dream killers
夢を、笑わせない
Kill the dream killers
夢を、笑わせない
(fade with chant)
```

---

## 使い方メモ

1. Suno (suno.com) → Create → **Custom** モードON
2. Title / Style of Music / Lyrics の3欄に上記をコピペ
3. Persona/Instrumental は OFF
4. Generate → 2バージョン出るので気に入った方を Publish
5. 出来上がった曲を右クリック → "Copy Audio URL"（または Download mp3 してホスティング）
6. `index.html` の冒頭:
   ```js
   const CONFIG = {
     AUDIO_TRACK_URL: "<ここに貼る>",
     ...
   };
   ```
7. リロード → サウンドトグルONで合成BGMの代わりに新曲が流れる

## 別バリエーション（気分で差し替え可）

### A. もっとアンセム / ロック寄り
```
gritty alt rock anthem, distorted guitars, driving drums, dark cinematic, defiant Japanese-English chant, midnight Tokyo skyline, 95 BPM, minor key, raw vocal energy
```

### B. もっとローファイ / 静かな反骨
```
lo-fi cinematic hip-hop, dusty piano loop, soft 808, smoky Japanese spoken-word verses, defiant whisper rap, 85 BPM, midnight neon mood, intimate underground
```

### C. もっと激しい / ハードコア
```
phonk x drill hybrid, distorted 808, aggressive Japanese drill flow, sirens, dark Tokyo underground, 140 BPM, half-time drop, gang vocal chant chorus, raw, unhinged
```
