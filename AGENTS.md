# AGENTS.md

このファイルは、Captain Chappy（CCOS）リポジトリで作業するAI / Codex / エージェント向けの作業ルールです。

## Project purpose

Captain Chappyは、AIとの対話に「操縦席」と「外部記憶」を持たせるための実験的なOSSです。

目的は、ChatGPT / Codex / AIエージェントを、人間が意図と判断権を保ったまま継続的に使えるようにすることです。

このリポジトリは公開用です。個人用の非公開メモやprivateリポジトリの内容を、そのまま混ぜ込まないでください。

## Core principles

1. **Human judgment stays visible**
   - AIが勝手に決定済みにしない。
   - 未確認、仮置き、採用済み、反映待ちを混同しない。
   - 提案と実行を分ける。

2. **Public repository only contains public-safe material**
   - 個人情報、非公開会話、private repoの固有内容、本音の作業ログは入れない。
   - 公開する場合は、一般化・匿名化・テンプレート化する。

3. **CCOS is not a prompt dump**
   - 単発プロンプト集ではなく、外部記憶・対話ハーネス・運用ワークフローのOSSとして扱う。
   - ファイルを増やすときは、役割が明確なものだけ追加する。

4. **Do not weaken the concept**
   - 「便利なAI活用術」だけに縮小しない。
   - 「AIに全部任せる自動化」として説明しない。
   - 中核は、ユーザーが自分の意図・制約・判断軸を保ったままAIを使うこと。

5. **Keep files maintainable**
   - 長すぎる思想説明は `docs/` に分ける。
   - 再利用できる型は `templates/` に置く。
   - 実例は `examples/` に置く。
   - READMEは入口として読みやすく保つ。

## Repository structure

```text
README.md
  Project overview for humans.

AGENTS.md
  Operating rules for AI/Codex contributors.

docs/
  Concept, memory model, workflow, and design notes.

templates/
  Reusable markdown templates for users who want to build their own CC-style setup.

examples/
  Public-safe examples showing how CCOS can be used.
```

## File roles

- `README.md`: 初見向けの説明。短く魅力的に、CCOSの意義を伝える。
- `docs/CONCEPT.md`: READMEに入りきらない思想・背景・長期ビジョン。
- `docs/MEMORY_MODEL.md`: GitHubをAI外部記憶として使う設計。
- `docs/WORKFLOW.md`: 会話からメモ、レビュー、反映までの流れ。
- `templates/`: 他の人が自分用に複製・編集できる型。
- `examples/`: 公開できる実例。privateな具体情報は入れない。

## Writing rules

- 日本語を主言語にする。必要に応じて英語キーワードを併記する。
- 読み手は非エンジニアも含むため、抽象語だけで終わらせない。
- 「AIが勝手にやる」ではなく「人間が確認・編集・レビューできる」を重視する。
- 断定しすぎず、実験段階であることを明示する。
- 公開資料として読まれても問題ない表現にする。

## Safety and privacy

- privateリポジトリや個人メモ由来の情報は、そのまま公開しない。
- 実例を作る場合は、個人名、メール、URL、社名、固有事情を一般化する。
- READMEやdocsでは、CCOSの構想・仕組み・再現可能な型を説明する。
- ユーザー固有の深い記憶は、公開テンプレートではなくprivate側で扱う。

## Change policy

- 既存ファイルを更新する前に、目的と影響範囲を確認する。
- READMEの中核メッセージを変える場合は、次の3点を維持する。
  1. AIとの対話に、操縦席と外部記憶を持たせる。
  2. ノンプログラマーがAIとの対話で作っている実験である。
  3. GitHubを、見える・編集できる・レビューできるAI記憶として使う。
- 未合意の大きな方向転換は行わない。

## Current status

This repository is experimental and public-facing.

Treat all files as early public drafts unless a later version states otherwise.
