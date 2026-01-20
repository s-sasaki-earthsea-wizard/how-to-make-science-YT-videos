# 科学動画の作り方 - YouTube動画シリーズ

## プロジェクト概要

科学技術系YouTubeチャンネル向けの「科学動画の作り方」シリーズの脚本と構成を管理するプロジェクトです。動画制作のノウハウを共有し、科学コミュニケーションの発展に貢献することを目指します。

## シリーズ構成

| #   | エピソード         | フォルダ                                           | 状態   |
| --- | ------------------ | -------------------------------------------------- | ------ |
| 1   | 動画制作           | `video-scripts/1-video-production/`                | 準備中 |
| 2   | 脚本と構成         | `video-scripts/2-script-and-composition/`          | 未着手 |
| 3   | リサーチと資料収集 | `video-scripts/3-research-and-material-gathering/` | 未着手 |
| 4   | 機材とツール       | `video-scripts/4-equipment-and-tools/`             | 未着手 |
| 5   | バックストーリー   | `video-scripts/5-backstories/`                     | 未着手 |

## ディレクトリ構造

```text
how-to-make-science-YT-videos/
├── CLAUDE.md                    # プロジェクト設定・開発ガイドライン
├── README.md                    # プロジェクト説明
├── Makefile                     # 開発用コマンド
├── organizer.yaml               # GitHub設定
├── instructions/                # 制作ガイドライン
│   └── youtube_script_guidelines.md  # TTS変換ガイドライン
├── manim-scripts/               # Manimアニメーションスクリプト
└── video-scripts/               # 動画別脚本
    ├── 1-video-production/
    │   ├── survey-draft.md      # 調査・下書き
    │   ├── yt_script.md         # YouTube動画脚本
    │   ├── yt_script_tts.md     # TTS用脚本
    │   └── youtube_description.md  # 動画説明文
    ├── 2-script-and-composition/
    ├── 3-research-and-material-gathering/
    ├── 4-equipment-and-tools/
    └── 5-backstories/
```

## 各ファイルの役割

| ファイル                 | 説明                                       |
| ------------------------ | ------------------------------------------ |
| `survey-draft.md`        | トピックの調査結果、参考資料、下書きメモ   |
| `yt_script.md`           | 完成版のYouTube動画脚本                    |
| `yt_script_tts.md`       | ElevenLabs TTS用に最適化された脚本         |
| `youtube_description.md` | YouTube動画の説明文（概要欄）              |

## 言語設定

このプロジェクトでは**日本語**での応答を行ってください。コード内のコメント、ログメッセージ、エラーメッセージ、ドキュメンテーション文字列なども日本語で記述してください。

## 開発ルール

### コーディング規約

- Python: PEP 8準拠
- 関数名: snake_case
- クラス名: PascalCase
- 定数: UPPER_SNAKE_CASE
- Docstring: Google Style

## Git運用

- ブランチ戦略: feature/*, fix/*, refactor/*
- コミットメッセージ: 英文を使用、動詞から始める
- PRはmainブランチへ

## 開発ガイドライン

### ドキュメント更新プロセス

機能追加やPhase完了時には、以下のドキュメントを同期更新する：

1. **CLAUDE.md**: プロジェクト全体状況、Phase完了記録、技術仕様
2. **README.md**: ユーザー向け機能概要、実装状況、使用方法
3. **Makefile**: コマンドヘルプテキスト（## コメント）の更新
4. **makefiles/**: コマンドヘルプテキスト（## コメント）の更新

### コミットメッセージ規約

#### コミット粒度

- **1コミット = 1つの主要な変更**: 複数の独立した機能や修正を1つのコミットにまとめない
- **論理的な単位でコミット**: 関連する変更は1つのコミットにまとめる
- **段階的コミット**: 大きな変更は段階的に分割してコミット

#### プレフィックスと絵文字

- ✨ feat: 新機能
- 🐞 fix: バグ修正
- 📚 docs: ドキュメント
- 🎨 style: コードスタイル修正
- 🛠️ refactor: リファクタリング
- ⚡ perf: パフォーマンス改善
- ✅ test: テスト追加・修正
- 🏗️ chore: ビルド・補助ツール
- 🚀 deploy: デプロイ
- 🔒 security: セキュリティ修正
- 📝 update: 更新・改善
- 🗑️ remove: 削除

**重要**: Claude Codeを使用してコミットする場合は、必ず以下の署名を含める：

```text
🤖 Generated with [Claude Code](https://claude.ai/code)

Co-Authored-By: Claude <noreply@anthropic.com>
```
