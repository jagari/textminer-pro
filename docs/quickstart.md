# 빠른 시작 가이드

이 가이드는 TextMiner Pro의 기본 기능을 빠르게 살펴볼 수 있도록 도와줍니다.

## 기본 사용법

먼저 필요한 기능을 임포트합니다:

```python
from textminer import remove_stopwords, extract_keywords, summarize, detect_language
```

### 불용어 제거

```python
text = "This is a sample text with some stopwords like is, a, with"
clean_text = remove_stopwords(text)
print(clean_text)  # "This sample text stopwords like"
```

### 키워드 추출

```python
text = """
자연어 처리(NLP)는 컴퓨터와 인간 언어 간의 상호작용을 연구하는 
인공지능의 한 분야입니다. 자연어 처리 기술은 텍스트 분석, 기계 번역, 
음성 인식 등 다양한 응용 분야에서 활용됩니다.
"""
keywords = extract_keywords(text, top_n=5)
print(keywords)  # ['자연어', '처리', '인공지능', '기술', '분야']
```

### 텍스트 요약

```python
long_text = """
자연어 처리(NLP)는 언어학, 컴퓨터 과학, 인공지능의 하위 분야로, 
컴퓨터와 인간 언어 간의 상호작용에 관한 분야입니다. 특히 컴퓨터가 
대량의 자연어 데이터를 처리하고 분석하도록 프로그래밍하는 방법에 관한 
연구입니다. 자연어 처리의 과제로는 언어 이해, 생성, 번역 등이 있습니다. 
현대의 접근 방식은 딥러닝에 크게 의존하고 있습니다. 자연어 처리 기술은 
음성 인식, 문서 분류, 기계 번역, 스팸 필터링, 가상 비서 등 다양한 분야에서 
응용됩니다.
"""
summary = summarize(long_text, ratio=0.3)
print(summary)
```

### 언어 감지

```python
print(detect_language("이것은 한국어 문장입니다"))  # 'ko'
print(detect_language("This is an English sentence"))  # 'en'
print(detect_language("これは日本語の文章です"))  # 'ja'
print(detect_language("这是一个中文句子"))  # 'zh-cn'
```