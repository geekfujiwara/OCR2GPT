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

ソリューションは[リリース](https://github.com/geekfujiwara/OCR2GPT/releases)からダウンロードできます。

こちらをダウンロードするようにしてください。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/3aed0333-eec5-43cc-a97d-46fabf7c31ac)


## インポート後の警告
この警告は表示言語に関するものです。基本的にはこのまま利用することができます。
![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/47bd2f63-fff8-461a-a41e-39e1cb555561)

以下の2オブジェクトで構成されています。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/dd571dfd-f4da-41c1-80e8-fb2a659404bc)

```mermaid
flowchart TD
    GeekOCR2GPT --> プロンプトテンプレート
```

## データインポート
ソリューションをインポートした時点ではオブジェクトのみが環境に展開されます。
データは移行されませんので、データのインポートを行う必要があります。

> [!NOTE]
> アプリを開くことはできますが、ソリューションをインポートしただけではプロンプトテンプレートテーブルにはデータが含まれていません。
> ![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/3a244b44-6261-4183-9130-a73700f8b597)


テーブルを開きます。
![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/ea7eca85-fba3-4e63-a16b-e46ea34a7015)


インポートを選択します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/8e7a7d67-21a5-41fb-be90-084349e8de88)


サンプルデータはこちらをダウンロードします。

[mskk_prompttemplates.csv](https://github.com/geekfujiwara/OCR2GPT/files/13603840/mskk_prompttemplates.csv)

アップロードはこちらのようにcsvファイルをドロップします。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/d659b9b9-1e8d-4ce1-9212-94bade63673d)

サインインします。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/e2a69f99-ce00-456b-9076-a57f7f2a1777)

> [!NOTE]
> 裏ではcsvファイルをOneDrive にアップロードしてそれをアップロードするためにサインインを行っています。


次へを押します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/5d7ac24b-e3bc-4cc7-b7c4-eae64de23ec8)


プレビュー、その次でも「次へ」を押します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/3a13f9ca-c157-47ec-91ae-133a0343fe32)


ウィザードが「データを取得」まで来たら、既存のテーブルに読み込むを選択し、宛先テーブルはmskk_PromptTemplate を選択します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/830ee3e2-7d1c-4561-af15-05fafac7626d)

自動マップを押すと、ソース列が自動的に設定されることを確認します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/040d87d2-7bf1-44c0-9a96-b487c71bc67f)


次へを押します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/416f9661-418d-4d33-91ca-0cdfe37ffeb6)


手動で更新として公開します。

![image](https://github.com/geekfujiwara/OCR2GPT/assets/96101315/7564ff62-9e2f-4f84-a5a0-df864313840f)


> [!NOTE]
> 実行まで時間がかかります。
> データフローで実行されるため、バッチ処理で動くためです。約1分ほどで連携されます。


これにてデータインポートは完了です。


