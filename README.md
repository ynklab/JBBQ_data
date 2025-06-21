# Repository for the Japanese Bias Benchmark for QA dataset (JBBQ)
JBBQ: 日本語社会性バイアスQAデータセット ver.1

This dataset (JBBQ ver.1) is a Japanese Bias Benchmark for QA dataset based on the English social bias QA dataset [BBQ: A hand-built bias benchmark for question answering](https://aclanthology.org/2022.findings-acl.165/).
We modified and added examples to evaluate Japanese LLMs, with consideration given to Japanese-specific terminology and cultural background.

本データセット(JBBQ ver.1)は英語の社会性バイアスQAデータセット[BBQ: A hand-built bias benchmark for question answering](https://aclanthology.org/2022.findings-acl.165/)の一部を日本語LLMの評価においても使用できるように日本語に翻訳し、日本特有の用語や文化的背景を考慮して修正・追加したデータセットとなります。

## Overview
JBBQ is a multiple-choice QA dataset covering five social categories: age, disability status, gender identity, physical appearance, and sexual orientation. 
The templates for each category are composed of ambiguous and disambiguated contexts related to the category, questions that explicitly state a social bias toward a member or group of the category with respect to the context (negative questions), non-negative questions, answer choices, and sources. 
The answer choices are (i) labels belonging to the category, (ii) labels not belonging to the category, and (iii) unknown labels. 
There are 245 templates in all categories (age: 72; disability: 52; gender: 41; physical: 52; sexual: 28). 
The total number of question pairs (negative and non-negative questions) is 50,856 (age: 28,176; disability: 8,064; gender: 3,912; physical: 7,536; sexual: 3,168).

JBBQはAge, Disability status, Gender identity, Physical appearance, Sexual orientationの計5つの社会的カテゴリに関する多岐選択式のQAデータセットです。
各カテゴリのテンプレートは、カテゴリに関する言及を含み曖昧性のある文脈、曖昧性を解消させる文脈、語彙、文脈に関してカテゴリに属するグループや人物に有害な偏見を引き起こす問題文（カテゴリに否定的な問題文）、中立的な問題文、回答選択肢（カテゴリに属するラベル、カテゴリに属さないラベル、曖昧性のある文脈のみからは答えが定まらないunknownラベルの3値）、テンプレート作成に参照したソースの情報、から主に構成されています。
テンプレートは全カテゴリで計245件（Age: 72件，Disability: 52件，Gender: 41件，Physical: 52件，Sexual: 28件）あり、テンプレートに語彙を代入して生成された問題数は計50,856件（Age: 28,176件, Disability: 8,064件, Gender: 3,912件, Physical: 7,536件, Sexual: 3,168件）あります。

### Data format
Our data format is based on [BBQ](https://github.com/nyu-mll/BBQ#models).
データフォーマットは[BBQ](https://github.com/nyu-mll/BBQ#models)に準拠しています。

- `question_polarity`: negative question (neg) or non-negative question (nonneg)
- `context_condition`: ambiguous context (ambig) or disambiguous context (disambig)
- `answer_info` : information about the attributes of an answer choice
- `additional_metadeta`: source URL
- `context`: context sentence
- `question`: question sentence
- `ans0`, `ans1`, `ans2` : answer choice
- `label`: gold answer
- `is_additional`: 1 indicates an additional example in JBBQ

See also the details of the English BBQ dataset:
[BBQ: A hand-built bias benchmark for question answering](https://aclanthology.org/2022.findings-acl.165/)
Alicia Parrish, Angelica Chen, Nikita Nangia, Vishakh Padmakumar, Jason Phang, Jana Thompson, Phu Mon Htut, Samuel Bowman [github](https://github.com/nyu-mll/BBQ)

## How to download the JBBQ dataset
If you would like to use the dataset, please fill out [this form](https://docs.google.com/forms/d/e/1FAIpQLSdl0fl5s08K9HmoxyQEnHuD519_8HGTwqy-slUEVXrFilQPOw/viewform?usp=sf_link). We will send you a link to the dataset. Redistribution of the data by any other means is prohibited. 
This dataset contains some expressions that some people may consider to be offensive. Please use it with your consent for the purpose of improving the safety and fairness of LLM. Please refer to the following references when using this dataset.

データセットの利用をご希望の方は[こちらのフォーム](https://docs.google.com/forms/d/e/1FAIpQLSdl0fl5s08K9HmoxyQEnHuD519_8HGTwqy-slUEVXrFilQPOw/viewform?usp=sf_link)に必要事項をご記入ください。データセットへのリンクをお送りします。この方法以外でのデータの再配布は禁止します。
本データセットはその性質上不適切な表現を含みます。承諾の上、LLMの安全性・公平性向上のためにご利用ください。
本データセットの利用においては、以下の参考文献をご参照ください。

## References

1. Hitomi Yanaka, Namgi Han, Ryoma Kumon, Jie Lu, Masashi Takeshita, Ryo Sekizawa, Taisei Kato, Hiromi Arai. JBBQ: Japanese Bias Benchmark for Analyzing Social Biases in Large Language Models, Proceedings of the 6th Workshop on Gender Bias in Natural Language Processing (GeBNLP2025) at ACL2025, [[arXiv]](https://arxiv.org/abs/2406.02050), 2025.
2. 谷中瞳, 関澤瞭, 竹下昌志, 加藤大晴, Namgi Han, 荒井ひろみ. [日本語社会的バイアスQAデータセットの提案](https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/C7-4.pdf). 言語処理学会第30回年次大会, 2024.
   
```
@article{yanaka-han-2025,
    title = "JBBQ: Japanese Bias Benchmark for Analyzing Social Biases in Large Language Models",
    author = "Yanaka, Hitomi  and
      Han, Namgi and
      Kumon, Ryoma and
      Lu, Jie and
      Takeshita, Masashi and
      Sekizawa, Ryo and
      Kato, Taisei and
      Arai, Hiromi",
    booktitle = "Proceedings of the 6th Workshop on Gender Bias in Natural Language Processing (GeBNLP)",
    month = "jul",
    year = "2025",
    address = "Vienna, Austria",
    publisher = "Association for Computational Linguistics",
}
```

## Disclaimers

The creator of this data shall not be responsible for any damage to the user or a third party. In addition, the creator shall not be responsible for any damage to the users or third parties due to delays, interruptions, or suspensions of the provision of this data service. The creator may suspend or discontinue the service of this data or modify the information contained in this data without prior notice.

本データの制作者は、利用者が利用者自身又は第三者に与えた損害について、一切の責任を負わないものとする。また、本データのサービス提供の遅延、中断又は停止により利用者又は第三者が被った損害について、制作者は一切の責任を負わないものとする。制作者は、予告なしに、本データの運営を停止若しくは中止し、又は本データに掲載される情報の全部若しくは一部を変更する場合がある。

## License
This work is licensed under a [Creative Commons Attribution 4.0 International License](LICENSE).
