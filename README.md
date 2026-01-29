# 状態管理ツール

日々の出来事を記録し  
中間状態（current）を経由して  
週報などの報告書を生成する PoC ツール。

## Docs
- LT 向けにまとめた検討背景  
  docs/lt-background.md

## Usage

### 状態更新

日々あったことを日本語でそのまま入力する。

**入力例**

```bash
state update
- 今日はAPI設計の見直しを進めた
- エンドポイント案を3つに絞り込んだ
- レビューは来週の定例で実施予定
- 認可まわりの仕様が曖昧で実装方針を決めきれていない
- 既存の権限モデルの資料が見つからず確認に時間がかかった
- パフォーマンス要件が未確定なのでページング戦略が決められない
- 明日やることはレビュー用の資料を作ること
- 合わせて認可仕様の確認先を洗い出す
- ベンダーに質問事項を投げる
```

実行結果

- log.md に日付付きで追記される
- current.md が更新される

---

### 週報生成

current.md を元に週報を生成する。

```bash
weekly generate
```

実行結果

- weekly/YYMMDD-YYMMDD.md が生成される
- current の状態を元に整形された週報 Markdown が出力される

---

※ 本ツールは完成品ではなく、状態管理と agent 設計の PoC です。

<!--
個人用
- リポジトリ
  - https://github.com/ShunsukeNONOMURA/experiments-status-manager
- chatgpt壁打ち
  - https://chatgpt.com/c/697b0a8f-247c-8324-a534-7ac9452a2db5
-->