# 小巡救援任務 3D 遊戲

開著救援無人機「小巡」，和巡巡媽媽一起在雨林裡完成五關救援任務的 3D 小遊戲。純前端靜態網頁，用 [Three.js](https://threejs.org/) 繪製，手機和電腦都能玩。

**線上遊玩：** https://vicjuan.github.io/xiaoxun-rescue-game/

## 五個關卡

1. **森林火災**：用吊籃把樹上的小猴子送到對岸，灑水撲滅 4 個火點，水用完了就飛到河面補水。
2. **淹水**：飛到屋頂放下救生圈，再把救生艇引導到小屋。
3. **大風**：頂著強風飛回機庫躲風，風停後把鳥巢送回椰子樹上。
4. **土石流**：用熱成像找到受困的登山客，送急救包，再飛過綠色圓圈標出安全路線。
5. **地震**：飛到倒塌的小屋旁邊聽聲音找人，停在上方照明，讓媽媽吊開屋頂，最後飛回機庫。

## 操作方式

| 動作 | 手機 / 平板 | 電腦 |
| --- | --- | --- |
| 起飛 / 降落 | 綠色「起飛」按鈕（飛起來後變成紫色「降落」） | T 鍵 |
| 移動 | 拖動左下角搖桿 | 方向鍵或 WASD |
| 高度 | 畫面左邊中間的升降機：按住 ▲▼，或拖動中間的橘色把手 | R 上升、F 下降 |
| 快慢 | 畫面上方中間的直式滑桿：往上滑變快、往下滑變慢 | G 切換，或 1／2／3 |
| 灑水 | 按住藍色「灑水」 | 按住空白鍵 |
| 吊籃（吊起 / 放下） | 點橘色「吊籃」 | E 鍵或 Enter |

- 遊戲開始時小巡停在機庫的停機坪上，要先按「起飛」。
- 右上角的速度表顯示現在的速度（km/h），升降機下方顯示離地高度。
- 補水要飛到河面上 6 公尺以內；吊東西要飛得夠低，吊籃才勾得到。
- 躲風和最後回家都要飛到停機坪上方，自己按「降落」。水面上不能降落。

巡巡媽媽會用語音提示下一步，畫面上的黃色箭頭會指向目標。手機橫放比較好操作。

## 在 iPad 上當 App 玩

1. 用 iPad 的 Safari 打開 https://vicjuan.github.io/xiaoxun-rescue-game/
2. 點網址列旁的**分享**按鈕，選**「加入主畫面」**，再按「新增」。
3. 主畫面會出現小巡圖示，點開就是全螢幕遊戲。第一次打開後會存到 iPad 裡，之後沒網路也能玩。

iPhone 和 Android 也能用同樣的方式加入主畫面。

## 在本機執行

不需要安裝或建置，直接用瀏覽器開 `index.html`，或在專案資料夾啟動任一靜態伺服器：

```bash
python3 -m http.server 8000
# 打開 http://localhost:8000
```

需要網路連線來載入 Three.js（cdnjs）與 Google Fonts。

## 專案結構

```
index.html             遊戲本體（HTML、CSS、JavaScript 與語音都在同一個檔案）
manifest.webmanifest   主畫面 App 的名稱、圖示與全螢幕設定
sw.js                  離線快取（改版時把 VERSION 加一）
apple-touch-icon.png   iPad / iPhone 主畫面圖示
icons/                 其他尺寸的 App 圖示
.nojekyll              讓 GitHub Pages 直接提供靜態檔案
```

## 使用的開源資源

- [Three.js r128](https://github.com/mrdoob/three.js)（MIT）
- 巡巡媽媽的語音以 [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) 搭配 MeloTTS 中文模型離線合成
- 字型：Google Fonts 的 LXGW WenKai TC、Noto Sans TC
