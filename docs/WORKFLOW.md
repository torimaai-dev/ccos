# Workflow

## 目的

このドキュメントは、Captain Chappy（CCOS）で想定する基本ワークフローを説明します。

CCOSの目的は、AIとの会話をその場限りで終わらせず、次の対話・作業・レビューに使える形へ変換することです。

## 基本の流れ

```text
1. Conversation
   AIとの会話・相談・壁打ち

2. Capture
   重要な文脈、判断軸、未決事項を回収

3. Classify
   一時メモ、反映候補、採用済み、private情報を分ける

4. Review
   人間が確認する

5. Publish / Apply
   公開用docs、templates、AGENTS.mdなどへ反映

6. Maintain
   重複、古さ、矛盾、次回への引き継ぎを整理
```

## 1. Conversation

最初は、きれいな指示である必要はありません。

CCOSは、雑な相談、途中の違和感、未整理なアイデアも素材として扱います。

ただし、会話そのものをそのまま公開ファイルにするのではなく、後で使える文脈へ整理します。

## 2. Capture

会話から回収するものは、主に次のような情報です。

- ユーザーの目的
- 制約
- 判断軸
- 嫌なこと、避けたいこと
- まだ決まっていないこと
- 次に確認すべきこと
- 再利用できる表現
- ワークフロー化できる手順

重要なのは、会話ログを保存すること自体ではなく、次に使える形にすることです。

## 3. Classify

回収した情報は、状態ごとに分けます。

```text
draft
  下書き。まだ整理途中。

candidate
  反映候補。採用するか確認が必要。

accepted
  採用済み。次回以降も使うルールや知識。

needs_review
  人間の確認待ち。

private
  公開不可。

archived
  参照用。
```

AIは、candidateを勝手にacceptedとして扱ってはいけません。

## 4. Review

レビューでは、次を確認します。

- 目的に合っているか
- private情報が混ざっていないか
- 仮置きと採用済みを混同していないか
- 既存のREADMEやdocsと矛盾していないか
- 他の人が読んでも再利用できる形になっているか
- AIが勝手に意味を変えていないか

## 5. Publish / Apply

レビュー後、公開できるものだけをpublic repositoryへ反映します。

配置の目安は次の通りです。

```text
README.md
  初見向けの概要。

AGENTS.md
  AI/Codex向け作業ルール。

docs/
  詳しい思想、設計、運用説明。

templates/
  他の人が複製して使える型。

examples/
  公開できる実例。
```

## 6. Maintain

記憶やドキュメントは、作って終わりではありません。

定期的に次を見直します。

- 重複している内容
- 古くなった説明
- 長くなりすぎたREADME
- docsに分けた方がよい思想説明
- templatesに切り出せる型
- examplesにできる実例
- AGENTS.mdに追加すべき運用ルール

## プッシュ型ガイド

CCOSは、ユーザーが明確な質問をするまで待つだけではなく、保存された文脈から次に必要そうな作業を提案することを目指します。

例:

- 「この会話はhandoff_memoにした方がよい」
- 「これはREADMEではなくdocs/CONCEPT.md向き」
- 「これはpublicではなくprivateに残すべき」
- 「この未決事項はreview対象にするべき」
- 「次はAGENTS.mdにルール化した方がよい」

ただし、提案と実行は分けます。

AIが勝手に反映せず、人間が確認できる形にします。

## 非エンジニア向けの前提

CCOSは、プログラマーだけのためのものではありません。

非エンジニアでも、AIとの対話を通じて、自分の作業環境、判断軸、メモ、プロンプト、ワークフローを少しずつ育てられることを目指します。

そのため、ワークフローは複雑にしすぎず、次の状態を大事にします。

- どこに何を書くか分かる
- AIに何を頼めばいいか分かる
- 何がまだ未確認か分かる
- 公開してよいものとprivateなものを分けられる
- 次回の会話に引き継げる

## 最小運用

最初の最小構成は次の通りです。

```text
README.md
AGENTS.md
docs/CONCEPT.md
docs/MEMORY_MODEL.md
docs/WORKFLOW.md
templates/handoff_memo.md
templates/review_checklist.md
examples/non_programmer_build_log.md
```

この構成から始め、必要に応じて増やします。
