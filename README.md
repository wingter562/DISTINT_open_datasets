# Human vs. AI-translated Multilingual Corpora (HAM)
**Description**: High-quality multilingual parallel corpora (mostly public) paired with LLM-generated two-way translation. This dataset can be used for multiple purposes such as machine translation detection, translation fidelity evaluation, etc. 

**Contributors**: This dataset, as part of the *[Open data repository created by DISTINT group](https://github.com/wingter562/DISTINT_open_data "DISTINT open datasets")*, is contributed by Zixu Wangyu and Dr. Wentai Wu, Jinan University.

**Translators**: the corpora contain parallel human-written text pairs in Chinese and English, each can be regarded as human translation of the other. In addition, we used Large Language Models (LLMs) to perform neural machine translation (NMT) for both languages. This was done by prompting with the human-written text and translation instruction as the context. 

**LLMs used**: GLM-3-9b, DeepSeek V3 671b, 

**Meta data**:
- _languages_: English, Chinese
- _size_: 53821
- _sectors_: 3 ("Science", "Law", "Finance")
- _fields_:
  - "sample_id": Indices, integer (1 to 53821)
  - "raw_Chinese": human-written sentences in Chinese
  - "raw_English": human-written sentences in English parallel to the value stored in the "Chinese" field.
  - "GLM_Cn2En": GLM-based neural machine Chinese-to-English translation of the "raw_Chinese" field.
  - "GLM_En2Cn": GLM-based neural machine English-to-Chinese translation of the "raw_English" field.
  - "DS_Cn2En": DeepSeek-based neural machine Chinese-to-English translation of the "raw_Chinese" field.
  - "DS_En2Cn": DeepSeek-based neural machine English-to-Chinese translation of the "raw_English" field.

