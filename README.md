# Human vs. AI-translated Multilingual Corpora (HAM)
**Description**: High-quality multilingual parallel corpora (mostly public) paired with LLM-generated two-way translation. This dataset can be used for multiple purposes such as machine translation detection, translation fidelity evaluation, etc. 

**Contributors**: This dataset, as part of the *[DISTINT Open data Repository (DOR) created by DISTINT group](https://github.com/wingter562/DISTINT_open_data "DISTINT open datasets")*, is contributed by Yutszyuk Wong and Dr. Wentai Wu, Jinan University.

**Translators**: the corpora contain parallel human-written text pairs in Chinese and English, each can be regarded as human translation of the other. In addition, we used Large Language Models (LLMs) to perform neural machine translation (NMT) for both languages. This was done by prompting with the human-written text and translation instruction as the context. 

**LLMs used**: DeepSeek V3 671b, QwQ-32B, 

**Meta data**:
- _languages_: English, Chinese
- _size_: 53810
- _sectors_: 3 ("Science", "Law", "Finance")

### HumanText_Dataset
- "sample_id": Indices, integer (1 to 53810)
- "raw_Chinese": human-written sentences in Chinese
- "raw_English": human-written sentences in English parallel with the those stored in the "raw_Chinese" field.

### DS_Cn2En
- "id": Indices, integer (1 to 53810)
- "query_text_cn": raw sentences consistent with the "raw_Chinese" field in the HumanText_Dataset.
- "translation": **Deepseek**-based neural machine Chinese-to-English translation of the "query_text_cn" field.

### DS_En2Cn
- "id": Indices, integer (1 to 53810)
- "query_text_en": raw sentences consistent with the "raw_English" field in the HumanText_Dataset.
- "translation": **Deepseek**-based neural machine English-to-Chinese translation of the "query_text_en" field.

### Qw_Cn2En
- "id": Indices, integer (1 to 53810)
- "query_text_cn": raw sentences consistent with the "raw_Chinese" field in the HumanText_Dataset.
- "translation": **Qwen**-based neural machine Chinese-to-English translation of the "query_text_cn" field.

### Qw_En2Cn
- "id": Indices, integer (1 to 53810)
- "query_text_en": raw sentences consistent with the "raw_English" field in the HumanText_Dataset.
- "translation": **Qwen**-based neural machine English-to-Chinese translation of the "query_text_en" field.

