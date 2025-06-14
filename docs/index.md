# TextMiner Pro

![GitHub Actions](https://img.shields.io/github/workflow/status/jagari/textminer-pro/Python%20Package)
![PyPI](https://img.shields.io/pypi/v/textminer-pro-InjinSung)
![License](https://img.shields.io/github/license/jagari/textminer-pro)

`textminer-pro`는 파이썬 기반의 고급 텍스트 분석 도구입니다.

## 주요 기능

- **불용어 제거**: 의미 없는 단어들을 텍스트에서 제거합니다
- **핵심 키워드 추출**: TF-IDF 기반으로 중요한 키워드를 추출합니다
- **텍스트 요약**: 긴 문서를 요약하여 핵심 내용만 추출합니다
- **언어 감지**: 텍스트의 언어를 자동으로 식별합니다

## 예제 코드

```python
from textminer import remove_stopwords, extract_keywords, summarize, detect_language

# 불용어 제거
text = "This is a sample text with some stopwords"
clean_text = remove_stopwords(text)

# 키워드 추출
keywords = extract_keywords("자연어 처리는 컴퓨터가 인간의 언어를 이해하는 기술입니다")
print(keywords)  # ['자연어', '처리', '언어', '이해', '기술']

# 텍스트 요약
summary = summarize(long_text, ratio=0.3)  # 원본의 30% 길이로 요약

# 언어 감지
lang = detect_language("이것은 한국어 문장입니다")
print(lang)  # 'ko'
```
