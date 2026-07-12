# ミノボーンズ キャラクター画像 制作ガイド

生成AIでキャラ画像を1体ずつ作り、`assets/chars/` に置くだけでゲームに反映されます。
**画像が無いキャラは絵文字のまま**なので、1枚ずつ差し替えていけます。

---

## 1. 使い方（超重要・これだけ守れば動く）

1. リポジトリ（index.html と同じ階層）に **`assets/chars/`** フォルダを作る。
2. 下の一覧の **ファイル名（例 `garm.png`）** で画像を保存して入れる。
3. GitHub Pages に push すれば反映。iPhoneはSafariでリロード。

### 画像の仕様
- **形式：PNG（透過背景）** ／ 正方形（例 512×512 か 768×768）。
- **1体だけ**を中央に。影や地面は描かない（ゲーム側が台座の影を付けます）。
- キャラは**正面〜やや左向き**（味方は右の敵を向く構図になります）。
- 余白は上下左右に少し。顔・武器が端で切れないように。

---

## 2. 権利（App Store 配信前に必ず確認）

- 使う画像生成AIの規約で **商用利用可** かつ **生成物を自由に使える（帰属が自分/自由）** ことを確認。
- どのツールで作ったかを記録（`AUDIO_LICENSES.md` と同じ要領で管理を推奨）。
- 実在キャラ・既存作品に似せない（オリジナルとして作る）。

---

## 3. 共通プロンプト（トンマナを揃える土台）

各キャラの説明の前に、これを毎回付けると絵柄が揃います。日本語/英語どちらでも可。英語例：

```
A cute chibi RPG hero character, 2.5-head-tall proportions, hand-painted mobile-game art style,
soft rounded shapes, warm fantasy colors, gentle rim lighting, clean thick outline,
front view slightly turned left, full body standing pose, centered,
transparent background, no ground, no shadow, high detail, game asset, 512x512
```

日本語で使う場合の骨子：「かわいいデフォルメ2.5頭身のRPGキャラ、スマホゲーム風の手描きイラスト、丸みのある柔らかい形、暖色ファンタジー配色、リムライト、太めのクリーンな輪郭線、正面やや左向きの全身立ちポーズ、中央配置、**透過背景・影なし・地面なし**、ゲームアセット」。

各キャラは、この後ろに「■個別」の一文を足すだけ。

---

## 4. キャラ一覧とファイル名

各行：キャラ名 / 保存ファイル名 / 属性 / 職業 / 現在の絵文字（雰囲気の参考）。
属性の色 → 火=暖色/赤橙、水=青、木=緑、光=金/白。職業で装いを変えると個性が出ます
（戦士=剣鎧／魔法使い=杖ローブ／弓使い=弓／盗賊=軽装短剣／僧侶=聖職者/杖／守護=盾・重装）。

### 主人公クラス（開始時に名前を入力して選ぶ／ローグライクの起点）
プレイヤーが入力する「名前」はゲーム内表示のみ。画像ファイル名は**クラス名ベース**（下記）。
通常のほか poses/ に攻撃・ダメージ・勝利ポーズを置けます（例 `hero_knight_attack.png`）。

| クラス名 | ファイル名 | 属性 | 職業 | 参考絵文字 |
|---|---|---|---|---|
| 焔の剣士 | `assets/chars/hero_knight.png` | 火 | 戦士 | ⚔️ |
| 碧の魔道士 | `assets/chars/hero_mage.png` | 水 | 魔法使い | 🪄 |
| 翠の狩人 | `assets/chars/hero_hunter.png` | 木 | 弓使い | 🏹 |
| 聖の神官 | `assets/chars/hero_cleric.png` | 光 | 僧侶 | ✨ |

### 仲間（旧・初期キャラ4体もここへ合流）
| キャラ名 | ファイル名 | 属性 | 職業 | 参考絵文字 |
|---|---|---|---|---|
| 焔狼ガルム | `assets/chars/garm.png` | 火 | 戦士 | 🐺 |
| 水霊アクア | `assets/chars/aqua.png` | 水 | 僧侶 | 💧 |
| 森鹿シルワ | `assets/chars/silva.png` | 木 | 守護 | 🦌 |
| 聖鳥ルクス | `assets/chars/lux.png` | 光 | 魔法使い | 🕊️ |

### 仲間
| キャラ名 | ファイル名 | 属性 | 職業 | 参考絵文字 |
|---|---|---|---|---|
| 骨剣士スケルド | `assets/chars/skeld.png` | 火 | 戦士 | 💀 |
| 血蝙蝠ヴァンピ | `assets/chars/vampi.png` | 火 | 盗賊 | 🦇 |
| 竜児ドラコ | `assets/chars/draco.png` | 火 | 魔法使い | 🐲 |
| 不死鳥フェニ | `assets/chars/pheni.png` | 火 | 僧侶 | 🐦‍🔥 |
| 魔導リッチ | `assets/chars/lich.png` | 水 | 魔法使い | 🧙 |
| 雪女ユキメ | `assets/chars/yukime.png` | 水 | 魔法使い | ❄️ |
| 大蛸クラーケ | `assets/chars/krake.png` | 水 | 守護 | 🐙 |
| 苔亀ゴメス | `assets/chars/gomes.png` | 木 | 守護 | 🐢 |
| 妖精ピクス | `assets/chars/pixy.png` | 木 | 弓使い | 🧚 |
| 宝魔ミミック | `assets/chars/mimic.png` | 木 | 盗賊 | 📦 |
| 雷猫ボルニャ | `assets/chars/bolnya.png` | 光 | 弓使い | 🐱 |
| 天馬ペガロ | `assets/chars/pegaro.png` | 光 | 僧侶 | 🦄 |
| 影猫カゲロウ | `assets/chars/kagerou.png` | 水 | 盗賊 | 🐈‍⬛ |
| 鍛冶鬼カジン | `assets/chars/kajin.png` | 火 | 戦士 | 🔨 |
| 歌姫セイレン | `assets/chars/seiren.png` | 水 | 僧侶 | 🧜‍♀️ |
| 大神ハクレイ | `assets/chars/hakurei.png` | 光 | 弓使い | 🐕 |

### ガチャ限定UR（気合を入れたい看板キャラ）
| キャラ名 | ファイル名 | 属性 | 職業 | 参考絵文字 |
|---|---|---|---|---|
| 時の女神クロノア | `assets/chars/chronoa.png` | 光 | 魔法使い | 🧝‍♀️ |
| 魔王ベビゴン | `assets/chars/bebigon.png` | 火 | 戦士 | 😈 |
| 織姫スピカ | `assets/chars/spica.png` | 光 | 僧侶 | 🌟 |
| 骨神ミノカミ | `assets/chars/minokami.png` | 木 | 守護 | 🦴 |

### ボス（例として2体を実装済み。敵は少し大きめ・威圧的に）
| キャラ名 | ファイル名 | 属性 | 参考絵文字 |
|---|---|---|---|
| 迷宮の看守グレイヴ | `assets/chars/boss_grave.png` | 光 | ⚰️（重騎士） |
| 屍竜バリドボーン | `assets/chars/boss_baridborn.png` | 火 | 🐉 |

> 通常敵にも画像を付けたい場合は、敵データに `img:'ファイル名'` を足せば同じ仕組みで反映できます。必要になったら追加します。

---

## 5. 個別プロンプト例（主人公候補）

**焔狼ガルム（火・戦士）**：
```
（共通プロンプト）+ a brave wolf-beastman warrior boy, orange-red fur, wearing light
leather-and-steel armor with a warm-colored scarf, holding a short sword, confident friendly face
```

**水霊アクア（水・僧侶）**：
```
（共通プロンプト）+ a gentle blue water-spirit priestess, flowing aqua robe, holding a staff
with a water droplet gem, calm kind expression, soft blue glow
```

**森鹿シルワ（木・守護）**：
```
（共通プロンプト）+ a sturdy deer guardian, green nature-themed heavy armor with leaf motifs,
holding a big round shield, gentle strong presence
```

**聖鳥ルクス（光・魔法使い）**：
```
（共通プロンプト）+ a small holy bird mage, white and gold feathers, tiny wizard hat and cape,
holding a glowing golden staff, sparkles of light
```

あとは一覧の「属性＋職業＋名前の雰囲気」を同じ要領で一文にすれば量産できます。

---

## 6. 進め方のおすすめ

1. まず**主人公候補4体**を作る（最初に見える顔なので効果大）。
2. 次に**ガチャUR4体**（看板キャラ）とよく使う仲間。
3. 次に**ボス**。
4. 一体できるたびに置いて確認 → 絵柄が浮いたら共通プロンプトを微調整。

絵柄が固まってきたら、背景（階層ごとの一枚絵）と盤面ブロックの作り込みへ進みます。
