# Example: Codex Handoff

このファイルは、Codexに作業を渡すときの公開用サンプルです。

## Situation

READMEが長くなってきたため、思想説明をdocsへ分けたい。

## Goal

READMEを初見向けに読みやすくし、詳細な思想はdocs/CONCEPT.mdへ整理する。

## Files to read

```text
README.md
AGENTS.md
docs/CONCEPT.md
docs/MEMORY_MODEL.md
docs/WORKFLOW.md
```

## Task

1. READMEの重複や長すぎる説明を見つける
2. READMEに残すべき説明とdocsへ移す説明を分ける
3. READMEの中核メッセージは維持する
4. 変更案を作る
5. レビューしやすいように、変更理由を短く添える

## Keep

READMEでは、次の中核を残す。

- AIとの対話に、操縦席と外部記憶を持たせる
- ノンプログラマーがAIとの対話で作っている実験である
- GitHubをAIの外部記憶として使う
- 人間の判断権を残したままAIを使う

## Do not

- 単なるプロンプト集として説明しない
- AIに全部任せる自動化として説明しない
- private情報を入れない
- 未確認の内容を採用済みとして扱わない
- READMEの芯を弱めない

## Expected output

```text
- Proposed README changes
- Reason for each major change
- Any open questions
```

## Review checklist

- READMEは短く読みやすいか
- docsとの役割分担は明確か
- CCOSの中核が残っているか
- 公開して問題ない内容だけか
