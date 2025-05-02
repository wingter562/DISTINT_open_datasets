# Human vs. AI-translated Multilingual Corpora (HAM)
**Description**: High-quality multilingual parallel corpora (mostly public) paired with LLM-generated two-way translation. This dataset can be used for multiple purposes such as machine translation detection, translation fidelity evaluation, etc. 

**Contributors**: This dataset, as part of the *[DISTINT Open data Repository (DOR)](https://github.com/wingter562/DISTINT_open_data "DISTINT Open data Repository (DOR)")*, is contributed by Yutszyuk Wong and Dr. Wentai Wu, Jinan University.

**Translators**: the corpora contain parallel human-written text pairs in Chinese and English, each can be regarded as human translation of the other. In addition, we used Large Language Models (LLMs) to perform neural machine translation (NMT) for both languages. This was done by prompting with the human-written text and translation instruction as the context. 

**LLMs used**: DeepSeek V3 671b, QwQ-32B, 

--- 

**_Disclaimer_**: This dataset is derived from the online public corpus collection _CQPweb_ (https://corpus.bfsu.edu.cn/index.htm), without any modification to the raw text. The human-written raw text provided is made available **"as is"**. The creator(s) of this dataset do not guarantee the accuracy, completeness, or reliability of the information contained within. We are not responsible for any misinformation or inproper statement contained.

By using this dataset, you acknowledge that:  
- The data may contain errors, inaccuracies, or outdated information.  
- The dataset is not intended as professional, legal, medical, financial, or other expert advice.  
- You assume full responsibility for any decisions or actions taken based on this dataset.  

The creator(s) of this dataset **shall not be held liable** for any damages, losses, or consequences arising from the use, interpretation, or reliance on this data. Users are encouraged to independently verify the information before applying it in any context.  

---  

**Meta data**:
- _languages_: English, Chinese
- _size_: 53809
- _sectors_: 3 ("Science", "Law", "Finance")

### HumanText_Dataset
- "sample_id": Indices, integer (1 to 53809)
- "raw_Chinese": human-written sentences in Chinese
- "raw_English": human-written sentences in English parallel with the those stored in the "raw_Chinese" field.

### DS_Cn2En
- "id": Indices, integer (1 to 53809)
- "query_text_cn": raw sentences consistent with the "raw_Chinese" field in the HumanText_Dataset.
- "translation": **Deepseek**-based neural machine Chinese-to-English translation of the "query_text_cn" field.

### DS_En2Cn
- "id": Indices, integer (1 to 53809)
- "query_text_en": raw sentences consistent with the "raw_English" field in the HumanText_Dataset.
- "translation": **Deepseek**-based neural machine English-to-Chinese translation of the "query_text_en" field.

### Qw_Cn2En
- "id": Indices, integer (1 to 53809)
- "query_text_cn": raw sentences consistent with the "raw_Chinese" field in the HumanText_Dataset.
- "translation": **Qwen**-based neural machine Chinese-to-English translation of the "query_text_cn" field.

### Qw_En2Cn
- "id": Indices, integer (1 to 53810)
- "query_text_en": raw sentences consistent with the "raw_English" field in the HumanText_Dataset.
- "translation": **Qwen**-based neural machine English-to-Chinese translation of the "query_text_en" field.

