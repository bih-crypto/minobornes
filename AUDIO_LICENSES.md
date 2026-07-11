# ミノボーンズ 音源ライセンス管理台帳

App Store 公開に向け、ゲーム内で使用する **すべての音源（BGM・効果音）** の権利を1件ずつ記録する台帳です。
音源を追加・差し替えるたびに、必ずこの表を更新してください。ゲーム内（？ボタン →「🎵 音源ライセンス一覧」）にも同じ台帳を表示できます。

---

## 現在の状態

- **BGM（場面別6種＋属性別4種）**: 外部の **CC0（パブリックドメイン相当）** 音源を使用（下表「導入済み BGM」）。すべて商用利用可・クレジット表記不要。`bgm/*.mp3` に配置し、ファイルが無い場面は従来の自作シンセ音へ自動フォールバック。
- **効果音（SE）**: 引き続き **WebAudio による自作合成音**（作者＝本プロジェクト、権利フリー、クレジット不要）。

| 用途 | タイトル | 作者 | ライセンス | 配布元URL | 商用利用 | クレジット表記 | 備考 |
|---|---|---|---|---|---|---|---|
| SE 全般 | 自作シンセ音（WebAudio合成） | 本プロジェクト | オリジナル（権利フリー） | – | 可 | 不要 | 効果音は自作合成のまま |

---

## 導入済み BGM（CC0・2026-07-11 導入）

すべて **CC0**（Creative Commons Zero / パブリックドメイン相当）。**商用利用可・クレジット表記不要**。各曲のライセンスは、配布元ページの CC0 表示および同梱 INFO.txt で **個別に確認済み**。

| ファイル | 場面 | 原曲 | 作者 | ライセンス | 配布元/ライセンス確認URL | 商用 | クレジット |
|---|---|---|---|---|---|---|---|
| bgm/title.mp3 | タイトル（かわいい/軽快） | Retro Game Music Pack – Title Screen | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/5-chiptunes-action | 可 | 不要 |
| bgm/dungeon.mp3 | 選択・マップ（探索） | Chiptune Adventures – Stage 1 | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/4-chiptunes-adventure | 可 | 不要 |
| bgm/battle.mp3 | 通常戦闘 | Retro Game Music Pack – Level 2 | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/5-chiptunes-action | 可 | 不要 |
| bgm/boss.mp3 | ボス戦（ダーク/緊迫） | Chiptune Adventures – Boss Fight | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/4-chiptunes-adventure | 可 | 不要 |
| bgm/victory.mp3 | クリア（明るい/壮大） | Retro Game Music Pack – Ending | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/5-chiptunes-action | 可 | 不要 |
| bgm/gameover.mp3 | ゲームオーバー（静かで重い） | Tragic ambient main menu (ambientmain_0) | brandon75689（投稿: HaelDB） | CC0（OGA-BY 3.0 とのデュアル／**CC0を選択適用**） | https://opengameart.org/content/tragic-ambient-main-menu | 可 | 不要 |
| bgm/battle_fire.mp3 | 属性戦闘・火（任意） | Retro Game Music Pack – Level 3 | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/5-chiptunes-action | 可 | 不要 |
| bgm/battle_water.mp3 | 属性戦闘・水（任意） | Chiptune Adventures – Stage 2 | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/4-chiptunes-adventure | 可 | 不要 |
| bgm/battle_wood.mp3 | 属性戦闘・木（任意） | Retro Game Music Pack – Level 1 | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/5-chiptunes-action | 可 | 不要 |
| bgm/battle_light.mp3 | 属性戦闘・光（任意） | Chiptune Adventures – Stage Select | Juhani Junkala (SubspaceAudio) | CC0 | https://opengameart.org/content/4-chiptunes-adventure | 可 | 不要 |

> **変換**: 原曲（WAV/OGG）を ffmpeg で mp3（192kbps / 44.1kHz / stereo）へ変換。CC0 のため改変・再配布に制約なし。
> **補足**: OpenGameArt の「5 Chiptunes (Action)」ページで配布される実ファイルは Juhani Junkala「Retro Game Music Pack」（Title Screen / Level 1–3 / Ending）。同梱 INFO.txt にも "released under CC0 creative commons license" と明記。
> **CITライセンス方針**: gameover 曲はデュアルライセンス（OGA-BY 3.0 / CC0）だが、本プロジェクトでは **CC0 の側を選択**して利用（クレジット不要）。

---

## フリー音源を導入する場合の手順（重要）

1. **CC0（パブリックドメイン相当）を最優先**で選ぶ。CC0なら商用利用可・クレジット不要で最も安全です。
2. CC-BY 等クレジット必須のものを使う場合は、**必ずアプリ内クレジット画面に表記**し、この表の「クレジット表記」を「要」にする。
3. **作品ごとにライセンスを個別確認**する。同じサイトでも作品によってライセンスが違うことがあります（特に Freesound）。
4. ダウンロード時のライセンス表記ページを**スクリーンショットで保管**しておく（後日の証跡用）。
5. 下の表に1行追加する。

### 追記フォーマット（コピーして使用）

```
| BGM（戦闘） | 曲名 | 作者名 | CC0 / CC-BY 4.0 等 | https://配布元URL | 可/不可 | 要/不要 | メモ |
```

---

## 導入候補の配布元（未導入・参考）

いずれも利用前に各作品のライセンスを必ず確認してください。

| 配布元 | URL | 主なライセンス | 商用 | クレジット | 備考 |
|---|---|---|---|---|---|
| Kenney.nl | https://kenney.nl/assets | CC0 | 可 | 不要 | ゲーム向けSE/音楽が豊富、CC0で安全 |
| OpenGameArt (CC0作品) | https://opengameart.org | 作品ごと（CC0作品を選択） | 作品による | 作品による | ライセンス絞り込み検索が可能 |
| Pixabay Music | https://pixabay.com/music/ | Pixabayコンテンツライセンス | 可 | 不要 | 商用可・クレジット不要（規約は要確認） |
| Freesound | https://freesound.org | 作品ごと（CC0のみ推奨） | 作品による | 作品による | CC0以外は要クレジット。個別確認必須 |
| DOVA-SYNDROME | https://dova-s.jp | 独自規約 | 多くは可 | 多くは不要 | 日本の定番。規約を各曲で確認 |
| 効果音ラボ | https://soundeffect-lab.info | 独自規約 | 可 | 不要 | 和風・ゲーム系SEが充実 |

---

## 注意事項

- **YouTube や無料まとめサイトからの音源は使用しない**（出典・権利が不明確なため）。
- 「フリー」という表記だけを信用せず、必ず**正式なライセンス文**を確認する。
- 音源のほか、**フォント**（現在 Google Fonts の Kiwi Maru / DotGothic16 = OFL、商用可）も同様に管理する。
- 絵文字は各プラットフォーム標準のものを使用しており、画像として再配布していないため通常は問題ありませんが、独自イラストに差し替えるとより安全かつ魅力的です。
