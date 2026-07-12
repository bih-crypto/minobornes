# 画像アセット配置ガイド（assets/）

ゲームの画像を入れるフォルダ一覧と、ファイル名の付け方をまとめた台帳です。
**画像は「画像優先・絵文字フォールバック」方式**で読み込まれます。該当する画像ファイルが存在すればそれを表示し、
無ければ従来どおり絵文字が表示されます（`onerror` フォールバック）。だから**段階的に差し替え**できます。

---

## 命名ルール（厳守）

- **半角小文字の英数字（a–z, 0–9）とアンダースコア（`_`）のみ**。
- **日本語・全角文字・スペース・記号は使わない**（URL・GitHub Pages で不具合の原因になる）。
- 拡張子は原則 **`.png`**（透過可）。写真的な背景で軽量化したい場合のみ `.jpg` も可。
- キー名（`garm`, `skeleton` など）は、ゲーム内部で各キャラ／敵／ピースに割り当てた**キーと一致**させること。
  - 例）キャラ「ガルム」の内部キーが `garm` なら、立ち絵は `garm.png`。
- ポーズ・状態違いは **`<key>_<状態>.png`** の形式（アンダースコア区切り）。

---

## フォルダ一覧と入れるもの

| フォルダ | 用途 | ファイル名の例 |
|---|---|---|
| `assets/chars/` | キャラの基本立ち絵（1キャラ1枚） | `garm.png` |
| `assets/chars/poses/` | 同キャラのポーズ・状態違い | `garm_attack.png` / `garm_damage.png` / `garm_win.png` / `garm_skill.png` |
| `assets/enemies/` | 敵キャラ。基本＋ポーズ違い | `skeleton.png` / `skeleton_attack.png` |
| `assets/pieces/` | 特殊パズルピース | `slime.png` / `thunder.png` / `curse_soil.png` |
| `assets/ui/` | UIアイコン（ステータス等） | `hp.png` / `mp.png` / `gold.png` / `soul.png` / `exp.png` |
| `assets/rings/` | 指輪 | `ring_fire.png` |
| `assets/equip/` | 装備品 | `sword.png` / `shield.png` |
| `assets/bg/` | 背景 | `forest.png` / `cave.png` / `volcano.png` |
| `assets/fx/` | エフェクト | `fire.png` / `heal.png` / `levelup.png` |

---

## ポーズ・状態の推奨サフィックス（chars/poses・enemies 共通）

| サフィックス | 意味 | 例 |
|---|---|---|
| `_attack` | 攻撃 | `garm_attack.png` |
| `_damage` | 被弾 | `garm_damage.png` |
| `_win` | 勝利 | `garm_win.png` |
| `_skill` | スキル／必殺技 | `garm_skill.png` |

> 基本立ち絵（サフィックス無し）が最優先。ポーズ画像は「あれば使う」拡張なので、
> まずは各キャラ／敵の基本1枚（`<key>.png`）から用意すると効率的です。

---

## 画像仕様の目安（任意・推奨）

- **形式**: PNG（透過）。背景は不透過でも可。
- **サイズ**: 立ち絵・敵は 512×512px 前後の正方形を推奨（表示側で縮小）。UIアイコンは 128×128px 程度。
- **軽さ**: Web配信のため1枚あたり数百KB以内を目安に。背景など大きい画像は `.jpg` 圧縮も検討。
- **余白**: 立ち絵はキャラを中央に、上下左右に少し余白を持たせると崩れにくい。

---

## 差し替えの流れ

1. 上表のフォルダに、命名ルールに沿った画像を置く。
2. `git add -A` → コミット → `git push origin main`。
3. GitHub Pages が数十秒で再デプロイ。該当キャラ／敵／アイコンが画像表示に切り替わる（未配置は絵文字のまま）。

> 各フォルダには空フォルダ保持用の `.gitkeep` を置いています。画像を追加したら `.gitkeep` は残しても削除しても構いません。
> ライセンスの記録が必要な素材（外部素材）は、リポジトリ直下の `AUDIO_LICENSES.md` と同様に権利を管理してください（自作画像なら不要）。
