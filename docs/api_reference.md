# API 레퍼런스

TextMiner Pro의 모든 공개 API에 대한 상세한 문서입니다.

## 불용어 제거

```python
from textminer import remove_stopwords

def remove_stopwords(text: str, lang='english') -> str:
    """
    불용어를 제거하는 함수
    
    Args:
        text (str): 원본 텍스트
        lang (str): 언어 코드 (기본값: 'english')
        
    Returns:
        str: 불용어가 제거된 텍스트
        
    Example:
        >>> remove_stopwords("This is a sample text", lang='english')
        'This sample text'
    """
```

## 키워드 추출

```python
from textminer import extract_keywords

def extract_keywords(text: str, top_n=5) -> list:
    """
    TF-IDF 기반으로 텍스트에서 중요한 키워드를 추출합니다.
    
    Args:
        text (str): 키워드를 추출할 원본 텍스트
        top_n (int): 반환할 상위 키워드 수 (기본값: 5)
        
    Returns:
        list: 상위 n개의 키워드 리스트
        
    Example:
        >>> extract_keywords("자연어 처리는 컴퓨터 과학의 중요한 분야입니다", top_n=3)
        ['자연어', '처리', '컴퓨터']
    """
```

## 텍스트 요약

```python
from textminer import summarize

def summarize(text: str, ratio=0.2) -> str:
    """
    TF-IDF 기반 텍스트 요약 함수
    
    Args:
        text (str): 요약할 원본 텍스트
        ratio (float): 원본 대비 요약 비율 (0.0~1.0)
        
    Returns:
        str: 요약된 텍스트
        
    Example:
        >>> summarize(long_text, ratio=0.3)
        '자연어 처리(NLP)는 언어학, 컴퓨터 과학, 인공지능의 하위 분야로...'
    """
```

## 언어 감지

```python
from textminer import detect_language

def detect_language(text: str) -> str:
    """
    텍스트의 언어를 감지합니다.
    
    Args:
        text (str): 언어를 감지할 원본 텍스트
        
    Returns:
        str: ISO 639-1 표준의 언어 코드
        
    Example:
        >>> detect_language("This is English text")
        'en'
        >>> detect_language("이것은 한국어 텍스트입니다")
        'ko'
    """
```
