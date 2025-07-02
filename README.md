# buttplugmod_SecretFlasherManaka

# Mod Tested MelonLoader v0.7.1 Open-Beta
# ----------------------------------------------
# Easy Start
## First 
### SecretFlasherManaka install MelonLoader v0.7.1
### Run game 
### Initialized
### Exit
## Second 
### Unzip decompressiontoMods.7z to Mods directory "SecretFlasherManaka/Mods/"
## Finanly
### Run game
### Enjoy it
# ----------------------------------------------

# 簡単な手順
## まず
### SecretFlasherManaka に MelonLoader v0.7.1 をインストールします。
### ゲームを起動します。
### 初期化されました。
### 終了します。  

## 次に
### decomprestoMods.7z を解凍して、「SecretFlasherManaka/Mods/」ディレクトリにコピーします。
## 最後に
### ゲームを起動します。
### お楽しみください。  
# ----------------------------------------------

# 简易步骤
## 第一步
### 将 SecretFlasherManaka 安装 MelonLoader v0.7.1
### 运行游戏
### 初始化完成
### 退出  

## 第二步
### 将 decompresstoMods.7z 解压到 "SecretFlasherManaka/Mods/" 目录
## 最后
### 运行游戏
### 享受游戏吧！

# ----------------------------------------------

# VibeSync Mod User Manual

## VibeSync Mod v3.8.5


---

## 1. Introduction

VibeSync Mod is a MelonLoader module designed to dynamically synchronize your Buttplug compatible devices (such as Lovense toys) with in-game states through the Buttplug.io framework. It intelligently adjusts vibration patterns and intensities based on your heart rate, the game character's "VibeState," and the "Ecstasy Gauge" fill amount, providing an immersive and interactive experience.

## 2. Key Features

*   **Dynamic Vibration Sync:** Dynamically adjusts vibration intensity and mode based on real-time in-game data: heart rate, VibeState (low/high vibration), and Ecstasy Gauge fill.
*   **Diverse Vibration Modes:** Offers various preset vibration patterns including wave-like (Low Wave / High Wave), intermittent (Low Intermittent / High Intermittent), and hybrid (Low Hybrid / High Hybrid) modes.
*   **Intelligent Climax Mode:** Automatically triggers intense climax vibration when the in-game Ecstasy Gauge meets specific conditions, distinguishing between "Minor Climaxes" and more intense "Major Climaxes" based on accumulated progress.
*   **Configurable Cooldown Durations:** Features independent, customizable no-vibration cooldown periods after Minor and Major Climaxes, helping you recover. These cooldowns are intelligently cut into smaller commands for smoother control.
*   **Multi-Motor Staggered Vibration:** If your device has multiple vibration motors, the mod can achieve a staggered effect where intensity progressively transfers between motors, creating richer and more engaging vibration patterns.
*   **Real-time Control & Debugging:** Provides in-game hotkeys for convenient connection/disconnection from the Buttplug server and toggling detailed log output.
*   **Highly Customizable:** All key parameters can be adjusted via an external JSON configuration file to suit your personal preferences and device characteristics.

## 3. Installation Guide

1.  **Install MelonLoader:** Ensure you have successfully installed MelonLoader for your game according to the official MelonLoader guide.
2.  **Download Intiface Central:** VibeSync Mod requires the Buttplug.io Intiface Central application to act as a bridge between your Buttplug device(s) and the mod. Please download and install Intiface Central from the official Buttplug.io website.
3.  **Download VibeSync Mod:** Download the `VibeSyncMod.dll` file and the `vibe_config.json` file to your computer.
4.  **Deploy Mod Files:** Place the downloaded `VibeSyncMod.dll` and `vibe_config.json` files into the `Mods` folder located in your game's root directory. If the `Mods` folder does not exist, create it manually.
    *   Example Path: `YourGameFolder/Mods/VibeSyncMod.dll`
    *   Example Path: `YourGameFolder/Mods/vibe_config.json`
5.  **Start Intiface Central:** Before launching the game, ensure that Intiface Central is running and your Buttplug device(s) are connected and recognized by Intiface Central.

## 4. How to Use

1.  **Launch the game.**
2.  **Connect to Buttplug Server:** In-game, press the **`=` (Equals) key** on your keyboard. You will see connection attempts and results in the MelonLoader console. If successful, your device may provide a brief vibration feedback.
3.  **Disconnect from Buttplug Server:** Press the **`=` (Equals) key** again. Your device will stop vibrating and disconnect.
4.  **Toggle Detailed Logs:** In-game, press the **`-` (Minus) key** on your keyboard. This will toggle the display of detailed debug logs in the MelonLoader console. Enabling verbose logs can help you understand the mod's internal workings and troubleshoot issues.
5.  **Experience Dynamic Vibration:** The mod will automatically start and adjust your device's vibration based on real-time changes in your in-game heart rate, VibeState, and Ecstasy Gauge.

## 5. Configuration File (`vibe_config.json`) Explanation

The `vibe_config.json` file allows you to customize the mod's behavior. You can open and edit it using any text editor (e.g., Notepad, Notepad++, VS Code).

**Important Note:** It's best to close the game before editing the configuration file. If you modify the file while the game is running, you'll need to restart the game or reconnect the mod (press `=` key twice) for the changes to take effect.

```json
{
  "ButtplugServerUri": "ws://127.0.0.1:12345",
  "ConnectKey": "Equals",
  "LogToggleKey": "Minus",
  "EnableVerboseLogging": true,
  "EnableHeartRateDebugLog": false,

  "ClimaxVibrationDuration": 0.4,
  "ClimaxPauseDuration": 0.4,
  "ClimaxMaxIntensityLevel": 20.0,
  
  "LowVibeClimaxBaseCycles": 5,
  "LowVibeClimaxMaxAccumulatedCycles": 25,
  "HighVibeClimaxBaseCycles": 10,
  "HighVibeClimaxMaxAccumulatedCycles": 50,
  
  "MajorClimaxTriggerCount": 3,
  
  "MinorClimaxCooldownDuration": 5.0,
  "MajorClimaxCooldownDuration": 10.0,
  "MotorStaggerDuration": 0.01
}
```

### Parameter Details:

#### 5.1. General Settings

*   `ButtplugServerUri` (String):
    *   The WebSocket address of the Buttplug server (e.g., Intiface Central).
    *   **Default:** `"ws://127.0.0.1:12345"`
    *   **Recommendation:** Usually no need to change, unless you've configured Intiface Central to use a different port or run on a different computer.
*   `ConnectKey` (String):
    *   The keyboard key used to connect/disconnect from the Buttplug server.
    *   **Default:** `"Equals"` (corresponds to the `=` key on most keyboards)
    *   **Options:** Any string representation of a Unity `KeyCode` enum, e.g., `"C"`, `"Space"`, `"Return"`, etc.
*   `LogToggleKey` (String):
    *   The keyboard key used to toggle detailed log output in the MelonLoader console.
    *   **Default:** `"Minus"` (corresponds to the `-` key on most keyboards)
    *   **Options:** Any string representation of a Unity `KeyCode` enum, e.g., `"K"`, `"L"`, etc.
*   `EnableVerboseLogging` (Boolean):
    *   Whether to enable very detailed debug logs in the MelonLoader console.
    *   **Default:** `true`
    *   **Recommendation:** Set to `true` for troubleshooting, `false` for regular gameplay to reduce log clutter.
*   `EnableHeartRateDebugLog` (Boolean):
    *   Whether to output a periodic (every 3 seconds) debug log of heart rate, Ecstasy Gauge, and current vibration state to the console.
    *   **Default:** `false`
    *   **Recommendation:** Only set to `true` if you want to observe how the mod reacts to game states.

#### 5.2. Climax Mode Settings

*   `ClimaxVibrationDuration` (Float):
    *   In Climax mode, the duration (in seconds) of each "on" vibration pulse.
    *   **Default:** `0.4`
*   `ClimaxPauseDuration` (Float):
    *   In Climax mode, the duration (in seconds) of each "off" pause between vibration pulses.
    *   **Default:** `0.4`
*   `ClimaxMaxIntensityLevel` (Float):
    *   The maximum vibration intensity level (0-20 scale) used during Climax mode.
    *   **Default:** `20.0` (maximum intensity)
*   `LowVibeClimaxBaseCycles` (Integer):
    *   When the game's VibeState is "Low", the base number of vibration cycles for a Climax (applies to Minor Climaxes or the base part of Major Climaxes).
    *   **Default:** `5`
*   `LowVibeClimaxMaxAccumulatedCycles` (Integer):
    *   When the game's VibeState is "Low", the maximum number of additional climax vibration cycles that can be accumulated through heart rate.
    *   **Default:** `25`
*   `HighVibeClimaxBaseCycles` (Integer):
    *   When the game's VibeState is "High", the base number of vibration cycles for a Climax.
    *   **Default:** `10`
*   `HighVibeClimaxMaxAccumulatedCycles` (Integer):
    *   When the game's VibeState is "High", the maximum number of additional climax vibration cycles that can be accumulated through heart rate.
    *   **Default:** `50`
*   `MajorClimaxTriggerCount` (Integer):
    *   The number of accumulated "Minor Climaxes" required to trigger a "Major Climax" (if a climax is triggered again). For example, a value of `3` means after 3 Minor Climaxes, the next triggered climax will be a Major Climax.
    *   **Default:** `3`

#### 5.3. Climax Cooldown & Motor Behavior Settings

*   `MinorClimaxCooldownDuration` (Float):
    *   The duration (in seconds) of the no-vibration cooldown period after a "Minor Climax" finishes. This duration is intelligently split into multiple 1-second (or remaining fraction) silent commands by the mod for consistent control.
    *   **Default:** `5.0`
*   `MajorClimaxCooldownDuration` (Float):
    *   The duration (in seconds) of the no-vibration cooldown period after a "Major Climax" finishes. Similarly split into smaller commands.
    *   **Default:** `10.0`
*   `MotorStaggerDuration` (Float):
    *   This parameter controls the tiny time offset (in seconds) for intensity changes between multiple motors on a device, both during active patterns and when gradually ramping down to zero. It creates a wave-like or ripple effect in the vibration.
    *   **Default:** `0.01`
    *   **Recommendation:** Keep this value small for a smooth staggered effect. Setting it too high might make vibration patterns feel choppy. This setting has no effect on single-motor devices.

## 6. Troubleshooting

*   **Mod Not Loading:**
    *   Ensure `VibeSyncMod.dll` and `vibe_config.json` are correctly placed in your game's `Mods` folder.
    *   Check the MelonLoader console for any error messages.
*   **Cannot Connect to Buttplug Server (pressing `=` key does nothing or gives an error):**
    *   Make sure the Intiface Central application is running on your computer.
    *   Verify Intiface Central's settings: ensure the WebSocket server is enabled and its port matches `ButtplugServerUri` in `vibe_config.json` (default: `12345`).
    *   Check your firewall settings to ensure they are not blocking communication between the game and `127.0.0.1:12345` (or your configured address).
    *   Try restarting both Intiface Central and the game.
*   **Device Connected but No Vibration:**
    *   Confirm your device is connected and working correctly within Intiface Central. Try manually controlling vibration in Intiface Central to see if the device responds.
    *   In-game, press the `-` key to enable detailed logs and look for warnings like "No vibrating device available" or "Invalid motor index".
    *   Check if your in-game character's heart rate is within the 90-160 BPM range, and if the VibeState is "Low" or "High" (not "Off"). The mod only activates within these parameters.
*   **Vibration Patterns Not as Expected:**
    *   Enable `EnableHeartRateDebugLog` (`true`) and press the `-` key in-game. Observe the detailed state log every 3 seconds. This will show current heart rate, Ecstasy Gauge, VibeState, and the exact vibration instructions the mod is trying to execute. Compare this information with your expectations.
    *   Adjust various parameters in `vibe_config.json`, especially intensity and time-related settings, and Climax mode configurations.
*   **Game Stuttering or Performance Degradation:**
    *   Set `EnableVerboseLogging` and `EnableHeartRateDebugLog` to `false` to reduce log output.
    *   If `MotorStaggerDuration` was accidentally set too high, lower its value.
    *   While multi-motor devices can slightly increase processing, Buttplug protocol is generally efficient.

If you encounter issues that you cannot resolve, please provide the full MelonLoader console log to the mod's support channel (if available).

---

Thank you for using VibeSync Mod. We hope it enhances your gaming experience!

---
---

# VibeSync Mod ユーザーマニュアル

## VibeSync Mod v3.8.5

---

## 1. はじめに

VibeSync Mod は、MelonLoader 用のモジュールで、Buttplug.io フレームワークを介して、Buttplug 互換デバイス（Lovense 製玩具など）の振動をゲーム内の特定の状態と動的に同期させることを目的としています。心拍数、ゲームキャラクターの「VibeState」（振動状態）、および「Ecstasy Gauge」（エクスタシーゲージ）の充填量に基づいて振動パターンと強度をインテリジェントに調整し、没入型でインタラクティブな体験を提供します。

## 2. 主な機能

*   **動的振動同期:** ゲーム内のリアルタイムデータ（心拍数、VibeState（低振動/高振動）、エクスタシーゲージの充填量）に基づいて、振動強度とモードを動的に調整します。
*   **多様な振動モード:** 波状（Low Wave / High Wave）、断続的（Low Intermittent / High Intermittent）、ハイブリッド（Low Hybrid / High Hybrid）など、様々なプリセット振動パターンを提供します。
*   **インテリジェントなクライマックスモード:** ゲーム内のエクスタシーゲージが特定の条件を満たした場合、激しいクライマックス振動モードを自動的にトリガーし、蓄積された進行状況に基づいて「小クライマックス」とより激しい「大クライマックス」を区別します。
*   **設定可能なクールダウン時間:** 小クライマックスおよび大クライマックス終了後には、独立してカスタマイズ可能な無振動クールダウン期間が設けられており、回復を助けます。これらのクールダウンは、よりスムーズな制御のためにインテリジェントに短いコマンドに分割されます。
*   **多モーター千鳥振動:** お使いのデバイスが複数の振動モーターを備えている場合、Mod はモーター間で強度が段階的に伝わる千鳥効果を実現し、より豊かで魅力的な振動パターンを作り出します。
*   **リアルタイム制御とデバッグ:** Buttplug サーバーへの接続/切断、および詳細なログ出力の切り替えを便利に行うためのゲーム内ホットキーを提供します。
*   **高度なカスタマイズ性:** すべての主要なパラメータは、外部の JSON 設定ファイルを通じて調整でき、個人の好みやデバイスの特性に合わせて設定できます。

## 3. インストールガイド

1.  **MelonLoader のインストール:** MelonLoader の公式ガイドに従って、ゲームに MelonLoader が正常にインストールされていることを確認してください。
2.  **Intiface Central のダウンロード:** VibeSync Mod は、Buttplug デバイスと Mod の間の橋渡し役として、Buttplug.io の Intiface Central アプリケーションを必要とします。Buttplug.io 公式ウェブサイトから Intiface Central をダウンロードしてインストールしてください。
3.  **VibeSync Mod のダウンロード:** `VibeSyncMod.dll` ファイルと `vibe_config.json` ファイルをコンピューターにダウンロードします。
4.  **Mod ファイルの展開:** ダウンロードした `VibeSyncMod.dll` と `vibe_config.json` ファイルを、ゲームのルートディレクトリにある `Mods` フォルダに配置します。`Mods` フォルダが存在しない場合は、手動で作成してください。
    *   例パス: `YourGameFolder/Mods/VibeSyncMod.dll`
    *   例パス: `YourGameFolder/Mods/vibe_config.json`
5.  **Intiface Central の起動:** ゲームを起動する前に、Intiface Central が実行されており、Buttplug デバイスが接続され、Intiface Central に認識されていることを確認してください。

## 4. 使用方法

1.  **ゲームを起動します。**
2.  **Buttplug サーバーに接続:** ゲーム内でキーボードの **`=` (イコール) キー** を押します。MelonLoader コンソールに接続試行と結果の情報が表示されます。接続が成功すると、デバイスから短い振動フィードバックがある場合があります。
3.  **Buttplug サーバーから切断:** もう一度 **`=` (イコール) キー** を押します。デバイスは振動を停止し、切断されます。
4.  **詳細ログの切り替え:** ゲーム内でキーボードの **`-` (マイナス) キー** を押します。これにより、MelonLoader コンソールに詳細なデバッグログを表示するかどうかが切り替わります。詳細ログを有効にすると、Mod の内部動作を理解し、問題のトラブルシューティングに役立ちます。
5.  **動的振動を体験:** Mod は、ゲーム内の心拍数、VibeState、およびエクスタシーゲージのリアルタイムの変化に基づいて、デバイスの振動を自動的に開始および調整します。

## 5. 設定ファイル (`vibe_config.json`) の説明

`vibe_config.json` ファイルを使用すると、Mod の動作をカスタマイズできます。任意のテキストエディタ（例: メモ帳、Notepad++、VS Code）で開いて編集できます。

**重要:** 設定ファイルを編集する前に、ゲームを終了することをお勧めします。ゲームの実行中にファイルを変更した場合、変更を有効にするにはゲームを再起動するか、Mod を再接続（`=` キーを2回押す）する必要があります。

```json
{
  "ButtplugServerUri": "ws://127.0.0.1:12345",
  "ConnectKey": "Equals",
  "LogToggleKey": "Minus",
  "EnableVerboseLogging": true,
  "EnableHeartRateDebugLog": false,

  "ClimaxVibrationDuration": 0.4,
  "ClimaxPauseDuration": 0.4,
  "ClimaxMaxIntensityLevel": 20.0,
  
  "LowVibeClimaxBaseCycles": 5,
  "LowVibeClimaxMaxAccumulatedCycles": 25,
  "HighVibeClimaxBaseCycles": 10,
  "HighVibeClimaxMaxAccumulatedCycles": 50,
  
  "MajorClimaxTriggerCount": 3,
  
  "MinorClimaxCooldownDuration": 5.0,
  "MajorClimaxCooldownDuration": 10.0,
  "MotorStaggerDuration": 0.01
}
```

### パラメータ詳細:

#### 5.1. 一般設定

*   `ButtplugServerUri` (文字列):
    *   Buttplug サーバー（例: Intiface Central）の WebSocket アドレス。
    *   **デフォルト:** `"ws://127.0.0.1:12345"`
    *   **推奨:** Intiface Central を別のポートを使用するように設定した場合や、別のコンピューターで実行している場合を除き、通常は変更する必要はありません。
*   `ConnectKey` (文字列):
    *   Buttplug サーバーに接続/切断するために使用するキーボードのキー。
    *   **デフォルト:** `"Equals"` (ほとんどのキーボードの `=` キーに対応)
    *   **オプション:** Unity `KeyCode` 列挙型の文字列表現（例: `"C"`、`"Space"`、`"Return"` など）。
*   `LogToggleKey` (文字列):
    *   MelonLoader コンソールでの詳細ログ出力の表示を切り替えるために使用するキーボードのキー。
    *   **デフォルト:** `"Minus"` (ほとんどのキーボードの `-` キーに対応)
    *   **オプション:** Unity `KeyCode` 列挙型の文字列表現（例: `"K"`、`"L"` など）。
*   `EnableVerboseLogging` (ブール値):
    *   MelonLoader コンソールに非常に詳細なデバッグログを出力するかどうか。
    *   **デフォルト:** `true`
    *   **推奨:** 問題のトラブルシューティング時には `true` に設定し、通常のプレイ時にはログの量を減らすために `false` に設定できます。
*   `EnableHeartRateDebugLog` (ブール値):
    *   心拍数、エクスタシーゲージ、現在の振動状態の定期的（3秒ごと）なデバッグログをコンソールに出力するかどうか。
    *   **デフォルト:** `false`
    *   **推奨:** Mod がゲームの状態にどのように反応するかを観察したい場合にのみ `true` に設定します。

#### 5.2. クライマックスモード設定

*   `ClimaxVibrationDuration` (浮動小数点数):
    *   クライマックスモードで、各「オン」振動パルスの持続時間（秒）。
    *   **デフォルト:** `0.4`
*   `ClimaxPauseDuration` (浮動小数点数):
    *   クライマックスモードで、振動パルス間の各「オフ」一時停止の持続時間（秒）。
    *   **デフォルト:** `0.4`
*   `ClimaxMaxIntensityLevel` (浮動小数点数):
    *   クライマックスモード中に使用される最大振動強度レベル（0-20スケール）。
    *   **デフォルト:** `20.0` (最大強度)
*   `LowVibeClimaxBaseCycles` (整数):
    *   ゲームの VibeState が「Low」の場合、クライマックスの基本振動サイクル数（小クライマックスまたは大クライマックスの基本部分に適用）。
    *   **デフォルト:** `5`
*   `LowVibeClimaxMaxAccumulatedCycles` (整数):
    *   ゲームの VibeState が「Low」の場合、心拍数を通じて蓄積できる追加のクライマックス振動サイクルの最大数。
    *   **デフォルト:** `25`
*   `HighVibeClimaxBaseCycles` (整数):
    *   ゲームの VibeState が「High」の場合、クライマックスの基本振動サイクル数。
    *   **デフォルト:** `10`
*   `HighVibeClimaxMaxAccumulatedCycles` (整数):
    *   ゲームの VibeState が「High」の場合、心拍数を通じて蓄積できる追加のクライマックス振動サイクルの最大数。
    *   **デフォルト:** `50`
*   `MajorClimaxTriggerCount` (整数):
    *   「大クライマックス」をトリガーするために必要な蓄積された「小クライマックス」の回数。例えば、`3` に設定した場合、3回の小クライマックスの後（再びクライマックスがトリガーされた場合）、次が「大クライマックス」になります。
    *   **デフォルト:** `3`

#### 5.3. クライマックスクールダウンとモーター動作設定

*   `MinorClimaxCooldownDuration` (浮動小数点数):
    *   「小クライマックス」振動モード終了後の無振動クールダウン期間（秒）。この期間は、Mod によってインテリジェントに複数の1秒（または残りの分数）のサイレントコマンドに分割され、一貫した制御を保証します。
    *   **デフォルト:** `5.0`
*   `MajorClimaxCooldownDuration` (浮動小数点数):
    *   「大クライマックス」振動モード終了後の無振動クールダウン期間（秒）。同様に、小さなコマンドに分割されます。
    *   **デフォルト:** `10.0`
*   `MotorStaggerDuration` (浮動小数点数):
    *   このパラメータは、デバイスの複数のモーター間で強度が段階的に変化する際の微小な時間オフセット（秒）を制御します。これは、アクティブなパターン中と、徐々にゼロに移行する際のいずれにも適用されます。これにより、振動に波状またはリップル効果が生まれます。
    *   **デフォルト:** `0.01`
    *   **推奨:** 滑らかな千鳥効果を得るために、この値は小さく保つことが推奨されます。値を高く設定しすぎると、振動パターンが途切れたり、不自然に感じられる場合があります。単一モーターデバイスにはこの設定は影響しません。

## 6. トラブルシューティング

*   **Mod がロードされない:**
    *   `VibeSyncMod.dll` と `vibe_config.json` ファイルがゲームの `Mods` フォルダに正しく配置されていることを確認してください。
    *   MelonLoader コンソールにエラーメッセージがないか確認してください。
*   **Buttplug サーバーに接続できない（`=` キーを押しても反応がない、またはエラーが出る）:**
    *   Intiface Central アプリケーションがコンピューターで実行されていることを確認してください。
    *   Intiface Central の設定を確認し、WebSocket サーバーが有効になっており、そのポートが `vibe_config.json` の `ButtplugServerUri`（デフォルト: `12345`）と一致していることを確認してください。
    *   ファイアウォールの設定を確認し、ゲームと `127.0.0.1:12345`（または設定した別のアドレス）間の通信がブロックされていないことを確認してください。
    *   Intiface Central とゲームの両方を再起動してみてください。
*   **デバイスは接続されているが振動しない:**
    *   Intiface Central 内でデバイスが接続され、正しく機能していることを確認してください。Intiface Central で手動で振動を制御してみて、デバイスが反応するかどうかを確認してください。
    *   ゲーム内で `-` キーを押して詳細ログを有効にし、「No vibrating device available」や「Invalid motor index」のような警告がないか確認してください。
    *   ゲーム内のキャラクターの心拍数が 90-160 BPM の範囲内であり、VibeState が「Low」または「High」（「Off」ではない）であることを確認してください。Mod はこれらのパラメータの範囲内でのみアクティブになります。
*   **振動パターンが期待通りではない:**
    *   `EnableHeartRateDebugLog` を `true` に設定し、ゲーム内で `-` キーを押して、3秒ごとの詳細な状態ログを観察してください。これにより、現在の心拍数、エクスタシーゲージ、VibeState、および Mod が実行しようとしている正確な振動指示が表示されます。この情報を期待値と比較してください。
    *   `vibe_config.json` の様々なパラメータ、特に強度と時間に関連する設定、およびクライマックスモードの設定を調整してください。
*   **ゲームの途切れやパフォーマンスの低下:**
    *   ログ出力を減らすために、`EnableVerboseLogging` と `EnableHeartRateDebugLog` を `false` に設定してください。
    *   `MotorStaggerDuration` が誤って高すぎる値に設定されている場合、その値を下げてください。
    *   複数のモーターを備えたデバイスは処理をわずかに増加させる可能性がありますが、通常 Buttplug プロトコルは効率的です。

解決できない問題が発生した場合は、Mod のサポートチャネル（利用可能な場合）に MelonLoader コンソールの完全なログを提供してください。

---

VibeSync Mod をご利用いただきありがとうございます。皆様のゲーム体験が向上することを願っています！

---
---

# VibeSync Mod 用户手册

## VibeSync Mod v3.8.5

---

## 1. 简介

VibeSync Mod 是一款 MelonLoader 模组，旨在通过 Buttplug.io 框架，将您的 Buttplug 兼容型设备（如 Lovense 玩具）的震动与游戏内的特定状态动态同步。它能根据您的心率、游戏角色的“VibeState”（震动状态）和“Ecstasy Gauge”（狂喜槽）的填充量，智能地调整震动模式和强度，提供沉浸式的互动体验。

## 2. 主要功能

*   **动态震动同步:** 根据游戏中的实时数据：心率、VibeState（低震动/高震动）和狂喜槽的填充量，动态调整震动强度和模式。
*   **多样化的震动模式:** 提供波浪式（Low Wave / High Wave）、间歇式（Low Intermittent / High Intermittent）以及混合式（Low Hybrid / High Hybrid）等多种预设震动模式。
*   **智能高潮模式:** 当游戏内狂喜槽达到特定条件时，自动触发剧烈的高潮震动模式，并根据积累情况区分“小高潮”和更强烈的“大高潮”。
*   **可配置的冷却时间:** 小高潮和大高潮结束后，有独立的、可自定义的无震动冷却时间，帮助您从高潮中恢复。这些冷却时间会被智能地拆分成小段指令，确保平滑控制。
*   **多马达错位震动:** 如果您的设备有多个震动马达，模组可以实现马达间强度逐步传递的错位效果，创造更丰富、更有趣的震动模式。
*   **实时控制与调试:** 提供游戏内快捷键，方便您连接/断开 Buttplug 服务器以及切换详细日志输出。
*   **高度可定制:** 所有关键参数都可通过外部 JSON 配置文件进行调整，以适应您的个人偏好和设备特性。

## 3. 安装指南

1.  **安装 MelonLoader:** 确保您已按照 MelonLoader 的官方指南，为您的游戏成功安装了 MelonLoader。
2.  **下载 Intiface Central:** VibeSync Mod 需要 Buttplug.io 的 Intiface Central 应用程序作为 Buttplug 设备和 Mod 之间的桥梁。请从 Buttplug.io 官方网站下载并安装 Intiface Central。
3.  **下载 VibeSync Mod:** 下载 `VibeSyncMod.dll` 文件和 `vibe_config.json` 文件到您的计算机上。
4.  **部署 Mod 文件:** 将下载的 `VibeSyncMod.dll` 和 `vibe_config.json` 文件放入游戏根目录下的 `Mods` 文件夹中。如果 `Mods` 文件夹不存在，请手动创建它。
    *   示例路径：`您的游戏文件夹/Mods/VibeSyncMod.dll`
    *   示例路径：`您的游戏文件夹/Mods/vibe_config.json`
5.  **启动 Intiface Central:** 在启动游戏之前，请确保 Intiface Central 正在运行，并且您的 Buttplug 设备已连接并被 Intiface Central 识别。

## 4. 如何使用

1.  **启动游戏。**
2.  **连接 Buttplug 服务器:** 在游戏内按下键盘上的 **`=` (等号) 键**。您会在 MelonLoader 控制台看到连接尝试和结果信息。如果连接成功，您的设备可能会有短暂的震动反馈。
3.  **断开 Buttplug 服务器:** 再次按下 **`=` (等号) 键**。设备将停止震动并断开连接。
4.  **切换详细日志:** 在游戏内按下键盘上的 **`-` (减号) 键**。这将切换 MelonLoader 控制台中是否显示详细的调试日志。开启详细日志可以帮助您了解 Mod 的内部工作状态和排除故障。
5.  **体验动态震动:** 模组将根据游戏内您的心率、VibeState 和狂喜槽的实时变化，自动开始并调整您的设备的震动。

## 5. 配置文件 (`vibe_config.json`) 说明

`vibe_config.json` 文件允许您自定义 Mod 的行为。您可以使用任何文本编辑器（如记事本、Notepad++、VS Code）打开并编辑它。

**重要提示:** 在编辑配置文件之前，最好先关闭游戏。如果您在游戏运行时修改了配置文件，需要重新启动游戏或重新连接 Mod（按 `=` 键两次）才能使更改生效。

```json
{
  "ButtplugServerUri": "ws://127.0.0.1:12345",
  "ConnectKey": "Equals",
  "LogToggleKey": "Minus",
  "EnableVerboseLogging": true,
  "EnableHeartRateDebugLog": false,

  "ClimaxVibrationDuration": 0.4,
  "ClimaxPauseDuration": 0.4,
  "ClimaxMaxIntensityLevel": 20.0,
  
  "LowVibeClimaxBaseCycles": 5,
  "LowVibeClimaxMaxAccumulatedCycles": 25,
  "HighVibeClimaxBaseCycles": 10,
  "HighVibeClimaxMaxAccumulatedCycles": 50,
  
  "MajorClimaxTriggerCount": 3,
  
  "MinorClimaxCooldownDuration": 5.0,
  "MajorClimaxCooldownDuration": 10.0,
  "MotorStaggerDuration": 0.01
}
```

### 参数详解:

#### 5.1. 通用设置

*   `ButtplugServerUri` (字符串):
    *   Buttplug 服务器（例如 Intiface Central）的 WebSocket 地址。
    *   **默认值:** `"ws://127.0.0.1:12345"`
    *   **建议:** 通常不需要更改，除非您将 Intiface Central 设置为使用不同的端口或运行在不同的电脑上。
*   `ConnectKey` (字符串):
    *   用于连接/断开 Buttplug 服务器的键盘按键。
    *   **默认值:** `"Equals"` (对应键盘上的 `=` 键)
    *   **可选项:** Unity `KeyCode` 枚举的字符串表示，例如 `"C"`，`"Space"`，`"Return"` 等。
*   `LogToggleKey` (字符串):
    *   用于切换 MelonLoader 控制台详细日志输出的键盘按键。
    *   **默认值:** `"Minus"` (对应键盘上的 `-` 键)
    *   **可选项:** Unity `KeyCode` 枚举的字符串表示，例如 `"K"`，`"L"` 等。
*   `EnableVerboseLogging` (布尔值):
    *   是否在 MelonLoader 控制台输出非常详细的调试日志。
    *   **默认值:** `true`
    *   **建议:** 调试问题时设为 `true`，正常游玩时可设为 `false` 以减少日志输出量。
*   `EnableHeartRateDebugLog` (布尔值):
    *   是否每 3 秒在控制台输出一次心率、狂喜槽和当前震动状态的调试日志。
    *   **默认值:** `false`
    *   **建议:** 仅在您想查看 Mod 如何根据游戏状态做出反应时设为 `true`。

#### 5.2. 高潮模式设置

*   `ClimaxVibrationDuration` (浮点数):
    *   高潮模式中，每次震动“开启”的持续时间 (秒)。
    *   **默认值:** `0.4`
*   `ClimaxPauseDuration` (浮点数):
    *   高潮模式中，每次震动“停止”的持续时间 (秒)。
    *   **默认值:** `0.4`
*   `ClimaxMaxIntensityLevel` (浮点数):
    *   高潮模式中的最大震动强度 (0-20级)。
    *   **默认值:** `20.0` (最高强度)
*   `LowVibeClimaxBaseCycles` (整数):
    *   当游戏 VibeState 为“Low”时，小高潮（或大高潮的基础部分）的基础震动循环次数。
    *   **默认值:** `5`
*   `LowVibeClimaxMaxAccumulatedCycles` (整数):
    *   当游戏 VibeState 为“Low”时，高潮模式中可通过心率累积的额外震动循环次数的上限。
    *   **默认值:** `25`
*   `HighVibeClimaxBaseCycles` (整数):
    *   当游戏 VibeState 为“High”时，小高潮（或大高潮的基础部分）的基础震动循环次数。
    *   **默认值:** `10`
*   `HighVibeClimaxMaxAccumulatedCycles` (整数):
    *   当游戏 VibeState 为“High”时，高潮模式中可通过心率累积的额外震动循环次数的上限。
    *   **默认值:** `50`
*   `MajorClimaxTriggerCount` (整数):
    *   触发“大高潮”所需的累计“小高潮”次数。例如，设为 `3` 表示每经历 3 次小高潮后（如果再次触发高潮），下一次将是“大高潮”。
    *   **默认值:** `3`

#### 5.3. 高潮冷却与马达行为设置

*   `MinorClimaxCooldownDuration` (浮点数):
    *   “小高潮”震动模式结束后，设备完全停止震动的冷却持续时间 (秒)。这个时间会被 Mod 智能切割成多个 1 秒（或剩余不足 1 秒）的静默指令，以保证指令发送的规律性。
    *   **默认值:** `5.0`
*   `MajorClimaxCooldownDuration` (浮点数):
    *   “大高潮”震动模式结束后，设备完全停止震动的冷却持续时间 (秒)。同样会被 Mod 切割成多个静默指令。
    *   **默认值:** `10.0`
*   `MotorStaggerDuration` (浮点数):
    *   这个参数控制多马达设备在模式执行过程中，以及模式结束后逐步归零时，每个马达之间**强度变化的微小时间错位**。它创造一种波浪或涟漪般的震动感。
    *   **默认值:** `0.01`
    *   **建议:** 通常保持这个小值，以获得平滑的错位效果。设置太高可能会导致震动模式显得卡顿或不流畅。对于单马达设备，此设置无效。

## 6. 故障排除

*   **Mod 未加载:**
    *   确保 `VibeSyncMod.dll` 和 `vibe_config.json` 文件正确放置在游戏的 `Mods` 文件夹中。
    *   检查 MelonLoader 控制台是否有任何错误信息。
*   **无法连接到 Buttplug 服务器（按 `=` 键无反应或报错）:**
    *   确保 Intiface Central 应用程序正在您的电脑上运行。
    *   检查 Intiface Central 的设置，确认 WebSocket 服务器已启用，并且其端口与 `vibe_config.json` 中的 `ButtplugServerUri` (默认为 `12345`) 匹配。
    *   检查您的防火墙设置，确保没有阻止游戏与 `127.0.0.1:12345` (或您配置的其他地址) 之间的通信。
    *   尝试重新启动 Intiface Central 和游戏。
*   **设备连接但没有震动:**
    *   在 Intiface Central 中确认您的设备已连接并正常工作。尝试在 Intiface Central 中手动控制震动，看设备是否响应。
    *   在游戏内按 `-` 键开启详细日志，观察是否有关于“No vibrating device available”或“Invalid motor index”的警告。
    *   检查游戏内人物的心率是否在 90-160 BPM 之间，以及 VibeState 是否为“Low”或“High”（而不是“Off”）。Mod 仅在此范围内激活。
*   **震动模式不如预期:**
    *   开启 `EnableHeartRateDebugLog` (`true`) 并在游戏内按 `-` 键，查看每 3 秒的详细状态日志。这会显示当前心率、狂喜槽、VibeState 以及 Mod 正在尝试执行的震动指令。对比这些信息与您的预期。
    *   调整 `vibe_config.json` 中的各项参数，尤其是强度和时间相关的设置，以及高潮模式的配置。
*   **游戏卡顿或性能下降:**
    *   将 `EnableVerboseLogging` 和 `EnableHeartRateDebugLog` 设置为 `false` 以减少日志输出。
    *   如果 `MotorStaggerDuration` 被意外地设置得很大，降低其值。
    *   虽然多马达设备可能会轻微增加处理负担，但通常 Buttplug 协议的效率很高。

如果遇到无法解决的问题，请在 Mod 的支持渠道（如果有的话）提供 MelonLoader 控制台的完整日志。

---

感谢您使用 VibeSync Mod，希望它能提升您的游戏体验！
