# 勤怠管理Bot

### 使用例

#### 出勤

- おはようございます => 現在時刻で出勤
- 今日は11時に出勤しました => 今日の11時に出勤
- 昨日は11時に出勤しました => 昨日の11時に出勤
- 7月30日は11時に出勤しました => 7/30の11時に出勤

#### 退勤

- お疲れ様でした => 現在時刻で退勤
- 今日は18時に退勤しました => 今日の18時に退勤
- 昨日は１８時に退勤しました => 昨日の18時に退勤
- 7月３０日は18時に退勤しました => 7/30の18時に退勤

#### 休憩

- 今日は休憩なしでした => 今日の休憩をなしにする
- 今日は2時間休憩しました => 今日の休憩を2時間にする

## セットアップ

### パッケージのインストール
```
yarn install
```

### Slack Appの設定

- Slack Verification Tokenを取得
- Slack Bot User Tokenを取得
- Slack Incoming Urlを取得

### env

envに取得したSlack Appの情報を追加

### google apps scriptの設定
googleにログイン

```
yarn clasp login
```

google apps scriptのプロジェクトを作成

```
yarn clasp create
```

google apps scriptで　ファイル＞プロジェクトのプロパティ＞スクリプトのプロパティ　にプロパティ->`sheetId`、値->スプレッドシートのID を設定

### deploy
```
yarn deploy
```

- google apps scriptで　公開＞Webアプリケーションとして導入　で公開する
- 公開したURLをslack event subscriberに入力する

### 完了
