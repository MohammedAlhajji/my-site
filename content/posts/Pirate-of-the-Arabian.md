+++
title = 'Pirates of the Arabian'
date = 2023-10-19T20:41:47+03:00
draft = false
+++

# Pirates of the Arabian 

A couple of months ago, Inception, a G42 company, Mohamed bin Zayed University of Artificial Intelligence (MBZUAI), Cerebras Systems, an archaeologist, a server at Wingstop, and a forklift operator announced the release of [JAIS](https://mbzuai.ac.ae/news/meet-jais-the-worlds-most-advanced-arabic-large-language-model-open-sourced-by-g42s-inception/), supposedly the best open-source Arabic model for its size.


## The Dataset
The model was pretrained on approximately 33% Arabic text; this text contains wiki articles, news articles, Arabic books, and social media content. Notably, a part of the dataset was, in fact, translated from English text using Inception's in-house translation model.


## How Does it Perform?
### Chat
- Bad. its responses sound unnatural. I suppose the translated english text has affected its ability to respond in Arabic text. More importantly, it is not able to understand context well. For example: ويش معنى قرصان؟ (What does pirate mean?) The model responds with: "أنا آسف، لكن ذلك ليس سؤالا مناسبًا لطرحه كمساعد مسؤول وأخلاقيًا."
- LLAMA actually does a better job at this. It responds saying it's a type of bakery, which is right, but it describes the ingredients and they are not right. or maybe they are and I just suck at baking.

### Sentiment Analysis
- Sucks. It's fine with simple examples, but something like "متت من الفرح" would trip it up. It actually tells me that my grammar is wrong???? 
- The LLAMA 13b model (`meta-llama/Llama-2-13b-chat-hf`), which is of the same size, answers it better. 

### Translation
- Much better than equivalent LLAMA models! When it works. 
- It seems safety is set too high, and a lot of times it would refuse to translate sentences like this random Taylor Swift line: "You know the greatest films of all time were never made."

### Named Entity Recognition
- Requires a lot of handholding, sadly, compared to equivalent LLAMA models.

## Thoughts
I'm not going to sit behind a keyboard and just critique someone's work. I'm sure they've put a lot of effort into this. However, if you thought this is a model that's ready for production level use, you'd be wrong. But what's production-ready anyway? Well, come back next week (week=whenever).
