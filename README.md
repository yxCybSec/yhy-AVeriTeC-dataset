This repository maintains the dataset described in the paper [AVeriTeC: A Dataset for Real-world Claim Verification with Evidence from the Web](https://arxiv.org/abs/2305.13117).
### Format 格式

The dataset is formatted as JSON, with each split located as a separate file in the `data/`-folder. Each claim is an object of the following form:

该数据集采用 JSON 格式，每个拆分部分作为单独的文件位于 `data/` 文件夹中。每个声明都是具有以下形式的对象：

```json
{
  "claim": "The claim text itself",
  "required_reannotation": "True or False. Denotes that the claim received a second round of QG-QA and",
  "label": "The annotated verdict for the claim",
  "justification": "A textual justification explaining how the verdict was reached from the question-a",
  "claim_date": "Our best estimate for the date the claim first appeared",
  "speaker": "The person or organization that made the claim, e.g. Barrack Obama, The Onion.",
  "original_claim_url": "If the claim first appeared on the internet, a url to the original location",
  "cached_original_claim_url": "Where possible, an archive.org link to the original claim url",
  "fact_checking_article": "The fact-checking article we extracted the claim from",
  "reporting_source": "The website or organization that first published the claim, e.g. Facebook, CNN.",
  "location_ISO_code": "The location most relevant for the claim. Highly useful for search.",
  "claim_types": [
    "The types of the claim",
  ],
  "fact_checking_strategies": [
    "The strategies employed in the fact-checking article",
  ],
  "questions": [
    {
      "question": "A fact-checking question for the claim",
      "answers": [
        {
          "answer": "The answer to the question",
          "answer_type": "Whether the answer was abstractive, extractive, boolean, or unanswer",
          "source_url": "The source url for the answer",
          "cached_source_url": "An archive.org link for the source url",
          "source_medium": "The medium the answer appeared in, e.g. web text, a pdf, or an ima"
        }
      ]
    },
  ]
}
