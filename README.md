# TincleShotCode

TinCLE のショートコーディング作品集です。

ショートコーディングは、いわゆる「コードゴルフ」（バイト数の短さを競う遊び）です。「指定された行数で、動く完成品を書く」ことです。行数を決めて、その中にゲームを全部収める——その制約の中でどこまでやれるかを試しています。

## 作品

| ファイル | 行数 | 内容 |
|---|---|---|
| puzzle.c | 8行 | 落ちものパズル。12×20 の盤面、7種のピース、回転・ライン消去・ソフトドロップ対応 |
| rpg.c | 8行 | RPG。15×10 マップの探索、ランダムエンカウント戦闘、レベルアップ、ポーション、ボスを倒すとクリア |
| mysterypuzzle.c | 8行 | 謎解きアドベンチャー。一人称視点でクリックして移動・調査する。全5シーン。日記で見つけた3桁のコードで塔の扉を開け、星のクリスタルを目指す |
| danmaku.js | 7行 | 弾幕STG「SPIRAL CAVERN」。螺旋弾幕のボス、WebAudio の効果音とBGM、HP半分で弾幕が濃くなる |
| fps8.c | 8行 | レイキャストFPS。8×8の迷路を進み、追ってくる敵を撃つ。ESCAPEモードは5体撃破か出口到達でクリア、ENDLESSモードはスコアアタック |

行数は物理行（ファイルの行数そのもの）で数えています。

## 操作

- **puzzle.c**: ←→ 移動 / ↑ 回転 / ↓ ソフトドロップ
- **rpg.c**: 矢印キー 移動 / 戦闘中は SPACE 攻撃、↓ ポーション / クリア・ゲームオーバー後は SPACE でリスタート
- **mysterypuzzle.c**: マウス クリックで移動・調査（日記を読む／キーパッドのダイヤルを回す／扉を開ける）/ 下端クリックで戻る
- **danmaku.js**: マウス・タッチ・矢印キー 移動（ショットは自動）/ SPACE・クリック 開始 / R・SPACE・クリック リスタート
- **fps8.c**: ←→（A/D） 旋回 / ↑↓（W/S） 前進・後退 / SPACE・画面中央クリック 射撃 / タイトルで SPACE・左クリック ESCAPEモード、R・右クリック ENDLESSモード / マウスだけでも移動可

## ビルドと実行

C の4本（puzzle.c / rpg.c / mysterypuzzle.c / fps8.c）は、TinCLE 配布パッケージの構成（ソースの隣に `libs/` がある状態）でビルドします。Windows / Web の両対応です。

- Windows: `tinclec puzzle.exe puzzle.c`（rpg.c / mysterypuzzle.c / fps8.c も同様）
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
| mysterypuzzle.c | 8 lines | A first-person puzzle adventure. Click to move and examine across five scenes. Find a 3-digit code in a diary, open the tower door, and reach the star crystal |
| danmaku.js | 7 lines | Bullet-hell shooter "SPIRAL CAVERN". A spiral-barrage boss, WebAudio sound effects and BGM, patterns get denser below half HP |
| fps8.c | 8 lines | A raycasting FPS. Fight through an 8×8 maze against an enemy that hunts you down. ESCAPE mode: defeat 5 enemies or reach the exit to clear; ENDLESS mode: score attack |

Line counts are physical lines — the number of lines in the file itself.

## Controls

- **puzzle.c**: ←→ move / ↑ rotate / ↓ soft drop
- **rpg.c**: Arrow keys to move / in battle, SPACE attacks and ↓ uses a potion / after clearing or a game over, SPACE restarts
- **mysterypuzzle.c**: Mouse — click to move and examine (read the diary, turn the keypad dials, open the door) / click the bottom edge to step back
- **danmaku.js**: Mouse, touch, or arrow keys to move (firing is automatic) / SPACE or click to start / R, SPACE, or click to restart
- **fps8.c**: ←→ or A/D to turn / ↑↓ or W/S to move forward and back / SPACE or click the center of the screen to shoot / on the title screen, SPACE or left click for ESCAPE mode, R or right click for ENDLESS mode / mouse-only movement also works

## Building and running

The four C files (puzzle.c / rpg.c / mysterypuzzle.c / fps8.c) build in the TinCLE distribution layout, with `libs/` next to the source. They support both Windows and Web.

- Windows: `tinclec puzzle.exe puzzle.c` (same for rpg.c / mysterypuzzle.c / fps8.c)
- Web: build with emcass (TinCLE's official Web build tool)

danmaku.js is a script meant to run on the `tinclecanvas` element (400×480) of a TinCLE Web page. To try it on its own, load it in a page that has `<canvas id="tinclecanvas" width="400" height="480">`.

## License

WTFPL (see LICENSE.txt).

TinCLE
* **Official Website:** https://michyo.net/tincle/
