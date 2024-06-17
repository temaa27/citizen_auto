<br>

<div align="center">


  <h1 align="center">AutoBot для Catizen</h1>
  
  <p align="center">
    <strong>This script unlocks the "Auto" mode button in the game without requiring the cost of 3900 $Fish.</strong>
  </p>
 
</div>

## Возможности
- Auto-boost
- Auto-merge cats
- Auto-buy free cats
- Auto-delete low-level cats
- Auto-collect Airdrop Bonus


### Telegram Desktop on Windows and Linux
- Download and launch the **[Beta Version](https://desktop.telegram.org/changelog#beta-version)** of Telegram Desktop on Windows or Linux (not supported on Telegram Desktop for macOS yet).
- Go to Settings > Advanced > Experimental settings > Enable webview inspection.
- Right click in the WebView and choose Inspect.

## Запуск скрипта

Следуйте следующим шагам:

1. Откройте игру в Telegram Web App и нажмите **Ctrl + Shift+ I**.

2. Зайдите в источники **"Sources/Источники"** в web инспекторе.

3. Найдите файл **"bundle-*.js"**. Он находится в папке **"tgCat/game/cat/js"**.

4. Откройте файл **"bundle-*.js"** и через **Ctrl + F** найдите линию **L([A("leaguechange")], M.prototype, "updateBg", null),**.

5. Добавьте точку останова на этой линии. Можно сделать это слева от линни кода правой кнопкой или **F9**.

6. Обновите страницу, нажав **F5** на вашей клавиатуре.

7. Нажмите на **"Console"** сверху в панели. В консоль внизу страницы вставьте скопированный код и нажмите **Enter**.

```
const consoleRed = 'font-weight: bold; color: red;';
const consoleGreen = 'font-weight: bold; color: green;';
const consolePrefix = '%c [AutoBot] ';

console.clear()
console.log(`${consolePrefix}Injecting...`, consoleGreen);

try {
    function onClickAuto() {
        P.cat.isAuto = !P.cat.isAuto,
        P.cat.isAuto ? (this.ani8.play(0, !0),
        Laya.timer.loop(500, this, this.checkAuto),
        this.checkFreeCat(),
        this.m_btn_AutoSetting.visible = !0) : (Laya.timer.clearAll(this.checkAuto),
        this.ani8.stop(),
        Laya.timer.loop(5e3, this, this.checkSum),
        this.m_btn_AutoSetting.visible = !1),
        this.m_img_StopAuto.visible = !P.cat.isAuto
        u(`AutoBot ${P.cat.isAuto ? 'deactivated' : 'activated'}!\n\nCracked by @clqkx`)
    }
    
    M.prototype.onClickAuto = onClickAuto
    console.log(`${consolePrefix}Script loaded`, consoleGreen);
    console.log(`${consolePrefix}Crack by @clqkx`, consoleGreen);

} catch (e) {
    console.log(`${consolePrefix}An error occurred, the BrakePoint is set incorrectly!`, consoleRed);
    console.log(`${consolePrefix}Please follow the instructions, and you will succeed :*`, consoleRed);
    console.log('https://github.com/clqkx/AutoBot-Catizen');
}
```
8. Вернись в **"Источники"** сверху в панели. Запусти сценарий.

9. Зайди в игру и нажми **"Auto"**.
   
### Вот и всё! Теперь ты можешь бесплатно использовать Auto clicker в Catizen в Telegram.

