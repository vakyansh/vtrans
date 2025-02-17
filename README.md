
# vtrans v0.0.1
**A Translation Corpus for Indic Languages with Formal and Colloquial Hindi-English Code-Mixed Variants**  

---

## 🚀 Overview  
Most existing translation systems produce formal translations that use complex words, making them difficult for everyday users to understand. These systems often generate literal translations due to the nature of the data they were trained on.  

**vtrans** introduces a new paradigm for collecting parallel data, focusing on formal and colloquial Hindi-English code-mixed translations. Designed for NLP research, this project serves as a proof of concept (POC) for gathering parallel corpora in a way that better reflects real-world language usage.

In v0.0.1, we are releasing a small dataset of 15,000+ entries as a POC.

---

## 💡 Problem Statement  
Most translation systems today:  
- Use formal, complex words that aren't easily understandable for general readers.  
- Generate literal translations due to conventional data collection methods.  

**vtrans** aims to bridge this gap by providing:  
- Formal translations for professional or official use.  
- Colloquial translations that are more relatable and easier to understand.  
- Code-mixed versions that reflect real-world usage, particularly in bilingual or multilingual communities.  

This dataset is specifically curated for research in Natural Language Processing (NLP), focusing on the nuances of formal and informal language usage in Hindi-English code-mixed contexts.  
---

## 📁 Dataset Structure  
Each entry in the dataset is a JSON object with the following fields:  

```json
{
  "input": "Original English text",
  "formal": {
    "hindi": "Formal Hindi translation",
    "translit": "Readable Formal Transliteration",
    "code_mixed": "Hindi-English code-mixed formal version"
  },
  "colloquial": {
    "hindi": "Colloquial Hindi translation",
    "translit": "Readable Colloquial Transliteration",
    "code_mixed": "Hindi-English code-mixed colloquial version"
  },
  "metadata": {
    "domain": "Domain of the input sentence (e.g., politics, sports, entertainment)",
    "sentiment": "Sentiment of the input sentence (e.g., positive, negative, neutral)",
    "gender_specific": null (will be present in v0.0.2)
  }
}
```

### 📌 Example Entry:  

```json
{
  "input": "READ WATCH YOU MAY CALL ME PAPPU BUT I DONT HATE YOU RAHUL HUGS PM MODI",
  "formal": {
    "hindi": "पढ़िए, देखिए, आप मुझे पप्पू कह सकते हैं, लेकिन मैं आपसे नफ़रत नहीं करता। राहुल ने प्रधानमंत्री मोदी को गले लगाया।",
    "translit": "Padhiye, dekhiye, aap mujhe Pappu kah sakte hain, lekin main aapse nafrat nahin karta. Rahul ne PM Modi ko gale lagaya.",
    "code_mixed": "पढ़िए, देखिए, आप मुझे पप्पू कह सकते हैं, लेकिन मैं आपसे नफ़रत नहीं करता। Rahul ने PM Modi को गले लगाया।"
  },
  "colloquial": {
    "hindi": "देखो भाई, तुम मुझे पप्पू बोल सकते हो, पर मैं तुमसे नफरत नहीं करता। राहुल ने पी एम मोदी को गले लगाया।",
    "translit": "Dekho bhai, tum mujhe Pappu bol sakte ho, par main tumse nafarat nahin karta. Rahul ne PM Modi ko gale lagaya.",
    "code_mixed": "देखो भाई, तुम मुझे पप्पू बोल सकते हो, पर मैं तुमसे नफरत नहीं करता। Rahul ने PM Modi को गले लगाया।"
  },
  "metadata": {
    "domain": "politics",
    "sentiment": "neutral"
  },
  "gender_specific": null
}
```
Complete data can be found in data/data.jsonl.zip file.

---

## 📊 Key Features  
- **Formal vs. Colloquial Translations:** Captures different tones and styles for the same input text.  
- **Code-Mixed Variants:** Reflects real-world conversational patterns in bilingual communities.  
- **Rich Metadata:** Includes domain and sentiment tags to facilitate contextual NLP research.  
- **Transliterations:** Multiple transliteration styles to support phonetic understanding and pronunciation.  

---

## 🔍 Use Cases  
This dataset is particularly useful for:  
- **Machine Translation:** Enhancing translation systems to produce more relatable and contextually accurate outputs.  
- **Code-Mixing Studies:** Researching bilingual communication patterns, especially in social media contexts.  
- **Speech Synthesis and ASR:** Improving Text-to-Speech and Automatic Speech Recognition systems for code-mixed languages.  

---

## 🙌 Contributing  
We welcome contributions to:  
- Improve translations and transliterations.  
- Add new metadata fields for better contextual analysis.  
- Fix errors or inconsistencies in existing entries.  

For more details, please refer to the `sample.json` to understand the data structure.  

---

## 📜 License & Usage  
### Code & Methodology  
- **Apache License 2.0**  
  - Users cannot patent derivatives of this work.  
  - Free to use, modify, and distribute with attribution.  

### Dataset  
- **CC-BY-4.0**  
  - Requires attribution when redistributed or used.  
  - Allows for modification and commercial use with proper credit.  

---
