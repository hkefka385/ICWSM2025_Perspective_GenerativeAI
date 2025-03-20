# README

## Paper Reference
**Title:** _Linguistic Landscape of Generative AI Perception: A Global Twitter Analysis Across 14 Languages_  
**URL:** [\[https://arxiv.org/abs/2405.20037\]](https://arxiv.org/abs/2405.20037)  
**Abstract (Optional):**  
> The advent of generative AI tools has had a profound impact on societies globally, transcending geographical boundaries. Understanding these tools' global reception and utilization is crucial for service providers and policymakers in shaping future policies. Therefore, to unravel the perceptions and engagements of individuals within diverse linguistic communities with regard to generative AI tools, we extensively analyzed over 6.8 million tweets in 14 different languages. Our findings reveal a global trend in the perception of generative AI, accompanied by language-specific nuances. While sentiments toward these tools vary significantly across languages, there is a prevalent positive inclination toward Image tools and a negative one toward Chat tools. Notably, the ban of ChatGPT in Italy led to a sentiment decline and initiated discussions across languages. Furthermore, we established a taxonomy for interactions with chatbots, creating a framework for social analysis underscoring variations in generative AI usage among linguistic communities. We find that the Chinese community predominantly employs chatbots as substitutes for search, while the Italian community tends to present more intricate prompts. Our research provides a robust foundation for further explorations of the social dynamics surrounding generative AI tools and offers invaluable insights for decision-makers in policy, technology, and education.


---

## Overview

This repository contains three datasets related to the use and perception of Generative AI on Twitter. The data is collected and organized as part of [the above-mentioned paper](#paper-reference) (_hereinafter referred to as “the Paper”_).

### 1. `tweetsID.csv`
- **Description:**  
  This CSV file contains Twitter post metadata—specifically, the Tweet ID, language information, and a list of Generative AI tools mentioned in each tweet.
- **Columns:**
  1. **TweetID**  
     - Unique ID of the tweet  
  2. **Language**  
     - Language of the tweet  
  3. **Generative AI tool**  
     - A list of Generative AI tools referenced in the tweet
- **Use Cases:**
  - Use the `TweetID` to retrieve tweet text from the Twitter API (subject to Twitter’s Terms of Service).  
  - Helpful for analyzing tweet counts by language or by which AI tools are most frequently mentioned.

### 2. `InteractionDataset`
- **Description:**  
  This folder-based dataset contains .xlsx files, each corresponding to a particular language. These files come from tweets that include screenshots of ChatGPT usage. The text from the screenshots is extracted via OCR.
- **File Contents (per .xlsx file):**
  1. **User**  
     - The user’s prompt to ChatGPT  
  2. **ChatGPT**  
     - ChatGPT’s original response  
  3. **User (translate in English)**  
     - English translation of the user’s prompt  
  4. **ChatGPT (translate in English)**  
     - English translation of ChatGPT’s response  
  5. **TweetID**  
     - ID of the tweet containing the screenshot  
  6. **Date**  
     - Date the screenshot was posted
- **Use Cases:**
  - Analyze real examples of user–ChatGPT interactions in multiple languages.
  - Compare how prompts differ across various languages or cultural contexts.

### 3. `chatbot_usage_dataset.csv`
- **Description:**  
  This CSV contains annotated data on how users employ ChatGPT, based on screenshots included in tweets. These annotations follow the taxonomy defined in the Paper.
- **Columns:**
  1. **Main-Category**  
     - The high-level category describing how ChatGPT is being used (e.g., “Search,” “Support for Business or Creative Tasks,” etc.)  
  2. **Sub-Category**  
     - A more granular classification under the main category  
  3. **User**  
     - The user’s original prompt  
  4. **ChatGPT**  
     - ChatGPT’s original response  
  5. **User (translation in English)**  
     - English translation of the user’s prompt  
  6. **ChatGPT (translation in English)**  
     - English translation of ChatGPT’s response  
  7. **Language**  
     - The language in which the prompt was made
- **Use Cases:**
  - Understand user behavior by categorizing ChatGPT use cases (e.g., searching for information, seeking creative support, etc.).  
  - Compare usage patterns by language or region.

---

## Usage Notes

1. **Data Privacy**  
   - While this repository does not contain direct tweet text, `TweetID` can be used to fetch the original tweets through Twitter’s API. Please ensure compliance with Twitter’s Terms of Service and privacy policies if you retrieve original tweet content.
2. **Copyright & License**  
   - Each tweet is copyright by its respective creator. The datasets here are meant primarily for research and academic use.  
   - If you plan to use or redistribute the data, please do so responsibly and in accordance with the license terms (if specified). Always include citations to this repository and the Paper.
3. **Limitations**  
   - Some information may be incomplete or imperfect (e.g., OCR errors, translation inaccuracies).  
   - The dataset’s coverage is limited to specific Generative AI tools and time periods. It may not capture every emergent tool or usage scenario.
4. **Updates**  
   - We may update or extend these datasets over time. Check the repository for any additions or improvements.  
   - Please open an Issue or Pull Request for any feedback or bug reports.

---

## Citation

If you use these datasets for your research, please cite the Paper and, if required, reference this repository.

