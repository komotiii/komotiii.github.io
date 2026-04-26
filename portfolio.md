# Portfolio Modernization Roadmap 2026

## 1. ポートフォリオの構想（ビジョン）
単なる「プログラムの置き場」から、**「物理学の背景を持ち、実利（期待値・自動化）を追求するデータエンジニア」**としての能力を証明するショーケースへと進化させる。

### 三層構造の戦略
1.  **【顔】 GitHub Profile**: 厳選されたPin（ピン留め）と、継続的な開発を示す「草（Contribution Graph）」。
2.  **【ハブ】 komotiii.github.io**: 非エンジニアにも伝わる言葉で実績を解説するポータルサイト。
3.  **【証明】 Clean Repositories**: 整理整頓され、リファクタリング（Refactoring）された実体コード。

---

## 2. リポジトリ配置計画（MECEマッピング）

### 🌟 スター選手（単独 Public リポジトリ）
実績として特に目立たせたい、完成度の高いプロジェクト。
* **`pachi-slot-analyzer`** ✅: Selenium並列スクレイピングと期待値算出。
* **`nar-keiba-monitor`**: 地方競馬のリアルタイムオッズ・勝率監視。
* **`sao-calendar-ui`**: アニメ風UIとGoogleカレンダーAPIの連携。
* **`nekoze-improve`**: MediaPipeを用いた姿勢検知・警告システム。
* **`raspi-home-iot`**: Raspberry Piを用いた温湿度サーバー（Flask/Tailscale検討）。

### 📦 詰め合わせモノレポ（Public リポジトリ）
小規模なスクリプトをカテゴリ別に整理した「おもちゃ箱」。

#### `python-automation-scripts` (現在作成中)
* `calendar-tools/`: `Add_event_cmd.py`, `Clear_event.py`, `Sum_calendar.py`
* `weather-tools/`: `Openweather_desk.py`, `Openweather_raspi.py`
* `desktop-monitoring/`: `CtrlV_img.py`, `CtrlV_txt.py`, `active_window.py`, `screenshot.py`, `CamScreen.py`, `Networkspeed.py`, `Typing_monitor.py`
* `api-bots/`: `PlayingBOT.py` (Refactored), `Tukunavi.py` (LINE/Discord通知)
    * *Note: .envファイルは api-bots フォルダ内で共通化。*
* `experimental/`: `Audio_txt.py` (LLM連携), `Morning_Voice.py`, `timeline_viewer.py`
* `misc/`: `Auto_startup.py`, `Tutturu15m.py`

#### `cpp-math-utils`
* `math-stats/`: `ave_med_car.cpp`, `fibo.cpp`
* `prime-numbers/`: `p_n.cpp`シリーズ（高速化版含む）
* `cli-timers/`: `timer.cpp`, `remain.cpp`シリーズ, `page_progress.cpp`, `reason.cpp`

#### `windows-workspace-config`
* `shortcut.ahk` (CapsLock rebind等), `startupv1.ahk`, `startupv2.ahk`

### 🔒 実用・機密プロジェクト（Private リポジトリ）
* **`Bybit-Trading-Panel`**: FastAPI + Reactによる取引管理パネル。
* **`bybit-trading-scripts`**: 資産運用直結の自動売買・アービトラージスクリプト群。

---

## 3. 実装のベストプラクティス（今後の指針）

### コードの品質
* **Refactoring Legacy Code**: 過去のレガシーコードを順次リファクタリング。
    * マジックナンバーの排除。
    * 冗長なプロセスの削除（例：Morning_Voiceの不要な継承）。
* **Security**: APIキーやトークンは絶対に直書きせず、`.env`ファイルで管理する。
    * GitHubには `.env.example` を上げ、実体は `.gitignore` で除外する。

### ポートフォリオサイト（komotiii.github.io）の管理
* **統合管理**: `schedule` などの単機能HTMLはリポジトリを分けず、`/schedule/index.html` のようにサブディレクトリで統合管理する。
* **導線設計**: ファイル名ではなく「〇〇システム」というプロジェクト名で紹介し、GitHubリポジトリへのリンクを貼る。

---

## 4. 進行状況チェックリスト
- [x] 不要なリポジトリのArchive化
- [x] GitHubプロフィールのREADME整備
- [x] `pachi-slot-analyzer` のPublic公開
- [/] `python-automation-scripts` の作成（PlayingBOT.pyリファクタリング中）
- [ ] `cpp-math-utils` のモノレポ作成
- [ ] `komotiii.github.io` の「プロジェクト名」ベースへの書き換え
"""

ds_python_interpreter(code=f"with open('portfolio_modernization_roadmap_2026.md', 'w', encoding='utf-8') as f: f.write({repr(content)})")
