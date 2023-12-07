# OCR2GPT
Power Apps キャンバスアプリのAI Builder テキスト認識エンジン(OCR) とGPT でテキストを作成する アクションを組み合わせたドキュメントOCRソリューションです。

# アプリの概要

# ソリューションのインポート方法

## 前提条件
AI Builder のGPT アクションが有効なリージョンで利用する必要があります。
AI Builder GPT アクションは、2023年12月時点では米国リージョンで利用することが可能です(パブリック プレビュー)。

> [!NOTE]
> 個人の学習用や開発用環境として米国リージョンの環境を取得することができます。
> 詳細は[こちら](https://learn.microsoft.com/ja-jp/power-apps/maker/maker-create-environment)をご覧ください。

ソリューションは[リリース]()からダウンロードできます。

## インポート後の警告
この警告は表示言語に関するものです。基本的にはこのまま利用することができます。
![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/47bd2f63-fff8-461a-a41e-39e1cb555561)

以下の2オブジェクトで構成されています。
![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/dd571dfd-f4da-41c1-80e8-fb2a659404bc)

```mermaid
flowchart TD
    Power Apps キャンバスアプリ: GeekOCR2GPT --> Dataverse テーブル: プロンプトテンプレート(Round Rect)
```
