# 키워드 추출 (Keyword Extraction)

텍스트에서 중요한 키워드를 추출하는 것은 문서 분류, 검색, 요약 등 다양한 자연어 처리 작업에 필수적입니다. TextMiner Pro는 TF-IDF(Term Frequency-Inverse Document Frequency) 알고리즘을 기반으로 텍스트에서 중요한 키워드를 추출하는 기능을 제공합니다.

## 기본 사용법

```python
from textminer import extract_keywords

text = """
자연어 처리(NLP)는 컴퓨터와 인간 언어 간의 상호작용을 연구하는 
인공지능의 한 분야입니다. 자연어 처리 기술은 텍스트 분석, 기계 번역, 
음성 인식 등 다양한 응용 분야에서 활용됩니다.
"""

# 상위 5개 키워드 추출
keywords = extract_keywords(text, top_n=5)
print(keywords)
```

## 작동 방식

`extract_keywords` 함수는 다음과 같은 과정을 통해 키워드를 추출합니다:

1. 텍스트를 TF-IDF 벡터로 변환합니다.
2. 각 단어의 TF-IDF 점수를 계산합니다.
3. 점수가 높은 순서대로 단어를 정렬합니다.
4. 상위 `top_n`개의 단어를 반환합니다.

## 고급 사용법

여러 문서에서 키워드를 추출하고 비교할 수도 있습니다:

```python
from textminer import extract_keywords
from sklearn.feature_extraction.text import TfidfVectorizer

# 여러 문서에서 키워드 추출
documents = [
    "자연어 처리는 컴퓨터가 인간의 언어를 이해하는 기술입니다.",
    "기계 학습은 데이터로부터 패턴을 학습하는 인공지능의 한 분야입니다.",
    "딥러닝은 인공 신경망을 활용한 기계 학습의 한 종류입니다."
]

# 각 문서별로 키워드 추출
for i, doc in enumerate(documents):
    print(f"문서 {i+1}의 키워드:", extract_keywords(doc, top_n=3))
```

## API 레퍼런스

```python
def extract_keywords(text: str, top_n=5) -> list:
    """
    TF-IDF 기반으로 텍스트에서 중요한 키워드를 추출합니다.
    
    Args:
        text (str): 키워드를 추출할 원본 텍스트
        top_n (int): 반환할 상위 키워드 수 (기본값: 5)
        
    Returns:
        list: 상위 n개의 키워드 리스트
    """
```
