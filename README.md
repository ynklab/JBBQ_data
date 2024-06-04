# JBBQ: 日本語社会性バイアスQAデータセット
repository for the Japanese Bias Benchmark for QA dataset (JBBQ).

本データセット(JBBQ)は英語の社会性バイアスQAデータセットBBQを日本語LLMの評価においても使用できるように日本語に翻訳し、日本特有の用語や文化的背景を考慮して修正したデータセットとなります。

BBQの詳細は以下の論文とリポジトリをご覧下さい。

[BBQ: A hand-built bias benchmark for question answering](https://aclanthology.org/2022.findings-acl.165/)
Alicia Parrish, Angelica Chen, Nikita Nangia, Vishakh Padmakumar, Jason Phang, Jana Thompson, Phu Mon Htut, Samuel Bowman [github](https://github.com/nyu-mll/BBQ)

## 評価

### タスク
- Multi-class classification
    - 入力： `context` + `question` 
    - 出力： `ans0` or `ans1` or `ans2`
    - [BBQでのフォーマット](https://github.com/nyu-mll/BBQ#models)

## References
1. Hitomi Yanaka, Namgi Han, Ryoma Kumon, Jie Lu, Masashi Takeshita, Ryo Sekizawa, Taisei Kato, Hiromi Arai. Analyzing Social Biases in Japanese Large Language Models. 
    [[arXiv]](https://arxiv.org/), 2024.
2. 谷中瞳, 関澤瞭, 竹下昌志, 加藤大晴, Namgi Han, 荒井ひろみ. [日本語社会的バイアスQAデータセットの提案](https://www.anlp.jp/proceedings/annual_meeting/2024/pdf_dir/C7-4.pdf). 言語処理学会第30回年次大会, 2024.

If you use this dataset in any published research, please cite the following:
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

## License
This work is licensed under a [Creative Commons Attribution 4.0 International License](LICENSE.txt).
