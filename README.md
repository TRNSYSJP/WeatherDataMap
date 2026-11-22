# Weather Data Map Plugin for TRNSYS

[English](#english) | [日本語](#日本語)

**Latest version: 1.0.1** — [Download from Releases](https://github.com/TRNSYSJP/WeatherDataMap/releases)

<img width="1031" alt="Weather Data Map Plugin 1.0.0" src="https://github.com/user-attachments/assets/aa6cd09b-9399-4113-8b8e-fc6ed94554c3" />

---

## English

### Overview

Weather Data Map is a plug-in for TRNSYS 18 Simulation Studio. It shows the stations (locations) of the TRNSYS weather data files on a map (OpenStreetMap).

Launch it from a weather data reader component (Type15 or Type99), click a station on the map, and click **OK**. The plug-in sets the weather data file to External Files of the component and renames the component to the city name.

The plug-in reads the headers of the files in the weather data folder and shows their stations on the map.

### Features

- **Current station selected at startup**: The station of the weather data selected in the component is selected and centered on the map.
- **Station search**: Search by city, state, country code or file name.
- **Map controls**: Zoom in and out, show all stations, go to the selected station, and a mini map (click or drag to move the map).
- **Station information**: Shows the city, state, country, latitude, longitude, elevation, time zone and file. **Copy** copies all of them.
- **Preferences**: Change the TRNSYS folder and the weather data folder of each format (for example, when TRNSYS is not installed in `C:\TRNSYS18`).
- **No .NET required**: You do not need to install the .NET runtime or the .NET Framework.

### Supported weather data

| Type | Format | Extension | Default folder |
|---|---|---|---|
| Type15-2 | TMY2 | `.tm2` | `Weather\US-TMY2` |
| Type15-3 | EnergyPlus (EPW) | `.epw` | `Weather\Energy+` |
| Type15-6 | Meteonorm for TRNSYS (TM2) | `.tm2` | `Weather\Meteonorm` |
| Type15-TMY3 | TMY3 | `.tmy3` | `Weather\US-TMY3` |
| Type99 | User format | `.99` | `Examples\Data Files` |

The default folders are relative to the TRNSYS folder (usually `C:\TRNSYS18`). Files in subfolders are also read.

### Requirements

- Windows 10 / Windows 11 (64-bit)
- TRNSYS 18 (Simulation Studio). TRNSYS 17 is not supported.
- Internet connection to display the map. The displayed map is kept on the PC for 14 days.
- Administrator rights to run the installer

### Installation

1. Download the latest release from [Releases](https://github.com/TRNSYSJP/WeatherDataMap/releases).
2. Run the installer (`WeatherDataMap-Setup-<version>.exe`) and select the TRNSYS 18 folder (usually `C:\TRNSYS18`) as the destination.

If a previous version (0.9.x) is installed, the installer uninstalls it automatically. The plug-in folder of 0.9.x and 1.0.0 (`Studio\Plugin\WeatherDataMap`) is removed, and the plug-in is installed in `Studio\Plugin\Quattro\WeatherDataMap`.

Note for 0.9.x users: the components have been moved to `Quattro` → `Weather Data Reading and Processing` in the Direct Access Toolbar.

Note for 0.9.x and 1.0.0 users: because the plug-in folder has changed in 1.0.1, the plug-in button is not shown for the components placed with these versions (**Standard Format with Map** and **User Format with Map**). For each component, change **Plug-in path** on the **Comment** tab to `.\Studio\Plugin\Quattro\WeatherDataMap\WeatherDataMap.exe`, and save the project (see 2.3 of the manual).

### Usage

1. In the Direct Access Toolbar of Simulation Studio, open `Quattro` → `Weather Data Reading and Processing`, and add a **Standard Format with Map** (Type15) or **User Format with Map** (Type99) component to your project.
2. Double-click the component, and click the plug-in button at the lower left of the Parameter (Input, Output, Derivative) tab.
3. Click a station on the map (or search for one), and click **OK**.

These components are the same as the standard "Standard Format" and "User Format" components of TRNSYS, except that they can launch the plug-in.

### Manual

The HTML manual (English and Japanese) is included in the release and installed with the plug-in. Open it with **Help** (F1 key) in the plug-in.

---

## 日本語

### 概要

Weather Data Map は、TRNSYS 18 の Simulation Studio で使うプラグインです。TRNSYS の気象データのファイルの地点を地図（OpenStreetMap）に表示します。

気象データリーダーのコンポーネント（Type15、Type99）から起動し、地図の地点をクリックして **OK** をクリックすると、その気象データのファイルをコンポーネントの External Files に設定し、コンポーネントの名前を地点名に変えます。

気象データのフォルダにあるファイルのヘッダーを読み、その地点を地図に表示します。

### 主な機能

- **選択中の地点を表示**: 起動したときに、コンポーネントで選ばれている気象データの地点を選び、地図の中心に表示します。
- **地点の検索**: 地点名・州・国コード・ファイル名で検索できます。
- **地図の操作**: 拡大・縮小、すべての地点の表示、選んだ地点への移動、ミニマップ（クリック・ドラッグで地図を移動）を使えます。
- **地点の情報**: 地点名、州、国、緯度、経度、標高、タイムゾーン、ファイルを表示します。**Copy** ですべてをコピーできます。
- **基本設定（Preferences）**: TRNSYS のフォルダと、形式ごとの気象データのフォルダを変えられます（TRNSYS を `C:\TRNSYS18` 以外にインストールした場合など）。
- **.NET 不要**: .NET ランタイムや .NET Framework をインストールする必要はありません。

### 対応している気象データ

| Type | 気象データの形式 | 拡張子 | 気象データのフォルダ（既定） |
|---|---|---|---|
| Type15-2 | TMY2 | `.tm2` | `Weather\US-TMY2` |
| Type15-3 | EnergyPlus（EPW） | `.epw` | `Weather\Energy+` |
| Type15-6 | Meteonorm for TRNSYS（TM2） | `.tm2` | `Weather\Meteonorm` |
| Type15-TMY3 | TMY3 | `.tmy3` | `Weather\US-TMY3` |
| Type99 | ユーザーフォーマット | `.99` | `Examples\Data Files` |

気象データのフォルダは、TRNSYS のフォルダ（通常は `C:\TRNSYS18`）からの相対パスです。サブフォルダのファイルも読みます。

### 動作に必要なもの

- Windows 10 / Windows 11（64 ビット）
- TRNSYS 18（Simulation Studio）。TRNSYS 17 には対応していません
- インターネット接続（地図の表示に使います。表示した地図は 14 日間 PC に保存します）
- インストーラーの実行に管理者の権限

### インストール

1. [Releases](https://github.com/TRNSYSJP/WeatherDataMap/releases) から最新版をダウンロードします。
2. インストーラー（`WeatherDataMap-Setup-<バージョン>.exe`）を実行し、インストール先に TRNSYS 18 のフォルダ（通常は `C:\TRNSYS18`）を指定します。

以前のバージョン（0.9.x）がインストールされている場合は、インストーラーが自動でアンインストールします。0.9.x と 1.0.0 のプラグインのフォルダ（`Studio\Plugin\WeatherDataMap`）は削除し、`Studio\Plugin\Quattro\WeatherDataMap` にインストールします。

0.9.x をお使いの方へ: コンポーネントは Direct Access Toolbar の `Quattro` → `Weather Data Reading and Processing` に移動しました。

0.9.x と 1.0.0 をお使いの方へ: 1.0.1 でプラグインのインストール先が変わったため、これらのバージョンで置いたコンポーネント（**Standard Format with Map**、**User Format with Map**）では、プラグインのボタンが表示されなくなります。コンポーネントごとに、**Comment** のタブの **Plug-in path** を `.\Studio\Plugin\Quattro\WeatherDataMap\WeatherDataMap.exe` に変え、プロジェクトを保存してください（マニュアルの 2.3）。

### 使い方

1. Simulation Studio の Direct Access Toolbar の `Quattro` → `Weather Data Reading and Processing` から、**Standard Format with Map**（Type15）または **User Format with Map**（Type99）のコンポーネントをプロジェクトに配置します。
2. コンポーネントをダブルクリックし、Parameter（Input、Output、Derivative）のタブの左下にあるプラグインのボタンをクリックします。
3. 地図の地点をクリック（または検索して選択）し、**OK** をクリックします。

これらのコンポーネントは、TRNSYS の標準の「Standard Format」「User Format」のコンポーネントと同じです。プラグインを起動できることだけが違います。

### マニュアル

HTML のマニュアル（日本語・英語）は、リリースに含まれ、プラグインと一緒にインストールされます。プラグインの **Help**（F1 キー）で開けます。

---

Map data © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors.

Copyright © 2026 quattro corporate design. All rights reserved.
