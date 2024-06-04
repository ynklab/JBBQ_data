# JBBQ: 日本語社会性バイアスQAデータセット ver.1
repository for the Japanese Bias Benchmark for QA dataset (JBBQ).

本データセット(JBBQ ver.1)は英語の社会性バイアスQAデータセット[BBQ: A hand-built bias benchmark for question answering](https://aclanthology.org/2022.findings-acl.165/)を日本語LLMの評価においても使用できるように日本語に翻訳し、日本特有の用語や文化的背景を考慮して修正したデータセットとなります。

## データセットの概要
JBBQはAge, Disability status, Gender identity, Physical appearance, Sexual orientationの5カテゴリの計9つの社会的カテゴリに関する多岐選択式のQAデータセットです。
各カテゴリのテンプレートは、カテゴリに関する言及を含み曖昧性のある文脈、曖昧性を解消させる文脈、語彙、文脈に関してカテゴリに属するグループや人物に有害な偏見を引き起こす問題文（カテゴリに否定的な問題文）、中立的な問題文、回答選択肢（カテゴリに属する人物ラベル、カテゴリに属さない人物ラベル、曖昧性のある文脈のみからは答えが定まらないunknownラベルの3値）、テンプレート作成に参照したソースの情報、から主に構成されます。
テンプレートは全カテゴリで計245件(Age: 72件，Disability: 52件，Gender: 41件，Physical: 52件，Sexual: 28件）あり、テンプレートに語彙を代入して生成された問題数は計8476件(Age: 4696件，Disability: 1344件，Gender: 652件，Physical: 1256件，Sexual: 528件）あります。

### データフォーマット
データフォーマットは[BBQのデータフォーマット](https://github.com/nyu-mll/BBQ#models)に準拠しています。

- `question_polarity`: 対象とする社会カテゴリに対する否定的な問題（neg）か中立的な問題（nonneg）か
- `context_condition`: 文脈が曖昧のあるもの（ambig）か曖昧性を解消するもの（disambig）か
- `answer_info` : 質問に対する選択肢の属性の情報
- `additional_metadeta`: 対象とする社会カテゴリに関する情報と根拠となるURL
- `context`: 文脈文
- `question`: 質問文
- `ans0`, `ans1`, `ans2` : 質問に対する選択肢
- `label`: 質問の正解
- `is_additional`: 1であれば，JBBQで追加したテンプレート

英語のBBQデータセットの詳細は、以下の論文とリポジトリをご覧下さい。
[BBQ: A hand-built bias benchmark for question answering](https://aclanthology.org/2022.findings-acl.165/)
Alicia Parrish, Angelica Chen, Nikita Nangia, Vishakh Padmakumar, Jason Phang, Jana Thompson, Phu Mon Htut, Samuel Bowman [github](https://github.com/nyu-mll/BBQ)

## ご利用上の注意
データセットの利用をご希望の方は[こちらのフォーム]()に必要事項をご記入ください。データセットへのリンクをお送りします。この方法以外でのデータの再配布は禁止します。
本データセットはその性質上不適切な表現を含みます。承諾の上、LLMの安全性・公平性向上のためにご使用ください。
本データセットの利用においては、以下の参考文献をご参照ください。

## 参考文献
1. Hitomi Yanaka, Namgi Han, Ryoma Kumon, Jie Lu, Masashi Takeshita, Ryo Sekizawa, Taisei Kato, Hiromi Arai. Analyzing Social Biases in Japanese Large Language Models. 
    [[arXiv]](https://arxiv.org/), 2024.
2. 谷中瞳, 関澤瞭, 竹下昌志, 加藤大晴, Namgi Han, 荒井ひろみ. [日本語社会的バイアスQAデータセットの提案](https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/C7-4.pdf). 言語処理学会第30回年次大会, 2024.
   
```
@misc{yanaka-han-2024,
    title = "Analyzing Social Biases in Japanese Large Language Models",
    author = "Yanaka, Hitomi  and
      Han, Namgi and
      Kumon, Ryoma and
      Lu, Jie and
      Takeshita, Masashi and
      Sekizawa, Ryo and
      Kato, Taisei and
      Arai, Hiromi",
    year={2024},
    eprint={XX},
    archivePrefix={arXiv},
    primaryClass={cs.CL}
}
```

## 免責事項
本データセットの制作者は、利用者が利用者自身又は第三者に与えた損害について、一切の責任を負わないものとする。また、本データセットのサービス提供の遅延、中断又は停止により利用者又は第三者が被った損害について、制作者は一切の責任を負わないものとする。制作者は、予告なしに、本データセットの運営を停止もしくは中止し、又は本データに掲載される情報の全部若しくは一部を変更する場合がある。

## License
This work is licensed under a [Creative Commons Attribution 4.0 International License](LICENSE.txt).
