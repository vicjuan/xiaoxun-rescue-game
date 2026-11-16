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
| 移動 | 拖動左下角搖桿 | 方向鍵或 WASD |
| 灑水 | 按住藍色「灑水」 | 按住空白鍵 |
| 吊籃（吊起 / 放下） | 點橘色「吊籃」 | E 鍵或 Enter |
| 補水 | 飛到河面上自動補水 | 同左 |

巡巡媽媽會用語音提示下一步，畫面上的黃色箭頭會指向目標。手機橫放比較好操作。

## 在本機執行

不需要安裝或建置，直接用瀏覽器開 `index.html`，或在專案資料夾啟動任一靜態伺服器：

```bash
python3 -m http.server 8000
# 打開 http://localhost:8000
```

需要網路連線來載入 Three.js（cdnjs）與 Google Fonts。

## 專案結構

```
index.html   遊戲本體（HTML、CSS、JavaScript 與語音都在同一個檔案）
.nojekyll    讓 GitHub Pages 直接提供靜態檔案
```

## 使用的開源資源

- [Three.js r128](https://github.com/mrdoob/three.js)（MIT）
- 巡巡媽媽的語音以 [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) 搭配 MeloTTS 中文模型離線合成
- 字型：Google Fonts 的 LXGW WenKai TC、Noto Sans TC
