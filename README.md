# TincleShotCode

TinCLE のショートコーディング作品集です。

ショートコーディングは、いわゆる「コードゴルフ」（バイト数の短さを競う遊び）です。「指定された行数で、動く完成品を書く」ことです。行数を決めて、その中にゲームを全部収める——その制約の中でどこまでやれるかを試しています。

## 作品

| ファイル | 行数 | 内容 |
|---|---|---|
| puzzle.c | 8行 | 落ちものパズル。12×20 の盤面、7種のピース、回転・ライン消去・ソフトドロップ対応 |
| rpg.c | 8行 | RPG。15×10 マップの探索、ランダムエンカウント戦闘、レベルアップ、ポーション、ボスを倒すとクリア |
| danmaku.js | 7行 | 弾幕STG「SPIRAL CAVERN」。螺旋弾幕のボス、WebAudio の効果音とBGM、HP半分で弾幕が濃くなる |

行数は物理行（ファイルの行数そのもの）で数えています。

## 操作

- **puzzle.c**: ←→ 移動 / ↑ 回転 / ↓ ソフトドロップ
- **rpg.c**: 矢印キー 移動 / 戦闘中は SPACE 攻撃、↓ ポーション / クリア・ゲームオーバー後は SPACE でリスタート
- **danmaku.js**: マウス・タッチ・矢印キー 移動（ショットは自動）/ SPACE・クリック 開始 / R・SPACE・クリック リスタート

## ビルドと実行

C の2本（puzzle.c / rpg.c）は、TinCLE 配布パッケージの構成（ソースの隣に `libs/` がある状態）でビルドします。Windows / Web の両対応です。

- Windows: `tinclec puzzle.exe puzzle.c`（rpg.c も同様）
- Web: emcass（TinCLE 公式の Web ビルド用ツール）でビルド

danmaku.js は、TinCLE の Web ページにある `tinclecanvas`（400×480）で動く前提のスクリプトです。単体で試す場合は、`<canvas id="tinclecanvas" width="400" height="480">` のあるページで読み込んでください。

## ライセンス

WTFPL（LICENSE.txt を参照してください）。

TinCLE
* **Official Website:** https://michyo.net/tincle/


---

# TincleShotCode (English)

A collection of TinCLE short-coding works.

Short-coding is "code golf" (the game of writing the shortest code in bytes). It means writing a finished, working product in a specified number of lines. Set the line count, fit the whole game inside it — and see how far you can get within that constraint.

## Works

| File | Lines | About |
|---|---|---|
| puzzle.c | 8 lines | Falling-block puzzle. 12×20 board, 7 piece types, rotation, line clears, soft drop |
| rpg.c | 8 lines | An RPG. Explore a 15×10 map, random-encounter battles, leveling up, potions, defeat the boss to clear the game |
| danmaku.js | 7 lines | Bullet-hell shooter "SPIRAL CAVERN". A spiral-barrage boss, WebAudio sound effects and BGM, patterns get denser below half HP |

Line counts are physical lines — the number of lines in the file itself.

## Controls

- **puzzle.c**: ←→ move / ↑ rotate / ↓ soft drop
- **rpg.c**: Arrow keys to move / in battle, SPACE attacks and ↓ uses a potion / after clearing or a game over, SPACE restarts
- **danmaku.js**: Mouse, touch, or arrow keys to move (firing is automatic) / SPACE or click to start / R, SPACE, or click to restart

## Building and running

The two C files (puzzle.c / rpg.c) build in the TinCLE distribution layout, with `libs/` next to the source. They support both Windows and Web.

- Windows: `tinclec puzzle.exe puzzle.c` (same for rpg.c)
- Web: build with emcass (TinCLE's official Web build tool)

danmaku.js is a script meant to run on the `tinclecanvas` element (400×480) of a TinCLE Web page. To try it on its own, load it in a page that has `<canvas id="tinclecanvas" width="400" height="480">`.

## License

WTFPL (see LICENSE.txt).

TinCLE
* **Official Website:** https://michyo.net/tincle/
