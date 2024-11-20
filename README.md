# 多機能Discord Bot

## 概要
このプロジェクトは、Discordサーバー向けに多機能で高拡張性を備えたボットを提供することを目的としています。  
サーバー管理を行う高性能ボットに加え、ChatGPTや生成AI機能を活用し、コミュニケーションやエンターテインメント、管理ツールを一体化したソリューションを目指しています。

---

## 特徴
1. **AI連携機能**
   - ChatGPTを利用した自然言語対話やテキスト生成。
   - 画像生成機能に対応（DALL-EなどのAPI統合）。
   - 名言ジェネレーターやクイズ自動生成。

2. **リアルタイム操作**
   - ダッシュボード上で埋め込みメッセージを作成・編集し、リアルタイムで反映。
   - チャンネルやスレッドを指定した発言が可能。

3. **拡張性**
   - プラグイン対応で、新しい機能を簡単に追加。
   - 管理者専用の高度な設定機能。

4. **定期発言機能**
   - 毎日「今日は〇〇の日」と記念日を自動で投稿。
   - カスタマイズ可能な通知スケジュール。

5. **エンターテインメント**
   - ミニゲーム、クイズ、音楽再生など多彩な遊び心を提供。

---

## 主な機能
### AI機能
- **ChatGPT連携**:
  - 質問応答、物語生成、カスタム対話が可能。
- **画像生成**:
  - 指定されたテーマに基づいてイラストや画像を生成。
- **感情認識**:
  - メッセージの感情を分析して適切な応答を返す。

### サーバー管理
- **自動モデレーション**:
  - 不適切な発言やスパムを自動で削除。
- **権限管理**:
  - 条件に応じた自動ロール付与。
- **アクティビティログ**:
  - 入退室やメッセージの操作を記録。

### ダッシュボード機能
- **埋め込みメッセージ操作**:
  - ダッシュボードで作成、リアルタイムプレビュー。
- **統計分析**:
  - サーバーの発言数やユーザーのアクティビティを可視化。

### エンタメ機能
- **ミニゲーム**:
  - クイズ、RPG風アクションゲーム、GeoGuessr風ゲーム。
- **名言ジェネレーター**:
  - ランダムまたはテーマ別に名言を生成。
- **音楽プレイヤー**:
  - YouTubeやSpotifyと連携。

---

## プロジェクトツリー
```plaintext
discord-bot/
├── src/
│   ├── commands/       # 各種コマンド機能
│   │   ├── admin.js    # 管理用コマンド
│   │   ├── fun.js      # エンタメ用コマンド
│   │   ├── ai.js       # AI関連コマンド
│   ├── events/         # イベントリスナー
│   │   ├── ready.js    # Bot起動時イベント
│   │   ├── message.js  # メッセージイベント
│   ├── utils/          # 共通ユーティリティ
│   │   ├── logger.js   # ログ出力
│   │   ├── database.js # データベース操作
│   ├── bot.js          # Botメインロジック
│   ├── config.json     # 設定ファイル
├── dashboard/
│   ├── public/         # 静的リソース
│   ├── src/            # ダッシュボードアプリケーション
│   │   ├── components/ # Reactコンポーネント
│   │   ├── pages/      # 各ページ
│   │   ├── App.js      # アプリケーションエントリポイント
│   ├── package.json    # フロントエンド依存関係
├── .env                # 環境変数
├── package.json        # サーバー依存関係
├── README.md           # このファイル
```

---

## インストール方法

1. このリポジトリをクローンします。
   ```bash
   git clone https://github.com/your-repo/discord-bot.git
   cd discord-bot
   ```

2. 必要な依存パッケージをインストールします。
   ```bash
   npm install
   ```

3. 環境変数を設定します。
   `.env` ファイルを作成し、以下を追加:
   ```env
   DISCORD_TOKEN=your_discord_bot_token
   CLIENT_ID=your_discord_client_id
   ```

4. ボットを起動します。
   ```bash
   npm start
   ```

---

## 使用方法
- ダッシュボードにアクセスし、Bot設定や管理を行います。
- コマンドリストを確認するには、Discord内で `/help` を使用します。

---

## 貢献方法
1. このリポジトリをフォークしてください。
2. 新しいブランチを作成します: `git checkout -b feature/new-feature`
3. 変更をコミットします: `git commit -m 'Add new feature'`
4. プルリクエストを送信してください。

---

## ライセンス
このプロジェクトはMITライセンスのもとで提供されています。