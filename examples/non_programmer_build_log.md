# Example: Non-programmer Build Log

このファイルは、Captain Chappy（CCOS）の公開用サンプルです。

ノンプログラマーがAIとの対話を通じて、自分用のAI作業環境を作っていく流れを示します。

## Starting point

ユーザーは、プログラマーではありません。

しかし、ChatGPTやCodexを使って、次のようなものを作りたいと考えています。

- 自分専用のAI記憶
- GitHub上の作業ルール
- AIに読ませる取扱説明書
- 会話を次回へ引き継ぐメモ
- Codexに渡す作業指示
- 公開できるOSSテンプレート

## Step 1: Conversation

最初は、きれいな設計書ではなく、AIとの雑な会話から始まります。

```text
AIとの対話が毎回リセットされる。
自分の意図や判断軸を、GitHubに置いてAIに読ませられないか。
ノンプログラマーでも、自分用のAI作業環境を作れるようにしたい。
```

## Step 2: Concept extraction

会話から、次の中核が抽出されます。

- AIとの対話に、操縦席と外部記憶を持たせる
- GitHubをAIの外部記憶として使う
- AIが勝手に決めるのではなく、人間の判断権を残す
- 会話をその場限りにせず、次の作業に引き継ぐ

## Step 3: Repository setup

公開用リポジトリを作ります。

```text
README.md
AGENTS.md
docs/
templates/
examples/
```

## Step 4: README

READMEでは、プロジェクトの入口を説明します。

- 何を作っているか
- なぜ必要か
- 誰に役立つか
- 何ではないか
- 現在どの段階か

## Step 5: AGENTS.md

AGENTS.mdでは、AIやCodexがこのリポジトリで作業するときのルールを書きます。

- public/privateを混ぜない
- 未確認の内容を採用済みにしない
- READMEを長くしすぎない
- docs、templates、examplesの役割を分ける

## Step 6: Templates

他の人が自分用に複製できるテンプレートを作ります。

- user_memory.md
- workflow.md
- handoff_memo.md
- review_checklist.md

## Step 7: Maintenance

作って終わりではなく、定期的に見直します。

- 重複していないか
- 古くなっていないか
- READMEに詰め込みすぎていないか
- private情報が混ざっていないか
- 次に使いやすい形になっているか

## What this demonstrates

この例が示しているのは、次のことです。

- ノンプログラマーでも、AIとの対話でOSSの構想を形にできる
- GitHubを使えば、AIの記憶や作業ルールを見える形にできる
- AIとの会話は、次の作業に引き継げる資産にできる
- CodexやChatGPTは、コードだけでなく、作業環境そのものを作る相棒になりうる

Captain Chappyを作ること自体が、Captain Chappyの使い方のデモです。
